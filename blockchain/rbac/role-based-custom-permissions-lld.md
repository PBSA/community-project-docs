# Role-Based Custom Permissions LLD

### 1. Purpose <a id="1.-Purpose"></a>

The purpose of this document is to provide a low-level design for the creation of role-based custom permissions on the Peerplays blockchain.

###  <a id="2.-Scope"></a>

### 2. Scope <a id="2.-Scope"></a>

The design requirement listed in this document will be limited to the creation of new custom permissions linked to the Peerplays accounts.

The document will also outline the linking of operation\(s\) to the permissions created.

The document will also outline the way the custom permission objects and their respective indices are stored and purged on the blockchain.

###  <a id="3.-Background[hardBreak]"></a>

### 3. Background   <a id="3.-Background[hardBreak]"></a>

The current Peerplays accounts have only two types of permissions; owner and active.

The owner and active permissions are tightly coupled into the account struct.

For any operation to be authorized successfully on a Peerplays account a signature of either of the authorities is required.

In order to increase the security of the blockchain and it’s accounts, there is a need to introduce more sophisticated and fine-grained access control for the accounts.

###  <a id="4.-Current-Permission-Structure"></a>

### 4. Current Permission Structure <a id="4.-Current-Permission-Structure"></a>

Every account that’s created on Peerplays has two default permissions by default.

1. Owner
2. Active

They have a parent-child relationship by default \(owner being the parent\).

####  <a id="4.1.1-Owner"></a>

#### 4.1.1 Owner <a id="4.1.1-Owner"></a>

The owner permission sits at the root of the permission hierarchy for every account.

It is, therefore, the highest relative permission an account can have within its permission structure.

Although the owner permission can do anything a lower level permission can, it is typically used for recovery purposes when a lower permission has been compromised.

As such, keys associated with the owner permission are typically kept in cold storage, not used for signing regular operations.

####  <a id="4.1.2-Active"></a>

#### 4.1.2 Active <a id="4.1.2-Active"></a>

The implicit default permission linked to all operations is active, which sits one level below the owner permission within the hierarchy structure.

As a result, the active permission can do anything the owner permission can, except changing the keys associated with the owner.

####  <a id="4.2-Authorities"></a>

#### 4.2 Authorities <a id="4.2-Authorities"></a>

In Peerplays \(graphene-based chains\), an authority consists of one or many entities that authorize an operation, such as transfers or bet placement, etc.

Authority consists of one or several pairs of an account name with a weight.

In order to obtain a valid transaction, the sum of the weights from signing the parties has to exceed the threshold as defined in the permissions.

Also, the permissions are designed around people, rather than around cryptography, making it easy to use.

Every account can be controlled by any weighted combination of other accounts and private keys.

####  <a id="4.3-Transaction-Verification"></a>

#### 4.3 Transaction Verification <a id="4.3-Transaction-Verification"></a>

Each transaction is verified based on the signatures received in the signed transaction.

If any of the active or owner permission related signature is present, the transaction is verified successfully.

If there are any unwanted extra signatures either valid or invalid other than the ones required for successful verification, the transaction is rejected.

The same verification logic is applied to both the transactions received as part of the blocks or the standalone transactions received over the network.

###  <a id="5.-Design-Changes"></a>

### 5. Design Changes <a id="5.-Design-Changes"></a>

The aim of the design is to decouple the new custom permissions from the accounts and operations.

The permissions can be created separately and can be assigned the valid required authorities which satisfies the maximum recursion depth of the blockchain.

And the permissions can be linked to the operations through separate operations which specifies the time validity of the permission over the operation.

Any given permission of an account can be linked to multiple types of operations.

This gives applications flexibility to use any available custom permission of an account and at the same time specify the validity.

####  <a id="5.1-Custom-Permissions"></a>

#### 5.1 Custom Permissions <a id="5.1-Custom-Permissions"></a>

Named permission objects are introduced and users are able to create the objects through new operations introduced.

Each permission has a unique name for any given account.

Code changes represented as pseudo-code,`// Permission Storage Class class custom_permission_object : public abstract_object<custom_permission_object> { public: static const uint8_t space_id = protocol_ids; static const uint8_t type_id = custom_permission_object_type; // Account for which this permission is being created account_id_type account; // Permission name string permission_name; // Authority required for this permission authority auth; } // Custom Permission multi index typedef multi_index_container< custom_permission_object, indexed_by< ordered_unique<tag<by_id>, member<object, object_id_type, &object::id>>, ordered_unique<tag<by_account_and_permission>, composite_key<custom_permission_object, member<custom_permission_object, account_id_type, &custom_permission_object::account>, member<custom_permission_object, string, &custom_permission_object::permission_name> > > > > custom_permission_multi_index_type; // Operations // Create custom permission op struct custom_permission_create_operation : public base_operation { asset fee; account_id_type owner_account; string permission_name; authority auth; } // Update custom permission op struct custom_permission_update_operation : public base_operation { asset fee; custom_permission_id_type permission_id; optional<string> new_permission_name; optional<authority> new_auth; account_id_type payer; } // Delete custom permission op struct custom_permission_delete_operation : public base_operation { asset fee; custom_permission_id_type permission_id; account_id_type payer; } // Evaluators // Create custom permission evaluator class create_custom_permission_evaluator : public evaluator<create_custom_permission_evaluator> { public: typedef custom_permission_create_operation operation_type; void_result do_evaluate(const custom_permission_create_operation& o); object_id_type do_apply(const custom_permission_create_operation& o); }; // Update custom permission evaluator class update_custom_permission_evaluator : public evaluator<update_custom_permission_evaluator> { public: typedef custom_permission_update_operation operation_type; void_result do_evaluate(const custom_permission_update_operation& o); object_id_type do_apply(const custom_permission_update_operation& o); }; // Delete custom permission evaluator class delete_custom_permission_evaluator : public evaluator<delete_custom_permission_evaluator> { public: typedef custom_permission_delete_operation operation_type; void_result do_evaluate(const custom_permission_delete_operation& o); object_id_type do_apply(const custom_permission_delete_operation& o); };`

