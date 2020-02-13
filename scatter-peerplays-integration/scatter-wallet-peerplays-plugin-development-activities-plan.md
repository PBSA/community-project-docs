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
      <td style="text-align:left">20 Dec 2020</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Define project scope (#3)</li>
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
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/3">#3</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/4">#4</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/5">#5</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ASAP</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />Define MVP for QA</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />Determine how to compile application with PPY plugin operable for MVP</li>
        </ul>
      </td>
      <td style="text-align:left">What QA environment is
        <br />expected? Full binary testing or
        <br />unit test running?</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">07 Feb 2020</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-1-connect-to-peerplays-blockchain">3.1</a>]
            Determine if a JavaScript fetch data layer is feasible</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Key utility functions</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>Connect to Peerplays blockchain:</p>
        <p>We can port all the necessary calls to fetch calls and avoid maintaining
          a constant
          <br />connection to the Peerplays blockchain.</p>
        <p></p>
        <p>Conversion of keys, generation of
          <br />keys, key validation, etc.</p>
        <p>See within Low-Level tasks</p>
      </td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/11">#11 SC-1</a> 
        </p>
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
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-1-connect-to-peerplays-blockchain">3.1</a>]
            Data Layer</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-3-support-for-ppy-asset-retrieve-ppy-balance">3.3</a>]
            Balance(s) retrieval</li>
        </ul>
        <p>[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-4-send-ppy">3.4</a>]
          Transfer Funds</p>
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
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />parse UI numbers to blockchain numbers</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>See Data Layer below</p>
        <p>See within Application Layer below</p>
      </td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/pull/29">#29 SC-16</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/pull/17">#17 SC-2</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/13">#13 SC-5</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/14">#14 SC-3</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">21 Feb 2020</td>
      <td style="text-align:left">
        <p>Functional Requirements</p>
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            /> <del>[</del><a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#2-0-high-level-requirements"><del>2.0</del></a><del>] Connect to Peerplays blockchain</del>
          </li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair">3.2</a>]
            Generate keypair</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-3-support-for-ppy-asset-retrieve-ppy-balance">3.3</a>]
            Support for PPY asset</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-3-support-for-ppy-asset-retrieve-ppy-balance">3.3</a>]
            Retrieve PPY Balance</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#2-0-high-level-requirements">2.0</a>]
            Create a new Peerplays Account (#15)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#2-0-high-level-requirements">2.0</a>]
            Store/Import Keys after creation (#26)</li>
        </ul>
        <p>Other tasks/issues from GitHub.</p>
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Authorize a Peerplays account with username &amp; password (#45 &amp;
            #21)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Remove hardcoded asset info (#19)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />investigate CORS issues (#18)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />incorporate unit tests provided by Scatter Team(#28)</li>
        </ul>
        <p>Required items for a Scatter Plugin</p>
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />Define default blockchain explorer</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />[required functions]</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />tweaks to existing code</li>
        </ul>
        <p></p>
      </td>
      <td style="text-align:left">
        <p>Constant connection via websocket (WS) like our other
          <br />dapps has not been chosen for
          <br />usage in the Peerplays Scatter
          <br />plugin.
          <br />It will instead use a fetch based approach similar to a restful
          <br />server call.</p>
        <p>
          <br />Other functional requirements not listed
          <br />here will be done on another deadline.
          <br />See within Application Layer below</p>
        <p></p>
        <p>See &quot;required functions&quot; within:
          <br />Low-Level
          <br />&gt; Application Layer
          <br />&gt; Required Scatter functions/declarations</p>
        <p></p>
        <p>Tweaks to existing code in lieu of discovery that
          <br />UI that has been used for plugin development is going to be deprecated.
          Tweaks required to ensure plugin will work with new UI (bridge)</p>
      </td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/15">#15 SC-4</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/26">#26 SC-15</a>
        </p>
        <p><a href="https://github.com/peerplays-network/peerplaysjs-lib/issues/45">#45 SC-7</a>
        </p>
        <p><a href="https://github.com/peerplays-network/peerplaysjs-lib/issues/45">#21 SC-14</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/26">#26 SC-15</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/19">#19 SC-10</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/18">#18</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/28">#28 SC-13</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">28 Feb 2020</td>
      <td style="text-align:left">
        <p>Presentation layer work (plugin integration with UI)</p>
        <p></p>
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-3-support-for-ppy-asset-retrieve-ppy-balance">3.3</a>]
            Support for PPY Asset/Retrieve PPY Balance</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-4-send-ppy">3.4</a>]
            Transfer functionality integrated with UI</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#2-0-high-level-requirements">2.0</a>]
            Import Peerplays Account</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#2-0-high-level-requirements">2.0</a>]
            Create Peerplays Account</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>TBD who will be adding forms or tweaking
          <br />anything in the Scatter UI (ScatterDesktop/ScatterBridge) but they
          <br
          />require all Data and Application layer tasks
          <br />to be complete.
          <br /><b>Balance</b>: &quot;Receive PPY&quot; functional
          <br />requirement
          <br /><b>Transfer</b>: &quot;Send PPY&quot; functional
          <br />requirement
          <br /><b>Import</b>: &quot;Import Key&quot; functional requirement
          <br /><b>Create</b>: &quot;Create Peerplays account&quot;
          <br />functional requirement</p>
        <p>See within Presentation Layer below</p>
      </td>
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/16">#16 SC-6</a>
      </td>
    </tr>
  </tbody>
</table>## High-Level

### Data Layer

#### \[[3.1](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-1-connect-to-peerplays-blockchain)\] Minimal fetch.

Only support the required functions. Support JavaScript fetch calls asynchronously.

* [x] New API/RESTFUL-like approach to getting/posting information to/from the blockchain instead of constant WS connection.

### Application Layer

#### \[[3.2](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)\] Register/Create Peerplays Account

Sends register request to chain faucet and then imports/stores \(`import(…)`\) the keys to the Scatter encrypted storage.

* [x] register\(username, password\)

#### \[[3.2](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)\] Authorize/Import Peerplays Account

Store account keys after they have been generated \(and authenticated\) as [multiple KeyPair objects](https://gitter.im/GetScatter-Peerplays-Integration/community?at=5e3e0947340a8019bbabbf5d) attached to a single Scatter identity.

* [ ] import\(\)
* [x] authUser\(username, password\)

#### \[[3.4](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-4-send-ppy)\] Transfer Funds

Requires porting of several functions from peerplaysjs-lib to support fetch calls instead of a constant WS connection route via exclusive usage of TransactionBuilder \(see low-level section below for details\).

* [x] build transfer transaction
* [x] set transaction fees for memo/no memo
* [x] sign a built transfer transaction
* [x] broadcast a signed transfer transaction

#### \[[3.3](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-3-support-for-ppy-asset-retrieve-ppy-balance)\] Retrieve account balance\(s\)

* [x] single asset retrieval
* [x] multiple asset retrieval

### Presentation Layer

#### \[[3.2](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)\] Register/Create Peerplays Account

Requires a form \[added by _TBD_\] that will retrieve a `username` from the end user. The `password` field is generated for them and they just need to verify it by copy and pasting it into another password text field.

* 1 username field
* 1 read-only field \(generated password\)
* 1 password field \(generated password pasted here by end-user\)
* 1 submit/register/create button
* [ ] register form

#### \[[3.2](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)\] Authorize/Import Peerplays Account

Account authorization and key generation involved for Peerplays \(form\) \[added by _TBD_\]

* 1 username field
* 1 password field
* 1 submit/login/import button
* [ ] account import form

#### Plugin Integration

Integration of code functionality from plugin with scatter frontend

* [ ] \[[3.2](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)\] Import Peerplays Account \(authUser function in Peerplays plugin\) \(new/tweak form required\)
* [ ] \[[3.2](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)\] Create Peerplays Account \(register function in Peerplays plugin\) \(new/tweak form required\)
* [x] \[[3.3](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-3-support-for-ppy-asset-retrieve-ppy-balance)\] Support for PPY Asset/Retrieve PPY Balance
* [ ] \[[3.4](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-4-send-ppy)\] Transfer functionality integrated with UI
* [ ] \[[3.5](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-5-receive-ppy)\] Receive PPY

## Low-Level 

### Application Layer

{% hint style="warning" %}
All functionality defined in this section are verified as "working" via unit tests as we have no working binary production method yet. \(presentation layer work may result in changes to one or more of these functionalities\)
{% endhint %}

#### Test Suite

Configuration of test-suite to support mainnet and testnet testing accounts

* [x] multi-chain/account supported test suite

#### \[[3.1](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-1-connect-to-peerplays-blockchain)\] API/RESTFUL-like function to make fetch calls to the blockchain instead of using constant WS connection

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
* [ ] tweaks to existing code in lieu of to-be-deprecated Scatter UI in favor of new Scatter UI \(bridge\)

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

**\[**[**3.2**](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-1-connect-to-peerplays-blockchain)**\] New account registration**

Request `username` and `password` from user. Check that `username` has not already been claimed via `getFullAccount()`. Send register request to chain faucet if form data is valid \(`register()`\).

* [x] getFullAccount
* [x] register

**\[**[**3.4**](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-1-connect-to-peerplays-blockchain)**\] Transfer of funds with memo support \(required function: `transfer`\)**

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

**\[**[**3.2**](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)**\] Key Generation/Conversion**

* [x] privateFromWif → convert the PrivateKey class instantiated object from the Wallet Import Format \(WIF\) key
* [x] wifFromPrivate → convert the PrivateKey class instantiated object into the Wallet Import Format \(WIF\) key
* [x] privateToPublic → convert the Wallet Import Format \(WIF\) key into its public key

**\[**[**3.2**](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)**\] Peerplays Account Authorization**

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

#### **\[**[**3.2**](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)**\] Create Peerplays Account**

* [ ] "Generate Keypair" via `username`, `generated_password` , and `password_confirm` fields that ultimately register a new account and store the keys for this new account \(once created\) within Scatter
* [ ] modify functions \(`register`\) to return expected data for UI

#### **\[**[**3.2**](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)**\] Import Peerplays Account**

* [ ] "Import Key" via Peerplays' familiar username and password login: `username` and `password` form which will authorize `username` if keys generated from form data are authentic
* [ ] modify functions to return expected data for UI

#### **\[**[**3.3**](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-3-support-for-ppy-asset-retrieve-ppy-balance)**\] Support for PPY Asset/Retrieve PPY Balance**

* [ ] Displays PPY account Balance

#### \[[3.4](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-4-send-ppy)\] Transfer & Sign

Modify to return a promise `resolve` or `reject`. The `resolve` must return a transaction ID.

* [ ] determine what the transaction ID represents \(block number?\)
* [x] modify return value to be compatible with UI

#### \[[3.5](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-5-receive-ppy)\] Receive PPY

* [ ] Displays Peerplays username to give others



