# Scatter Wallet Peerplays Plugin Development Activities Plan

{% hint style="warning" %}
**For all tasks, appropriate unit-tests must be provided \(smoke/positive tests\).  
All tasks/issues status' can be viewed on the GitHub project** [**here**](https://github.com/orgs/peerplays-network/projects/1)**.**
{% endhint %}

{% hint style="info" %}
#### GitHub Issues & Card

`#`: The \# symbol denotes a GitHub issue.  
`c.`: "c." denotes a GitHub project board note card.
{% endhint %}

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Due Date</b>
      </th>
      <th style="text-align:left"><b>Dev Activities</b>
      </th>
      <th style="text-align:left"><b>Remarks</b>
      </th>
      <th style="text-align:left"><b>GitHub Issues/Cards</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/milestone/1">20 Dec 2020</a> 
      </td>
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
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/milestone/2">07 Feb 2020</a>
      </td>
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
          a constant connection to the Peerplays blockchain.</p>
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
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/milestone/3">14 Feb 2020</a>
      </td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-1-connect-to-peerplays-blockchain">3.1</a>]
            Data Layer</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-5-support-for-ppy-asset-retrieve-ppy-balance">3.5</a>]
            Balance(s) retrieval</li>
        </ul>
        <p>[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-6-send-ppy">3.6</a>]
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
            />parse UI numbers to blockchain numbers (#36)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M0-UwMJVMl0F_WONrnb/v/master/scatter-peerplays-integration/scatter-wallet-peerplays-plugin-development-activities-plan">3.2</a>]
            Handling multiple Peerplays keys within
            <br />a single Scatter KeyPair
            <br />(#38)</li>
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
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/36">#36</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/pull/38">#38</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/milestone/4">21 Feb 2020</a> 
      </td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            /> <del>[</del><a href="https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#2-0-high-level-requirements"><del>2.0</del></a><del>] Connect to Peerplays blockchain</del>
          </li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-5-support-for-ppy-asset-retrieve-ppy-balance">3.5</a>]
            Support for PPY asset</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-5-support-for-ppy-asset-retrieve-ppy-balance">3.5</a>]
            Retrieve PPY Balance</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-3-create-peerplays-account">3.3</a>]
            Create a new Peerplays Account (#15)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys">3.4</a>]
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
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Define default blockchain explorer</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[required functions]</li>
        </ul>
        <p>Documentation/QA</p>
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Define <a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/qa-mvp-and-environment">MVP/requirements</a> for
            Quality Assurance (#41)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Design mockups and associated documentation for new required forms (#43)</li>
          <li
          class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Spike Integration of ScatterDesktop (#46)</li>
            <li class="task-list-item">
              <input type="checkbox" class="task-list-item-checkbox" disabled />Get QA Environment Configured (#40)</li>
        </ul>
        <p></p>
      </td>
      <td style="text-align:left">
        <p>Constant connection via websocket (WS) like our other dapps has not been
          chosen for usage in the Peerplays Scatter plugin.
          <br />It will instead use a fetch based approach similar to a restful server
          call.</p>
        <p>
          <br />Other functional requirements not listed here will be done on another
          deadline.
          <br />See within Application Layer below</p>
        <p></p>
        <p>See &quot;required functions&quot; within:
          <br />Low-Level
          <br />&gt; Application Layer
          <br />&gt; Required Scatter functions/declarations</p>
        <p></p>
        <p>Documentation: Define any requirements for QA activities to be possible.</p>
        <p></p>
        <p>See Spike within:</p>
        <p>High-level</p>
        <p>&gt; Application Layer</p>
        <p></p>
        <p>QA Environment required Electron executable compilation which will take
          more time.</p>
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
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/19">#19 SC-10</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/18">#18</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/28">#28 SC-13</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/41">#41</a>
        </p>
        <p>&lt;del&gt;&lt;/del&gt;<a href="https://github.com/peerplays-network/getscatter-walletpack/issues/40"><del>#40</del></a>&lt;del&gt;&lt;/del&gt;</p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/43">#43</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/46">#46</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/milestone/5">28 Feb 2020</a>
      </td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Retrieve keys from Scatter storage (#44)</li>
        </ul>
        <p>Presentation layer work (<b>plugin integration with UI</b>)</p>
        <p>Integrate with ScatterBridge (#34)</p>
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-5-support-for-ppy-asset-retrieve-ppy-balance">3.5</a>]
            Support for PPY Asset/Retrieve PPY Balance</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-6-send-ppy">3.6</a>]
            Transfer functionality integrated with UI
            <br />- debug sign/transfer within ScatterBridge (#35)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-7-receive-ppy">3.7</a>]
            Receive PPY (show username)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys">3.4</a>]
            Import Peerplays Account (#16) [form]</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />[<a href="https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-3-create-peerplays-account">3.3</a>]</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>The Peerplays team will be
          <br />making modifications to their fork of the Scatter Bridge repository. These
          modifications will encompass the two new forms required for Peerplays users
          to be able to &quot;import&quot;
          <br />their accounts and/or create a new Peerplays account that is then imported
          into Scatter.
          <br /><b>Balance</b>: &quot;Receive PPY&quot; functional
          <br />requirement
          <br /><b>Transfer</b>: &quot;Send PPY&quot; functional
          <br />requirement
          <br /><b>Import</b>: &quot;Import Key&quot; functional requirement
          <br /><b>Receive</b>: &quot;Receive PPY&quot; functional requirement
          <br /><b>Create</b>: &quot;Create Peerplays account&quot;
          <br />functional requirement</p>
        <p>See within Presentation Layer below</p>
      </td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/16">#16 SC-6</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/34">#34</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/35">#35</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/39">#39</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/44">#44</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://github.com/peerplays-network/getscatter-walletpack/milestone/5">06 March 2020</a>
      </td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Debug sig/transfer within ScatterBridge (#35)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Retrieve keys from Scatter Storage (#44)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Integrate with ScatterBridge (new) UI (#34)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Fix unit tests (CI/CD Failing) (#50)</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/35">#35</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/44">#44</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/34">#34</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/50">#50</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">20 March 2020</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" checked disabled
            />Update documentation for QA (c.1)</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />Scatter Desktop integration (production client encryption) (c.2)</li>
          <li
          class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />Add PPY icon to Scatter Bridge UI (#57)</li>
            <li class="task-list-item">
              <input type="checkbox" class="task-list-item-checkbox" disabled />Update Unit Tests (#58)</li>
            <li class="task-list-item">
              <input type="checkbox" class="task-list-item-checkbox" disabled />Update CD to account for Scatter Desktop integration(#40)</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>Scatter Desktop is indeed required to properly emulate the Peerplays plugin
          within a production environment. <del>Currently, the plugin is not compatible with Desktop so this is a high priority dev. task.</del>
        </p>
        <p>Meeting with Nathan shed light on long-withstanding issues with Desktop
          codebase, have since been resolved and remaining dev activities can be
          completed.</p>
        <p><b>PPY Icon</b>
        </p>
        <ul>
          <li>refer to icomoon and modify existing icomoon lib to include PPY icon</li>
          <li>other code modifications will be required to complete icon</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p><a href="https://github.com/orgs/peerplays-network/projects/1#card-33953859">c.1</a>
        </p>
        <p><a href="https://github.com/orgs/peerplays-network/projects/1#card-34148518">c.2</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/57">#57</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/58">#58</a>
        </p>
        <p><a href="https://github.com/peerplays-network/getscatter-walletpack/issues/40">#40</a>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">TBD</td>
      <td style="text-align:left">
        <p>Complete in order listed:</p>
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />alias imports (<code>import thing as t</code>) not supported by Scatter
            compilation, refactor to not require them</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />Refactor transfer function to use signerWithPopup</li>
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />verify transfer functions as expected with memo&apos;s provided</li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>signerWithPopup function should be called</p>
        <ul>
          <li>refer to gitter comments for more details on relevant changes required
            for this refactor: <a href="https://gitter.im/GetScatter-Peerplays-Integration/community?at=5e7b89b1e822ec79eb85b7ca">https://gitter.im/GetScatter-Peerplays-Integration/community?at=5e7b89b1e822ec79eb85b7ca</a>
          </li>
        </ul>
        <p>Verify transfer</p>
        <ul>
          <li>verified a transfer function during call with nathan but not verified
            it works with memos</li>
        </ul>
        <p>Alias import syntax within the walletpack plugin files need to be refactored/removed,
          once compiled they lose the references they are meant to alias</p>
      </td>
      <td style="text-align:left">TBD</td>
    </tr>
    <tr>
      <td style="text-align:left">TBD</td>
      <td style="text-align:left">
        <ul class="contains-task-list">
          <li class="task-list-item">
            <input type="checkbox" class="task-list-item-checkbox" disabled />Update walletpack, bridge, and desktop codebase with official repositories</li>
        </ul>
      </td>
      <td style="text-align:left">Ensure our code is up-to-date with the official codebase and verify any
        updates that may exist have not broken any plugin/ui functionality</td>
      <td
      style="text-align:left">TBD</td>
    </tr>
  </tbody>
</table>

## High-Level

### Data Layer

#### \[[3.1](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-1-connect-to-peerplays-blockchain)\] Minimal fetch.

Only support the required functions. Support JavaScript fetch calls asynchronously.

* [x] New API/RESTFUL-like approach to getting/posting information to/from the blockchain instead of constant WS connection.

### Application Layer

#### \[[3.2](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-2-generate-keypair)\] Generate/Store Keypair

Generate Scatter Keypair to associate with a Peerplays account and store it.

* [x] storeKeys\(\)

#### \[[3.3](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-3-create-peerplays-account)\] Register/Create Peerplays Account

Sends register request to chain faucet and then imports/stores \(`import(…)`\) the keys to the Scatter encrypted storage.

* [x] register\(username, password\)

#### \[[3.4](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys)\] Authorize/Import Peerplays Account

Store account keys after they have been generated \(and authenticated\) as a single KeyPair attached to a single Scatter identity. ScatterBridge does not support multiple Keypairs per key so we have opted to encrypt the three Peerplays authority keys into a single new "master" key that is decrypted with the Peerplays accounts owner public key within Scatter.

* [x] storeKeys\(\)
* [x] authUser\(username, password\)

#### \[[3.5](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-5-support-for-ppy-asset-retrieve-ppy-balance)\] Retrieve account balance\(s\)

* [x] single asset retrieval
* [x] multiple asset retrieval

#### \[[3.6](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-6-send-ppy)\] Transfer Funds

Requires porting of several functions from peerplaysjs-lib to support fetch calls instead of a constant WS connection route via exclusive usage of TransactionBuilder \(see low-level section below for details\).

* [x] build transfer transaction
* [x] set transaction fees for memo/no memo
* [x] sign a built transfer transaction
* [x] broadcast a signed transfer transaction

#### Spike Integration of ScatterDesktop

Discern how much effort is required to incorporate ScatterDesktop into our QA environment. This is not a mandatory step but would be beneficial knowledge for future development and understanding  
of how Scatter works as a whole.  
If the spike results show that there is not a lot of work involved \(won't effect next milestone completion date\), ScatterDesktop will be added to the QA Environment.

### Presentation Layer

#### \[[3.3](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-3-create-peerplays-account)\] Register/Create Peerplays Account

Refer to Functional Requirements.

* [x] [register form](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-3-create-peerplays-account)

#### \[[3.4](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys)\] Authorize/Import Peerplays Account

Refer to Functional Requirements.

* [x] [account import form](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys)

#### Plugin Integration

Integration of code functionality from plugin with scatter frontend

* [x] \[[3.3](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys)\] Create Peerplays Account \(register function in Peerplays plugin\) \(new/tweak form required\)
* [x] \[[3.4](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys)\] Import Peerplays Account \(authUser function in Peerplays plugin\) \(new/tweak form required\)
* [x] \[[3.5](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-5-support-for-ppy-asset-retrieve-ppy-balance)\] Support for PPY Asset/Retrieve PPY Balance
* [x] \[[3.6](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-6-send-ppy)\] Transfer functionality integrated with UI
* [x] \[[3.7](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-7-receive-ppy)\] Receive PPY \(show account username\)

### Quality Assurance

Quality Assurance \(QA\) will not be possible until there is presentation layer work complete. The resource from the Scatter team has instructed that so long as our unit tests are passing, the plugin should operate fine. However, for QA efforts to be possible, we will be required to make the GUI changes ourselves \(2 additional forms\) and discover a method of reliably viewing the Scatter application.

Recent communications have revealed that ScatterEmbed will soon be reaching the end of its official life in favour of a new Scatter UI called ScatterBridge. This will put some delays on QA deliveries while we learn this new UI and how it uses the other Scatter repositories to breath life into a Scatter blockchain plugin. Some tasks associated with this:

* [x] Define [MVP/requirements](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/qa-mvp-and-environment) for Quality Assurance
* [ ] Get QA Environment Configured

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

* [x] Define default blockchain explorer

  ```javascript
  const EXPLORER = {
    name: 'PeerplaysBlockchain',
    account: 'https://peerplaysblockchain.info/account/{x}',
    transaction: 'https://peerplaysblockchain.info/explorer/transactions/{x}',
    block: 'https://peerplaysblockchain.info/block/{x}',
  };
  ```

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
</table>

#### Port from `peerplays-core-gui` and/or `peerplaysjs-lib`

**\[**[**3.2**](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-1-connect-to-peerplays-blockchain)**\] Handling multiple Peerplays keys within a single Scatter KeyPair**

* [x] crypto functions \(encrypt/decrypt\)
* [x] keypair helper class \(returns Scatter Keypair with single "master" key\)

Scatter has multiple repositories with one of them being deprecated in favour of the newer ScatterBridge. ScatterBridge has a new issue regarding the prior unsolved issue of key management:

* you can only have a single key-pair within the Scatter KeyPair which is used for accounts and identification.

Solution:

Pre-requsites:

* form\(s\) to retrieve a Peerplays username & password from to generate keys and authorize account import requests with

Given the pre-requisites:

* we can generate all of a Peerplays accounts Wallet Import Format \(WIF\) keys
* convert an object representing the WIF data into a JSON string.

  ```text
  const wifs = {
      owner: 'ownerWIF',
      active: 'activeWIF',
      memo: 'memoWIF'
  };
  ```

* encrypt the JSON string using the owner public key as the "secret"
  * the "secret" is used to decrypt the WIFs again later
* store the "secret" \(owner public key\) under the Scatter `KeyPair.publicKeys[0].key`

Finally, store the keypair via Scatter so it can be retrieved later for other Peerplays actions.

* [x] storeKeys\(\)

**\[**[**3.3**](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-3-create-peerplays-account)**\] New account registration**

Request `username` and `password` from user. Check that `username` has not already been claimed via `getFullAccount()`. Send register request to chain faucet if form data is valid \(`register()`\). Once registration is complete, store the keys \(see end of 3.2\).

* [x] getFullAccount
* [x] register

**\[**[**3.4**](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys)**\] Peerplays Account Authorization \(Import\)**

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

#### \[[3.5](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-5-support-for-ppy-asset-retrieve-ppy-balance)\] Support for PPY Asset/Retrieve PPY Balance

Retrieve a users' Peerplays balance\(s\).

* [x] balanceFor
* [x] balancesFor

**\[**[**3.6**](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-6-send-ppy)**\] Transfer of funds with memo support \(required function: `transfer`\)**

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

**Peerplays Key Generation/Conversion**

* [x] privateFromWif → convert the PrivateKey class instantiated object from the Wallet Import Format \(WIF\) key
* [x] wifFromPrivate → convert the PrivateKey class instantiated object into the Wallet Import Format \(WIF\) key
* [x] privateToPublic → convert the Wallet Import Format \(WIF\) key into its public key

### Presentation Layer

{% hint style="info" %}
Many functions from Low-level Application Layer may require changes to account for specific formats of returned data for UI repositories making use of the Peerplays Scatter Plugin.
{% endhint %}

#### **\[**[**3.3**](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-3-create-peerplays-account)**\] Create Peerplays Account**

* [x] "Generate Keypair" via `username`, `generated_password` , and `password_confirm` fields that ultimately register a new account and store the keys for this new account \(once created\) within Scatter
* [x] modify functions \(`register`\) to return expected data for UI

#### **\[**[**3.4**](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys)**\] Import Peerplays Account**

* [x] "Import Key" via Peerplays' familiar username and password login: `username` and `password` form which will authorize `username` if keys generated from form data are authentic
* [x] modify functions to return expected data for UI

#### **\[**[**3.5**](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-5-support-for-ppy-asset-retrieve-ppy-balance)**\] Support for PPY Asset/Retrieve PPY Balance**

* [x] Displays PPY account Balance

#### \[[3.6](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-6-send-ppy)\] Transfer & Sign

Modify to return a promise `resolve` or `reject`. The `resolve` must return a transaction ID.

* [x] determine what the transaction ID represents \(block number?\)
* [x] modify return value to be compatible with UI

#### \[[3.7](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-7-receive-ppy)\] Receive PPY \(show username\)

* [x] Displays Peerplays username to give others



