# SON Requirements Specification

##  <a id="title-text"></a>

|  |  |
| :--- | :--- |
| Target Audience | Developers, QA |
| Epic |  [![](https://peerplays.atlassian.net/images/icons/issuetypes/epic.svg)SON-89](https://peerplays.atlassian.net/browse/SON-89) - LLDs - design and review Done |
| Document status | FINAL [![](https://peerplays.atlassian.net/secure/viewavatar?size=medium&avatarId=10318&avatarType=issuetype)SON-86](https://peerplays.atlassian.net/browse/SON-86) - review SON configuration LLD Done |
| Document owner | [Bobinson Bobby](https://peerplays.atlassian.net/wiki/people/5c59e1ed2149cc4fbc9ff5b2?ref=confluence)  |
| Tech lead |  |
| Architect | [Bobinson Bobby](https://peerplays.atlassian.net/wiki/people/5c59e1ed2149cc4fbc9ff5b2?ref=confluence) |
| QA | [Alick Feldman](https://peerplays.atlassian.net/wiki/people/5c5dd7500dc20b5befa2af6b?ref=confluence) |
| Document Call Sign | SON-req |

### Purpose <a id="SONConfiguration-Purpose"></a>

The purpose of this document is to provide the design for the SON configuration.

### 1. OBJECTIVE <a id="SONRequirementsSpecification-1.OBJECTIVE"></a>

Provide requirements for Sidechain Operating Nodes \(SON\). PIP \(Peerplays Improvement Proposal\) for the same is here : [https://github.com/peerplays-network/pips/blob/master/pip-0005.md](https://github.com/peerplays-network/pips/blob/master/pip-0005.md)

* Provide bi-directional exchange of value \(tokens/coins\) between multiple chains and Peerplays
* Let Peerplays based game developer

### 2. Assumptions <a id="SONRequirementsSpecification-2.Assumptions"></a>

* Peerplays blockchain will be upgraded to support Ubuntu 18.04
* GPoS will be merged and available 
* GCC 5.5 and G++ 5.5, BOOST 1.67.0, Peerplays-FC with default versions of build tools like cmake available on Ubuntu 18.04 will be used for the development.
* A specific version / branch of the Peerplays blockchain will be provided by PBSA where all the unit test cases are running successfully
* Voting UI will be made available 

### INTRODUCTION <a id="SONRequirementsSpecification-INTRODUCTION"></a>

In order to facilitate the transfer of token operations from the Peerplays blockchain to and from another blockchain Side Chain Operating nodes aka SONs is proposed. This mechanism will tie directly into GPOS in order to accomplish a full inter-blockchain communication mechanism. The scope of SONs is limited to transfer of value and not state across chains. The transfer of value will be bi-directional.

The core Peerplays blockchain will support SONs by having the witnesses run SON receiver logic. The core of Peerplays blockchain will not undergo any further changes to support various external chains like EOS, Bitcoin and Etherium. ie interface changes for support of new chains will happen at the SONs relay - transmitting logic and not at the Peerplays witness. 

SONs will be elected through a voting mechanism making use of GPoS. A user interface allowing users to vote for SONs has to be created. This can be also incorporated to the wallet.

### SON AS A PLUGIN <a id="SONRequirementsSpecification-SONASAPLUGIN"></a>

A Peerplays node, can enable or disable SON via the configuration file and restarting the node. When a node which wants to be an SON enables the SON plugin, it should be automatically registered in the Peerplays blockchain as an SON enabled node. Disabling or enabling the plugin should not impact replaying the node. A SON becomes active participant based on the votes it receives. That is to say if a node just activates the plugin and is not receiving any votes, it will not be able to operate as a SON.

The SON plugin must have a mechanism to submit transactions it receives from side chains.

The SON plugin should enable API and programatic interface which will help dApps or scripts to send transaction details from other chains to SONs. We must expose a generic interface which can be further extended for various blockchains. SONs must publish an API so that RPC requests for EOS, bitcoin & other chain related transactions to them. \(Refer BTC Relay & PeaceRelay\)

_**Transactions from Sidechain &gt; SON Transaction Receiver &gt; Processing and Signing of the Transaction by 2/3rd of the SONs &gt; SON Transaction Submitter &gt; Peerplays**_

As described above the SON must expose a generic transaction receiver with support for EOS, Bitshares, Bitcoin and Etherium. A generic definition of the interface should be provided as part of the High Level Design. The generic interface should be capable of extending to support more chains in the future.

Enabling the SON plugin will not have any impact on a Peerplays witness node unless the node is also elected as a SON. The primary difference between the earlier Bitcoin sidechain implementation and SON is that no additional components from other chains will have to be operated by the SON nodes. This will ensure a lean system as opposed to the Peerplays nodes running various blockchains like Bitcoin and Etherium Virtual Machines. This means no smart contracts written for say EVM will be executed in any of the Peerplays nodes irrespective whether they are witnesses, seed nodes or SONs.

### VOTING <a id="SONRequirementsSpecification-VOTING"></a>

SONs will be elected using GPOS voting. The SONs will change depending on criteria like the votes received, taken out of circulation due to down time, planned maintenance etc. A minimum of 5 SONs should be available at any point in time for the SONs to be operational. The requirement of minimum 15 is needed to provide resilience. Transaction approval will require a minimum of 2/3rd approvals in any case.

As an SON enabled node, if my downtime exceeds 12 continuous hours, I should be automatically deregistered in the Peerplays blockchain as an SON enabled node and all the votes casted for me should be reverted. \(Applicable only for unplanned downtime\)

### FEES <a id="SONRequirementsSpecification-FEES"></a>

A daily rewards pool will be established for SONs that will be paid out daily based on transactions signed and weight of voting. Both approved and rejected transactions shall be included as part of the total transaction count. Recommended starting balance should be 200 PPY daily.

A SON, will be paid for providing my services through the blockchain & in PPY. The payments will be dispersed after each Maintenance cycle. All the transaction fee deducted from the bitcoin transactions for SONs should be deposited in a separate account just like the dividend-distribution-account.

### KEY MANAGEMENT <a id="SONRequirementsSpecification-KEYMANAGEMENT"></a>

To create a multisig address on Bitcoin, the signatures of all the SONs are required. The signatures of the top 2/3rd SONs in-erms of votes would be used while creating the Multisig account on the bitcoin blockchain. The top 2/3rd selection is thus an important end user controlled activity in the chain.  
  
When a SON needs to perform maintenance, it will disable the node which will first rotate the keys used for the multi-signature wallet. This operation has to be detailed in the system architecture and design documents.  
  


In the event of a SON part of the key management goes down abruptly, the funds under maintenance will be stuck until the SON comes back. 

All bitcoin transactions in Peerplays blockchain get validated to ensure they are originated form the SONs only. Add validations on the Peerplays blockchain to check that the bitcoin transactions originated from the SONs only. 

As soon as there is a change in the SON, his private key on the bitcoin address should be replaced by the private key of a new incoming SON OR we can simply delete the private key from the outgoing SON's account and add it to the new SON's account. 

**TODO**: explore HTLC

### TRANSACTION SIGNING & CONSENSUS <a id="SONRequirementsSpecification-TRANSACTIONSIGNING&amp;CONSENSUS"></a>

As captured early, we would need 15 SONs for the normal operation of the SON network. If the number of nodes goes below this number SONs should stop accepting new transactions. However if there are already existing mult-signature wallets & pegged assets or tokens issues in the Peerplays network those operation should continue. Any Transaction submitted by the SONs on the Peerplays blockchain should be signed by at least half + 1 SONs. This would ensure that a single SON cannot submit a malicious transaction on the blockchain.

SONs should create a distributed event bus sort of mechanism which should receive transaction details. If a SON receives the request for a transaction via an API, it must publish it to the event bus which the other SONs can read and process. This should be using a publisher - subscriber mechanism. If at any point in time a SON finds that a particular transaction is signed by 2/3rd of the SONs, that SON will post the transaction to the Peerplays blockchain. This will ensure that the Peerplays blockchain receives only those transactions which are signed by 2/3rd of the SONs. Upon receiving the transaction from the event bus, the SON will verify the transaction details with the appropriate blockchain & if the data on the source blockchain \(sidechain\) seems to be intact, the SON will sign the transaction and publish it back to the event bus. Any transaction signed by 2/3rd of the SONs will be marked dirty and will be taken out of the event bus. For the event bus, a ring buffer design pattern can be implemented. \(refer: LMAX disruptor\)

This will prevent any SON from creating a malicious transaction by running a malicious bitcoin node.

### VESTING REQUIREMENTS <a id="SONRequirementsSpecification-VESTINGREQUIREMENTS"></a>

Nodes interested in becoming SONs must vest 50 amount of PPY. The PPY vested by SONs can't be claimed till 2 days after they have deregistered their SON node.

### PERFORMANCE REQUIREMENTS FOR SONS <a id="SONRequirementsSpecification-PERFORMANCEREQUIREMENTSFORSONS"></a>

The performance of the SONs should be determined by their uptime as well as the errors that they make. Uptime & missed blocks or similar errors should be tracked and presented to the voters providing historical performance data to the voters.

Witnesses should have the power to freeze SON's account or blacklist SON. If an error on the part of an SON is not verifiable with a fork of the bitcoin blockchain then the witnesses should have the power to freeze his account or blacklist him.

### ACCEPTANCE CRITERIA <a id="SONRequirementsSpecification-ACCEPTANCECRITERIA"></a>

* performance: TPS, computational resource KPI must be defined
* security audits: The ring buffer can be bombarded with event submissions. This must be carefully evaluated.
* For each blockchain SONs are going to support, separate KPI \(key performance indicators should be defined\)
* code peer review

###  User interaction and design <a id="SONRequirementsSpecification-Userinteractionanddesign"></a>

The end users are the Peerplays holders. They will be able to vote and select SONs. We need to prove a UI for the end users to engage in voting.

### Open Questions <a id="SONRequirementsSpecification-OpenQuestions"></a>

|  |
| :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left">How to address when a SON goes down abruptly and never comes back ?</th>
      <th
      style="text-align:left"></th>
        <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">What is the maximum allowed time for a SON to undergo maintenance ?</td>
      <td
      style="text-align:left">12 hours &amp; after this the SON will be banned</td>
        <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">What are the steps to announce maintenance ?</td>
      <td style="text-align:left">
        <p>An explicit maintenance announcement command should be provided. This
          will trigger</p>
        <p>rearrangement of multi-signature keys.</p>
      </td>
      <td style="text-align:left"></td>
    </tr>
  </tbody>
</table>

### Out of Scope <a id="SONRequirementsSpecification-OutofScope"></a>

TBD

