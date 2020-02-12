---
description: 'DOCUMENT STATUS: DRAFT'
---

# Scatter Wallet Peerplays Plugin Development Activities Plan

{% hint style="warning" %}
**For all tasks, appropriate unit-tests must be provided \(smoke/positive tests\).  
All tasks/issues status' can be viewed on the GitHub project** [**here**](https://github.com/orgs/peerplays-network/projects/1)**.**
{% endhint %}

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Date</b>
      </th>
      <th style="text-align:left"><b>Dev Activities</b>
      </th>
      <th style="text-align:left"><b>Remarks</b>
      </th>
      <th style="text-align:left"><b>GitHub Issue(s)</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">todo: check date was completed</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Define functional requirements (#4)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Define acceptance criteria (#5)</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/4">#4</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/5">#5</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">07 Feb 2020</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Determine if a JavaScript fetch data layer is feasible</li>
        </ul>
      </td>
      <td style="text-align:left">We can port all the necessary calls to fetch calls and avoid maintaining
        a constant connection to the Peerplays blockchain.</td>
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/11">#11 SC-1</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">07 Feb 2020</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Key utility functions</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>Conversion of keys, generation of keys, key validation, etc.</p>
        <p>See within Low-Level tasks.</p>
      </td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/24">#24 SC-12</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/25">#25 SC-11</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">14 Feb 2020</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Data Layer</li>
        </ul>
      </td>
      <td style="text-align:left">See Data Layer below</td>
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/pull/29">#29 SC-16</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">14 Feb 2020</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Balance(s) retrieval</li>
        </ul>
      </td>
      <td style="text-align:left">See within Application Layer below</td>
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/pull/17">#17 SC-2</a>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">14 Feb 2020</td>
      <td style="text-align:left">
        <p>Transfer Funds</p>
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />build transaction (#13 &amp; #15)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />set transaction fees (#13 &amp; #14)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />sign transaction (#13 &amp; #14)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />broadcast transaction (#13 &amp; #14)</li>
        </ul>
      </td>
      <td style="text-align:left">See within Application Layer below</td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/13">#13 SC-5</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/14">#14 SC-3</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">21 Feb 2020</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Create a new Peerplays Account (#15)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />Store/Import Keys after creation (#26)</li>
        </ul>
      </td>
      <td style="text-align:left">See within Application Layer below</td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/15">#15 SC-4</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/26">#26 SC-15</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">21 Feb 2020</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Authorize a Peerplays account with a standard login form (#45 &amp; #21)</li>
          <li
          class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />Store/Import keys after authorizing user (#26)</li>
        </ul>
      </td>
      <td style="text-align:left">See within Application Layer below</td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/peerplaysjs-lib/issues/45">#45 SC-7</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/21">#21 SC-14</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/26">#26 SC-15</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">21 Feb 2020</td>
      <td style="text-align:left">
        <p><b>FILL ME IN</b>
        </p>
        <p>Other tasks/issues from GitHub.</p>
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Remove hardcoded asset info (#19)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Investigate CORS issues (#18)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Incorporate unit tests provided by Scatter Team (#28)</li>
        </ul>
      </td>
      <td style="text-align:left">Miscellaneous tasks/issues that come up during development.</td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/19">#19 SC-10</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/18">#18</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/28">#28 SC-13</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">21 Feb 2020</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />Presentation layer work (plugin integration with UI)</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>TBD who will be adding forms or tweaking anything in the Scatter UI (ScatterDesktop/ScatterBridge)
          but they require all Data and Application layer tasks to be complete.</p>
        <p>See within Presentation Layer below</p>
      </td>
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/16">#16 SC-6</a>
      </td>
    </tr>
  </tbody>
</table>## High-Level

### Data Layer

Minimal. Only support the required functions. Support JavaScript fetch calls asynchronously.

* [x] New API/RESTFUL-like approach to getting/posting information to/from the blockchain instead of constant WS connection.

### Application Layer

#### Register/Create Peerplays Account

Sends register request to chain faucet and then imports/stores \(`import(…)`\) the keys to the Scatter encrypted storage.

* [x] register\(username, password\)

#### Authorize/Import Peerplays Account

Store account keys after they have been generated \(and authenticated\) as [multiple KeyPair objects](https://gitter.im/GetScatter-Peerplays-Integration/community?at=5e3e0947340a8019bbabbf5d) attached to a single Scatter identity.

* [ ] import\(\)
* [x] authUser\(username, password\)

#### Transfer Funds

Requires porting of several functions from peerplaysjs-lib to support fetch calls instead of a constant WS connection route via exclusive usage of TransactionBuilder \(see low-level section below for details\).

* [x] build transfer transaction
* [x] set transaction fees for memo/no memo
* [x] sign a built transfer transaction
* [x] broadcast a signed transfer transaction

#### Retrieve account balance\(s\)

* [x] single asset retrieval
* [x] multiple asset retrieval

### Presentation Layer

#### Register/Create Peerplays Account

Requires a form \[added by _TBD_\] that will retrieve a `username` from the end user. The `password` field is generated for them and they just need to verify it by copy and pasting it into another password text field.

* 1 username field
* 1 read-only field \(generated password\)
* 1 password field \(generated password pasted here by end-user\)
* 1 submit/register/create button
* [ ] register form

#### Authorize/Import Peerplays Account

Account authorization and key generation involved for Peerplays \(form\) \[added by _TBD_\]

* 1 username field
* 1 password field
* 1 submit/login/import button
* [ ] account import form

#### Plugin Integration

This task likely won’t be done by Peerplays but rather, by Nathan/Scatter team

Integration of code functionality from plugin with scatter frontend

* [ ] Transfer functionality integrated with UI
* [ ] Import Peerplays Account \(authUser function in Peerplays plugin\)
* [ ] Create Peerplays Account \(register function in Peerplays plugin\) 

## Low-Level 

### Application Layer

{% hint style="warning" %}
All functionality defined in this section are verified as "working" via unit tests as we have no working binary production method yet. \(presentation layer work may result in changes to one or more of these functionalities\)
{% endhint %}

#### Test Suite

Configuration of test-suite to support mainnet and testnet testing accounts

* [x] multi-chain/account supported test suite

#### API/RESTFUL-like function to make fetch calls to the blockchain instead of using constant WS connection

`database` API calls:

* [x] get\_required\_fees → determine what fees are necessary for the operation \(if we don't add anything or the wrong fees, the transaction will be rejected by the blockchain\)
* [x] get\_objects → retrieve object data from chain via its ID
* [x] get\_full\_accounts → get full account data object from chain by ID/username
* [x] lookup\_asset\_symbols → get the symbols associated with an asset ID ie: `1.3.0` = `PPY`
* [x] get\_chain\_id → retrieves the identifier code for the chain from the blockchain

`network_broadcast` API calls:

* [x] broadcast\_transaction\_with\_callback

#### Required Scatter functions/declarations

Re-create the base/required functions by any Scatter plugin

* [ ] Define default blockchain explorer

{% hint style="danger" %}
These functions are tested via a unit test suite provided by Nathan. This does not mean that these functionalities will work with the various UI repositories.
{% endhint %}

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />constructor</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />bip</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />bustCache</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />defaultExplorer</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />accountFormatter</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />returnableAccount</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />contractPlaceholder</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />checkNetwork</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />getEndorsedNetwork</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />isEndorsedNetwork</li>
        </ul>
      </th>
      <th style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />getChainIdusesResources</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />hasAccountActions</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />accountsAreImported</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />isValidRecipient</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />privateFromWif</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />privateToPublic</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />validPrivateKey</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />validPublicKey</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />bufferToHexPrivate</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />hexPrivateToBuffer</li>
        </ul>
      </th>
      <th style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />hasUntouchableTokens</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />defaultDecimals</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />defaultToken</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />actionParticipants</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />balancesFor</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />balanceFor</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />signerWithPopup</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />requestParser</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />transfer</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />signer</li>
        </ul>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>#### Port from `peerplays-core-gui` and/or `peerplaysjs-lib`

**New account registration**

Request `username` and `password` from user. Check that `username` has not already been claimed via `getFullAccount()`. Send register request to chain faucet if form data is valid \(`register()`\).

* [x] getFullAccount
* [x] register

**Transfer of funds with memo support \(required function: `transfer`\)**

* [x] getTransferTransaction → build the transaction with memo support → other required functions: `getAsset`, `getFees`, `getRequiredFees`, `setRequiredFees`
* [x] signer → part one of two for signing a transaction, this adds the keys required to the peerplays transaction object to allow us to later sign the transaction
* [x] finalize → if further processing is required on the transaction before signing, it's done in this method
* [x] sign → takes the keys added to the transaction object in `signer` and signs the transaction with them
* [x] broadcast → once the transaction is ready, send it to the blockchain to be processed
* [x] getAsset → get asset information from chain
* [x] getFees → get fees required for operation \(some fee schedule items have a price/KB as well as a flat fee\)
* [x] getRequiredFees → determine what fees are necessary for the operation \(if we don't add anything or the wrong fees, the transaction will be rejected by the blockchain\)
* [x] setRequiredFees → once the required fees are determined, set them on the transaction object

**Generic Object Data Retrieval**

* [x] getObjects

**Key Generation/Conversion**

* [x] privateFromWif → convert the PrivateKey class instantiated object from the Wallet Import Format \(WIF\) key
* [x] wifFromPrivate → convert the PrivateKey class instantiated object into the Wallet Import Format \(WIF\) key
* [x] privateToPublic → convert the Wallet Import Format \(WIF\) key into its public key

**Peerplays Account Authorization**

Peerplays account authentication \(logging in\) is done by:

1. requesting a `username` & `password` from the user
2. using the peerplaysjs-lib key generator, generate keys from the input provided in step 1
3. request the public keys from the blockchain for `username` retrieved in step 1
4. compare the active public key generated in step 2 with the active public key retrieved in step 3. One of two must match to consider a user "logged in" or "authenticated":

   * active public key generated must match the chain retrieved active public key
   * owner public key generated must match the chain retrieved active public key

   \[In the past, some accounts were registered with their owner & active keys swapped\]

* [x] getAccountKeys → will retrieve an accounts public keys \(owner, active, memo\) from the blockchain
* [x] authUser

### Presentation Layer

{% hint style="info" %}
Many functions from Low-level Application Layer may require changes to account for specific formats of returned data for UI repositories making use of the Peerplays Scatter Plugin.
{% endhint %}

#### Transfer & Sign

Modify to return a promise `resolve` or `reject`. The `resolve` must return a transaction ID.

* [ ] determine what the transaction ID represents \(block number?\)
* [x] modify return value to be compatible with UI