####  <a id="5.2-Custom-Account-Authorities"></a>

#### 5.2 Custom Account Authorities <a id="5.2-Custom-Account-Authorities"></a>

As mentioned above, the mappings between custom permissions and operation types are stored in the following objects.

Psuedo-code as below,`// Custom account authority Storage classes class custom_account_authority_object : public abstract_object<custom_account_authority_object> { public: static const uint8_t space_id = protocol_ids; static const uint8_t type_id = custom_account_authority_object_type; custom_permission_id_type permission_id; int operation_type; time_point_sec valid_from; time_point_sec valid_to; } // Custom account authority multi index typedef multi_index_container< custom_account_authority_object, indexed_by< ordered_unique<tag<by_id>, member<object, object_id_type, &object::id>>, ordered_unique<tag<by_permission_and_op>, composite_key<custom_account_authority_object, member<custom_account_authority_object, custom_permission_id_type, &custom_account_authority_object::permission_id>, member<custom_account_authority_object, int, &custom_account_authority_object::operation_type>, member<object, object_id_type, &object::id> >>, ordered_unique<tag<by_expiration>, composite_key<custom_account_authority_object, member<custom_account_authority_object, time_point_sec, &custom_account_authority_object::valid_to>, member<object, object_id_type, &object::id> > > > > custom_account_authority_multi_index_type; // Operations // Create custom account authority op struct custom_account_authority_create_operation : public base_operation { asset fee; custom_permission_id_type permission_id; int operation_type; time_point_sec valid_from; time_point_sec valid_to; } // Update custom account authority op struct custom_account_authority_update_operation : public base_operation { asset fee; custom_account_authority_id_type id; optional<custom_permission_id_type> new_permission_id; optional<time_point_sec> new_valid_to; account_id_type payer; } // Delete custom account authority op struct custom_account_authority_delete_operation : public base_operation { asset fee; custom_account_authority_id_type id; account_id_type payer; } // Evaluators // Create custom account authority evaluator class create_custom_account_authority_evaluator : public evaluator<create_custom_account_authority_evaluator> { public: typedef custom_account_authority_create_operation operation_type; void_result do_evaluate(const custom_account_authority_create_operation& o); object_id_type do_apply(const custom_account_authority_create_operation& o); }; // Update custom account authority evaluator class update_custom_account_authority_evaluator : public evaluator<update_custom_account_authority_evaluator> { public: typedef custom_account_authority_update_operation operation_type; void_result do_evaluate(const custom_account_authority_update_operation& o); object_id_type do_apply(const custom_account_authority_update_operation& o); }; // Delete custom account authority evaluator class delete_custom_account_authority_evaluator : public evaluator<delete_custom_account_authority_evaluator> { public: typedef custom_account_authority_delete_operation operation_type; void_result do_evaluate(const custom_account_authority_delete_operation& o); object_id_type do_apply(const custom_account_authority_delete_operation& o); };`

####  <a id="5.3-Transaction-Verification-Changes"></a>

#### 5.3 Transaction Verification Changes <a id="5.3-Transaction-Verification-Changes"></a>

For backward compatibility, the actual active/owner authority of a required account can still successfully sign the transactions.

All the new permissions being created are children of owner/active.

Related critical changes in transaction.cpp,`void chain::verify_authority(...); void chain::signed_transaction::verify_authority(...);`

####  <a id="5.4-Permission-limits-and-validity"></a>

#### 5.4 Permission limits and validity <a id="5.4-Permission-limits-and-validity"></a>

There needs to be a limit on the maximum number of permissions that can be created in an account.

Similarly the limit on the number of operation types that can be linked to an account custom permission.

All the mapping should be deleted from the database after the expiry. \( first block after valid\_to\)

The limits can be introduced in chain\_parameters so that committee can make changes to them from time to time.`// chain_parameters.hpp struct parameter_extension { .... // New changes optional < uint32_t > rbac_max_permissions_per_account = GRAPHENE_MAX_PERMISSIONS_PER_ACCOUNT; optional < uint32_t > rbac_max_account_authority_lifetime = GRAPHENE_MAX_ACCOUNT_AUTHORITY_LIFETIME; optional < uint32_t > rbac_max_authorities_per_permission = GRAPHENE_MAX_AUTHS_PER_PERMISSION; } // config.hpp #define GRAPHENE_MAX_PERMISSIONS_PER_ACCOUNT 5 //5 per account???? #define GRAPHENE_MAX_ACCOUNT_AUTHORITY_LIFETIME 180*24*60*60 //6 months???? #define GRAPHENE_MAX_AUTHS_PER_PERMISSION 5 //5 ????`Be the first to like thisNo labels

