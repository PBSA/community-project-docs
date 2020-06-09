# GPOS Patch 3, release v1.5.3-alpha

**Release Notes:** [https://github.com/peerplays-network/peerplays-core-gui/releases/tag/v1.5.3-alpha](https://github.com/peerplays-network/peerplays-core-gui/releases/tag/v1.5.3-alpha)

{% hint style="info" %}
copy of GPOS GUI - Power Up/Power Down : [https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/328270030/GPOS+GUI+-+Power+Up+Power+Down](https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/328270030/GPOS+GUI+-+Power+Up+Power+Down)
{% endhint %}

### **Sanity Testing**

**Pres-requisite** : new wallet account and existing account with GPOS balance

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Description</b>
      </th>
      <th style="text-align:left"><b>Expected Result</b>
      </th>
      <th style="text-align:left"><b>QA</b>
        <br /><b>Testing Notes</b>
      </th>
      <th style="text-align:left"><b>Pass/Fail</b>
      </th>
      <th style="text-align:left"><b>Build</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet</b> dApp with new wallet account created</td>
      <td
      style="text-align:left">
        <p>Should login successfully and display home page</p>
        <p>Validate <b>GPOS Panel</b> exists in right side of the wallet home page</p>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
        <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate content of the <b>GPOS Panel</b>
      </td>
      <td style="text-align:left">
        <p>GPOS Panel should contain</p>
        <ul>
          <li>GPOS description &quot;<b>Gamified Proof of Stake (GPOS) enables you to earn rewards of multiple cryptocurrencies supported in Peerplays by helping secure the network. Learn More</b>&quot; <b>note</b>:
            &#x2018;<b>Learn More</b>&#x2019; is a text button that will open the GPOS
            FAQ</li>
          <li>A button with text &quot;<b>GET STARTED</b>&quot; and background color
            green and is clickable</li>
          <li>Verify following parameters are displayed
            <ul>
              <li>GPOS Balance</li>
              <li>Voting Performance</li>
              <li>Quality Reward %</li>
              <li>Estimated rake reward %</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left">
        <p>&quot;GET STARTED&quot; Button is not Green</p>
        <p>
          <img src="https://peerplays.atlassian.net/wiki/download/thumbnails/328270030/image2019-12-13_17-37-12.png?version=1&amp;modificationDate=1576238834663&amp;cacheVersion=1&amp;api=v2&amp;width=150"
          alt/>
        </p>
      </td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on &quot;<b>GET STARTED</b>&quot; button in the GPOS Panel</td>
      <td
      style="text-align:left">Peerplays GPOS Wizard will open with Power Up, Power Down and Cancel buttons</td>
        <td
        style="text-align:left"></td>
          <td style="text-align:left">Pass</td>
          <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
          </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Click on &quot;<b>GET STARTED</b>&quot; button in the GPOS Panel and then
          Power Up</p>
        <p>Add amount 50 TEST to vest</p>
      </td>
      <td style="text-align:left">GPOS Panel should display GPOS Balance 50 TEST</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on CANCEL and Logout</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet</b> dApp with existing account with GPOS balance</td>
      <td
      style="text-align:left">
        <p>Should login successfully and display home page</p>
        <p>Validate <b>GPOS Panel</b> exists in right side of the wallet home page</p>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
        <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate content of the <b>GPOS Panel</b>
      </td>
      <td style="text-align:left">
        <p>GPOS Panel should contain</p>
        <ul>
          <li>GPOS description &quot;<b>Gamified Proof of Stake (GPOS) enables you to earn rewards of multiple cryptocurrencies supported in Peerplays by helping secure the network. Learn More</b>&quot; <b>note</b>:
            &#x2018;<b>Learn More</b>&#x2019; is a text button that will open the GPOS
            FAQ</li>
          <li>A button with text &quot;<b>PARTICIPATE&quot;</b>and background color
            blue and is clickable</li>
          <li>Verify following parameters are displayed
            <ul>
              <li>GPOS Balance</li>
              <li>Voting Performance</li>
              <li>Quality Reward %</li>
              <li>Estimated rake reward %</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on &quot;<b>PARTICIPATE</b>&quot; button in the GPOS Panel</td>
      <td
      style="text-align:left">Peerplays GPOS Wizard will open with Power Up, Power Down and Cancel buttons</td>
        <td
        style="text-align:left">No Cancel Button. Vote button instead of cancel.</td>
          <td style="text-align:left">Pass</td>
          <td style="text-align:left"><b>1.0.28</b>
          </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on CANCEL and Logout</td>
      <td style="text-align:left">Should logout successfully</td>
      <td style="text-align:left">No Cancel Button. Done button used</td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>1.0.28</b>
      </td>
    </tr>
  </tbody>
</table>

### **Functional Testing**

### **Validate content of GPOS Panel**

**Pre-requisite** : two wallet accounts user1 with vesting balance and user2 with zero vesting balance

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Description</b>
      </th>
      <th style="text-align:left"><b>Expected Result</b>
      </th>
      <th style="text-align:left"><b>QA</b>
        <br /><b>Testing Notes</b>
      </th>
      <th style="text-align:left"><b>Pass/Fail</b>
      </th>
      <th style="text-align:left"><b>Build</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet</b> dApp with user2 and password</td>
      <td style="text-align:left">Should login successfully and display home page</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>GPOS Panel</b> exists in right side of the wallet home page</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
        <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Validate content of the <b>GPOS Panel</b>
        </p>
        <p><b>If GPOS Balance &lt;= 0</b>
        </p>
      </td>
      <td style="text-align:left">
        <p>GPOS Panel should contain</p>
        <ul>
          <li>GPOS description &quot;<b>Gamified Proof of Stake (GPOS) enables you to earn rewards of multiple cryptocurrencies supported in Peerplays by helping secure the network. Learn More</b>&quot; <b>note</b>:
            &#x2018;<b>Learn More</b>&#x2019; is a text button that will open the GPOS
            FAQ</li>
          <li>A button with text &quot;<b>GET STARTED</b>&quot; and background color
            green and is clickable</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <ul>
          <li>Verify following parameter names are displayed (letter case should match)
            <ul>
              <li>GPOS Balance</li>
              <li>Voting Performance</li>
              <li>Quality Reward %</li>
              <li>Estimated Rake Reward %</li>
            </ul>
          </li>
        </ul>
        <p>Click on <b>&apos;Lean More&apos; </b>will open Help modal displaying GPOS
          section with Header<b> GAMIFIED PROOF OF STAKE</b> and content:</p>
        <p>The Peerplays blockchain uses Gamified Proof of Stake (GPOS) as the means
          to maintaining blockchain security while incorporating the human design
          element necessary for effective voting mechanics.</p>
        <p>By participating in GPOS you are staking your PPY for a period of 30 days.
          After the 30 day time period, you may request to withdraw the staked PPY.</p>
        <p>During the staking period, you will be capable of participating in the
          voting of node operators and other important functions within the Peerplays
          ecosystem. Advisors, Witnesses, new Proposals, SONs, and other types of
          nodes and providers that make up the Peerplays ecosystem will benefit from
          your votes.</p>
        <p>For your contribution in helping secure the blockchain, you will receive
          Participation Rewards. These rewards are based on the amount of PPY you
          have staked relative to the rest of the network distribution. Participation
          Rewards are given out each month and are based on the collective activity
          (i.e.: blockchain fees) on the Peerplays blockchain. As more value comes
          into the network, this is sent to you as a reward for helping make it happen.
          <br
          />For more detailed help please visit <a href="https://www.peerplays.com/ppy-tokens/#peerplays-core-wallet">https://www.peerplays.com/ppy-tokens/#peerplays-core-wallet</a>
        </p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Verify GPOS Balance</td>
      <td style="text-align:left">should be 0</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Verify Voting Performance</td>
      <td style="text-align:left">No Rewards in Dark Red</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Verify Quality Reward %</td>
      <td style="text-align:left">should be 0%</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Verify Estimated rake reward %</td>
      <td style="text-align:left">should be 0%</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Logout and Login to <b>PeerPlays Wallet</b> dApp with user1 and password</td>
      <td
      style="text-align:left">Should login successfully and display home page</td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
        <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>GPOS Panel</b> exists in right side of the wallet home page</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
        <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Validate content of the <b>GPOS Panel</b>
        </p>
        <p><b>If GPOS Balance &gt; 0</b>
        </p>
      </td>
      <td style="text-align:left">
        <p>GPOS Panel should contain</p>
        <ul>
          <li>GPOS description &quot;<b>Gamified Proof of Stake (GPOS) enables you to earn rewards of multiple cryptocurrencies supported in Peerplays by helping secure the network. Learn More</b>&quot; <b>note</b>:
            &#x2018;<b>Learn More</b>&#x2019; is a text button that will open the GPOS
            FAQ</li>
          <li>A button with text &quot;<b>PARTICIPATE&quot;</b>and background color
            blue and is clickable</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Verify GPOS Balance</td>
      <td style="text-align:left">should be total amount vested of type GPOS</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Verify Voting Performance</td>
      <td style="text-align:left">
        <p>Expected values is based on Vesting Factor</p>
        <p>Please refer to the table in next cell for expected text to display</p>
      </td>
      <td style="text-align:left"><b>Note</b>: This could be text that gives feedback on the user&apos;s
        voting performance ( <code>vesting_factor</code> ).</td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Quality Reward % = vesting factor * 100</td>
      <td style="text-align:left"><b>Note</b>: if there decimal places it should display only first two
        decimals</td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Verify Estimated rake reward %</td>
      <td style="text-align:left">
        <p>Estimated rake reward % = (b / TB) * p</p>
        <p>where</p>
        <p>b = User GPOS balance
          <br />TB = Total GPOS balance on blockchain
          <br />p = Reward %</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
  </tbody>
</table>

### **Getting Started/Power Up**

**Pre-requisite** : new wallet account or account without GPOS vesting balance

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Description</b>
      </th>
      <th style="text-align:left"><b>Expected Result</b>
      </th>
      <th style="text-align:left"><b>QA</b>
        <br /><b>Testing Notes</b>
      </th>
      <th style="text-align:left"><b>Pass/Fail</b>
      </th>
      <th style="text-align:left"><b>Build</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet</b> dApp with a valid username and password
        and with 0 GPOS balance</td>
      <td style="text-align:left">
        <p>Should login successfully and display home page</p>
        <p>In GPOS Panel, Only <b>Get Started </b>button should exist</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">In GPOS Panel, Click on <b>Get Started</b> button</td>
      <td style="text-align:left">
        <p><b>Peerplays GPOS Wizard</b> dialog will open and verify below content.</p>
        <p><b>Description</b>: &quot;Join GPOS by transferring your PPY to your GPOS
          balance.</p>
        <p>Consistently participate in voting for the best Witnesses, Advisors, Proposals,
          and SONs.</p>
        <p>Share the exciting news and DApps available on Peerplays with others.</p>
        <p>The more value that comes into Peerplays blockchain through its operations,
          the more those that participate to help make it secure will earn!</p>
        <p>If you want to increase your participation rewards you can do it two ways:</p>
        <ol>
          <li>Transfer more PPY into your GPOS balance</li>
          <li>Share Peerplays with others</li>
        </ol>
        <p>Together as a Decentralized Autonomous Cooperative (DAC), we can ensure
          Peerplays remains the most secure provably fair blockchain globally.&quot;</p>
        <p><b>POWER UP, </b>  <b>POWER DOWN</b> , <b>VOTE</b> and <b>CANCEL </b> buttons
          should exist</p>
        <p>POWER UP button should be enabled</p>
        <p>POWER DOWN button should be disabled</p>
        <p>VOTE button should be disabled</p>
        <p>CANCEL button should be enabled</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>POWER UP </b>button</td>
      <td style="text-align:left">
        <p>Power Up screen will open with</p>
        <p><b>Description</b>:</p>
        <p>When you Power Up your PPY on the Peerplays blockchain you are taking
          your first steps into participating in the Decentralized Autonomous Cooperative
          (DAC) that is the magic in blockchain tech. This means you will:</p>
        <ul>
          <li>Become a big part of something special on a global scale</li>
          <li>Earn participation rewards for your efforts</li>
          <li>Bragging rights to family and friends</li>
          <li>Stake your PPY while you participate</li>
          <li>Help secure the Peerplays blockchain</li>
        </ul>
        <p><b>Opening GPOS Balance</b>
        </p>
        <p><b>Deposit</b> field</p>
        <p><b>New GPOS Balance </b>
        </p>
        <p><b>CANCEL</b> button will be enabled</p>
        <p><b>SUBMIT</b> button will be disabled</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>CANCEL</b> button</td>
      <td style="text-align:left">returns to previous step - &quot;Getting Started&quot;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Get Started</b> button</td>
      <td style="text-align:left">Getting Started dialog will open</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Opening GPOS Balance</b>
      </td>
      <td style="text-align:left">should be 0 PPY</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>New GPOS Balance</b>
      </td>
      <td style="text-align:left">same as Opening GPOS Balance</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Deposit</b> input field</td>
      <td style="text-align:left">
        <p>Validate:</p>
        <ol>
          <li>Only numbers are permitted</li>
          <li>Character limit of 32</li>
          <li>Negative numbers not permitted</li>
          <li>Numbers larger than available balance not permitted</li>
        </ol>
      </td>
      <td style="text-align:left">
        <p><b>Comment</b>:</p>
        <ol>
          <li>E and e are permitted in deposit field.
            <img src="https://peerplays.atlassian.net/wiki/plugins/servlet/confluence/placeholder/macro?definition=e2ppcmE6a2V5PVdBTC0zMDR9&amp;locale=en_GB"
            alt/>
          </li>
          <li>Can&apos;t check character limit of 32 as don&apos;t have so many TEST
            for same.</li>
        </ol>
      </td>
      <td style="text-align:left"><b>Fail</b>
      </td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Enter valid PPY amount in <b>Deposit</b> field</td>
      <td style="text-align:left">
        <p>should not throw any error</p>
        <p><b>New GPOS Balance</b> should display the amount entered in Deposit field</p>
        <p><b>SUBMIT</b> button will be enabled</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>SUBMIT</b> button</td>
      <td style="text-align:left">
        <p>The content where the form exists will be replaced with a loading animation</p>
        <p>The &quot;Submit&quot; and &quot;Cancel&quot; buttons will be disabled
          during this animation.</p>
        <p>User should not be able to close the modal/dialog during this animation.</p>
        <p><b>On Success:</b>
        </p>
        <ul>
          <li>Loading animation goes away and in its place display a success message.
            <ul>
              <li>&quot;You have successfully Powered Up!&quot;.</li>
              <li>And a <b>Next </b>button</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><b>On Failure:</b>
        </p>
        <ul>
          <li>Loading animation goes away and in its place display a failure message.
            <ul>
              <li>&quot;You have failed to Power Up!&quot;</li>
              <li>and a &quot;<b>Retry</b>&quot; button</li>
              <li>click on &quot;<b>Retry</b>&quot; will <em><b>reset</b></em> the Power Up
                form to what it was as if it had never failed</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left">
        <p><b>Comment</b>:</p>
        <ol>
          <li>No such condition arises</li>
        </ol>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>If Power Up was success,</b>
        </p>
        <p>Click on <b>Next</b> button</p>
      </td>
      <td style="text-align:left">
        <p>Should take to Peerplays GPOS Wizad which has Power Up, Power Down , Vote
          and Done buttons.</p>
        <p>All button should be enabled</p>
      </td>
      <td style="text-align:left">
        <p><b>Comment</b>:</p>
        <ol>
          <li>Power Up button is disabled.</li>
          <li>If user logout and again login then all button&apos;s are enabled.</li>
          <li>
            <img src="https://peerplays.atlassian.net/wiki/plugins/servlet/confluence/placeholder/macro?definition=e2ppcmE6a2V5PVdBTC0zMDJ9&amp;locale=en_GB"
            alt/>
          </li>
        </ol>
      </td>
      <td style="text-align:left"><b>Fail</b>
      </td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Done</b> button</td>
      <td style="text-align:left">
        <p>GPOS Wizard will close.</p>
        <p>In Wallet Main Page</p>
        <ul>
          <li>Verify GPOS metrics ; GPOS Balance and Estimated Rake Reward % are updated
            on GPOS Panel
            <ul>
              <li>GPOS Balance = Power Up Balance</li>
              <li>Estimated Rake Reward % = (User GPOS Balance/ Network GPOS Balance) *
                Vesting Factor</li>
              <li>Get Started button will be replaced with Participate button</li>
            </ul>
          </li>
          <li>also main account balance/Available Balances
            <ul>
              <li>Available Balances = Prev Available Balances - Power Up Balance - Transaction
                Fee</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
  </tbody>
</table>

### **Participate/Power Up**

**Pre-requisite** : Peerplays account with GPOS vesting balance

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Description</b>
      </th>
      <th style="text-align:left"><b>Expected Result</b>
      </th>
      <th style="text-align:left"><b>QA</b>
        <br /><b>Testing Notes</b>
      </th>
      <th style="text-align:left"><b>Pass/Fail</b>
      </th>
      <th style="text-align:left"><b>Build</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet</b> dApp with a valid username and password
        and with GPOS balance &gt; 0</td>
      <td style="text-align:left">
        <p>Should login successfully and display home page</p>
        <p>GPOS Panel should contain</p>
        <ul>
          <li>GPOS description</li>
          <li>A button with text &quot;Participate&quot; and is clickable</li>
          <li>GPOS Balance</li>
          <li>Voting Performance</li>
          <li>Quality Reward %</li>
          <li>Estimated Rake Reward %</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">In GPOS Panel, Click on <b>Participate</b> button</td>
      <td style="text-align:left">
        <p><b>Peerplays GPOS Wizard </b>dialog will open and verify below content.</p>
        <p><b>Description</b>: &quot;Join GPOS by transferring your PPY to your GPOS
          balance.</p>
        <p>Consistently participate in voting for the best Witnesses, Advisors, Proposals,
          and SONs.</p>
        <p>Share the exciting news and DApps available on Peerplays with others.</p>
        <p>The more value that comes into Peerplays blockchain through its operations,
          the more those that participate to help make it secure will earn!</p>
        <p>If you want to increase your participation rewards you can do it two ways:</p>
        <ol>
          <li>Transfer more PPY into your GPOS balance</li>
          <li>Share Peerplays with others</li>
        </ol>
        <p>Together as a Decentralized Autonomous Cooperative (DAC), we can ensure
          Peerplays remains the most secure provably fair blockchain globally.&quot;</p>
        <p><b>POWER UP, </b>  <b>POWER DOWN</b> , <b>VOTE</b> and <b>CANCEL </b> buttons
          should exist</p>
        <p>POWER UP button should be enabled</p>
        <p>POWER DOWN button should be enabled</p>
        <p>VOTE button should be enabled</p>
        <p>CANCEL button should be enabled</p>
      </td>
      <td style="text-align:left">
        <p><b>Comment:</b>
        </p>
        <ol>
          <li>If user logout and again login then all button&apos;s are enabled.</li>
        </ol>
        <p>
          <img src="https://peerplays.atlassian.net/wiki/plugins/servlet/confluence/placeholder/macro?definition=e2ppcmE6a2V5PVdBTC0zMDJ9&amp;locale=en_GB"
          alt/>
        </p>
      </td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>POWER UP</b> button</td>
      <td style="text-align:left">
        <p>Power Up screen will open with</p>
        <p><b>Description</b>:</p>
        <p>When you Power Up your PPY on the Peerplays blockchain you are taking
          your first steps into participating in the Decentralized Autonomous Cooperative
          (DAC) that is the magic in blockchain tech. This means you will:</p>
        <ul>
          <li>Become a big part of something special on a global scale</li>
          <li>Earn participation rewards for your efforts</li>
          <li>Bragging rights to family and friends</li>
          <li>Stake your PPY while you participate</li>
          <li>Help secure the Peerplays blockchain</li>
        </ul>
        <p><b>Opening GPOS Balance</b>
        </p>
        <p><b>Deposit</b> field</p>
        <p><b>New GPOS Balance </b>
        </p>
        <p><b>CANCEL</b> button will be enabled</p>
        <p><b>SUBMIT</b> button will be disabled</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Opening GPOS Balance</b>
      </td>
      <td style="text-align:left">should be current gpos balance of the user say X PPY/TEST</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Current GPOS Balance</b>
      </td>
      <td style="text-align:left">should be same Opening GPOS Balance</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Deposit</b> input field</td>
      <td style="text-align:left">
        <p>Validate:</p>
        <ol>
          <li>Only numbers are permitted</li>
          <li>Character limit of 32</li>
          <li>Negative numbers not permitted</li>
          <li>Numbers larger than available balance not permitted</li>
        </ol>
      </td>
      <td style="text-align:left">
        <p><b>Comment</b>:</p>
        <ol>
          <li>E and e are permitted in deposit field.
            <img src="https://peerplays.atlassian.net/wiki/plugins/servlet/confluence/placeholder/macro?definition=e2ppcmE6a2V5PVdBTC0zMDR9&amp;locale=en_GB"
            alt/>
          </li>
          <li>Can&apos;t check character limit of 32 as don&apos;t have so many TEST
            for same.</li>
        </ol>
      </td>
      <td style="text-align:left"><b>Fail</b>
      </td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Enter valid PPY amount in <b>Deposit</b> input field</td>
      <td style="text-align:left">
        <p>should not throw any error</p>
        <p><b>New GPOS Balance</b> = Deposit Amount + Opening GPOS balance(X)</p>
        <p><b>SUBMIT</b> button will be enabled</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>SUBMIT</b> button</td>
      <td style="text-align:left">
        <p>The content where the form exists will be replaced with a loading animation</p>
        <p>The &quot;Submit&quot; and &quot;Cancel&quot; buttons will be disabled
          during this animation.</p>
        <p>User should not be able to close the modal/dialog during this animation.</p>
        <p><b>On Success:</b>
        </p>
        <ul>
          <li>Loading animation goes away and in its place display a success message.
            <ul>
              <li>&quot;You have successfully Powered Up!&quot;.</li>
              <li>And a <b>Next </b>button</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><b>On Failure:</b>
        </p>
        <ul>
          <li>Loading animation goes away and in its place display a failure message.
            <ul>
              <li>&quot;You have failed to Power Up!&quot;</li>
              <li>and a &quot;<b>Retry</b>&quot; button</li>
              <li>click on &quot;<b>Retry</b>&quot; will <em><b>reset</b></em> the Power Up
                form to what it was as if it had never failed</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left">
        <p><b>Comment</b>:</p>
        <ol>
          <li>No such condition arises</li>
        </ol>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>If Power Up was success,</b>
        </p>
        <p>Click on <b>Next</b> button</p>
      </td>
      <td style="text-align:left">
        <p>Should take to Peerplays GPOS Wizad which has Power Up, Power Down , Vote
          and Done buttons.</p>
        <p>All button should be enabled</p>
      </td>
      <td style="text-align:left">
        <p><b>Comment</b>:</p>
        <ol>
          <li>Power Up button is disabled.
            <img src="https://peerplays.atlassian.net/wiki/plugins/servlet/confluence/placeholder/macro?definition=e2ppcmE6a2V5PVdBTC0zMDJ9&amp;locale=en_GB"
            alt/>
          </li>
          <li>If user logout and again login then all button&apos;s are enabled.</li>
        </ol>
      </td>
      <td style="text-align:left"><b>Fail</b>
      </td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Done</b> button</td>
      <td style="text-align:left">
        <p>GPOS Wizard will close.</p>
        <p>In Wallet Main Page</p>
        <ul>
          <li>Verify GPOS metrics - GPOS Balance and Estimated Rake Reward % are updated
            on GPOS Panel
            <ul>
              <li>GPOS Balance = Previous GPOS Balance + New Power Up Balance</li>
              <li>Estimated Rake Reward % = (User GPOS Balance/ Network GPOS Balance) *
                Vesting Factor</li>
            </ul>
          </li>
          <li>also main account balance/Available Balances
            <ul>
              <li>Available Balances = Prev Available Balances - Power Up Balance - Transaction
                Fee</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
  </tbody>
</table>

### **Participate/Power Down**

**Pre-requisite** : Peerplays account with GPOS vesting balance

**Note: This testcase should be executed for the following cases:**

1. User has made single vesting, it has passed lockin period and available for withdrawal →  withdraw partial amount and then remaining amount
2. User has made multiple vesting, atleast first vesting has passed lockin period →  withdraw first vesting balance
3. User has made multiple vesting, two or more vesting have passed lockin period → make a withdraw where withdraw amount = sum of more 2 or more vesting balances 
4. **Note: withdraw transaction fee should be same for all the scenarios mentioned above**

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Description</b>
      </th>
      <th style="text-align:left"><b>Expected Result</b>
      </th>
      <th style="text-align:left"><b>QA</b>
        <br /><b>Testing Notes</b>
      </th>
      <th style="text-align:left"><b>Pass/Fail</b>
      </th>
      <th style="text-align:left"><b>Build</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet</b> dApp with a valid username and password
        and with GPOS balance &gt; 0</td>
      <td style="text-align:left">
        <p>Should login successfully and display home page</p>
        <p>GPOS Panel should contain</p>
        <ul>
          <li>A button with text &quot;Participate&quot; and is clickable</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">In GPOS Panel, Click on <b>Participate</b> button</td>
      <td style="text-align:left">
        <p><b>Peerplays GPOS Wizard </b>dialog will open and verify below content.</p>
        <p><b>Description</b>: &quot;Join GPOS by transferring your PPY to your GPOS
          balance.</p>
        <p>Consistently participate in voting for the best Witnesses, Advisors, Proposals,
          and SONs.</p>
        <p>Share the exciting news and DApps available on Peerplays with others.</p>
        <p>The more value that comes into Peerplays blockchain through its operations,
          the more those that participate to help make it secure will earn!</p>
        <p>If you want to increase your participation rewards you can do it two ways:</p>
        <ol>
          <li>Transfer more PPY into your GPOS balance</li>
          <li>Share Peerplays with others</li>
        </ol>
        <p>Together as a Decentralized Autonomous Cooperative (DAC), we can ensure
          Peerplays remains the most secure provably fair blockchain globally.&quot;</p>
        <p><b>POWER UP, </b>  <b>POWER DOWN</b> , <b>VOTE</b> and <b>CANCEL </b> buttons
          should exist</p>
        <p>POWER UP button should be enabled</p>
        <p>POWER DOWN button should be enabled</p>
        <p>VOTE button should be enabled</p>
        <p>CANCEL button should be enabled</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>POWER DOWN</b> button</td>
      <td style="text-align:left">
        <p>Power Down screen will open with following info</p>
        <p><b>Description</b>:</p>
        <p>When you Power Down it will take 30 days for you to withdraw your PPY
          balance in full. You will continue to receive participation rewards during
          that time so long as you have been participating. After Power Down you
          can then use your PPY like any other cryptocurrency. This means you will:</p>
        <ul>
          <li>Still be a part of something special, just not as much</li>
          <li>No longer helping secure the Peerplays blockchain</li>
          <li>No longer earn participation rewards</li>
          <li>Lose bragging rights</li>
          <li>Stop staking your PPY</li>
        </ul>
        <p>Opening GPOS Balance</p>
        <p>Available GPOS Balance</p>
        <p>Withdraw Field</p>
        <p>New GPOS Balance</p>
        <p><b>CANCEL</b> button will be enabled</p>
        <p><b>SUBMIT</b> button will be disabled</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Opening GPOS Balance</b>
      </td>
      <td style="text-align:left">should be current gpos balance of the user say X TEST</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Available GPOS Balance</b>
      </td>
      <td style="text-align:left">should be withdrawable gpos balance (Vesting balances which have crossed
        lock in period) of the user say X TEST</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Withdraw</b> input field</td>
      <td style="text-align:left">
        <p>Validate:</p>
        <ol>
          <li>Only numbers are permitted</li>
          <li>Character limit of 32</li>
          <li>Negative numbers not permitted</li>
          <li>Numbers larger than available balance not permitted</li>
        </ol>
      </td>
      <td style="text-align:left">
        <p><b>Comment</b>:</p>
        <ol>
          <li>E and e are permitted in deposit field.</li>
        </ol>
        <p>
          <img src="https://peerplays.atlassian.net/wiki/plugins/servlet/confluence/placeholder/macro?definition=e2ppcmE6a2V5PVdBTC0zMDR9&amp;locale=en_GB"
          alt/>
        </p>
        <ol>
          <li>Can&apos;t check char limit of 32 as don&apos;t have sum for same.</li>
        </ol>
      </td>
      <td style="text-align:left"><b>Fail</b>
      </td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Enter valid PPY/TEST amount in <b>Withdraw</b> input field</td>
      <td style="text-align:left">
        <p>should not throw any error</p>
        <p><b>New GPOS Balance</b> = Opening GPOS balance(X) - Withdraw amount</p>
        <p><b>SUBMIT</b> button will be enabled</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>SUBMIT</b> button</td>
      <td style="text-align:left">
        <p>The content where the form exists will be replaced with a loading animation</p>
        <p>The &quot;Submit&quot; and &quot;Cancel&quot; buttons will be disabled
          during this animation.</p>
        <p>User should not be able to close the modal/dialog during this animation.</p>
        <p><b>On Success:</b>
        </p>
        <ul>
          <li>Loading animation goes away and in its place display a success message.
            <ul>
              <li>&quot;You have successfully Powered Down!&quot;.</li>
              <li>And a <b>Next </b>button</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p><b>On Failure:</b>
        </p>
        <ul>
          <li>Loading animation goes away and in its place display a failure message.
            <ul>
              <li>&quot;You have failed to Power Down!&quot;</li>
              <li>and a &quot;<b>Retry</b>&quot; button</li>
              <li>click on &quot;<b>Retry</b>&quot; will <em><b>reset</b></em> the Power Down
                form to what it was as if it had never failed</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left">
        <p><b>Comment</b>:</p>
        <ol>
          <li>No such condition arises</li>
        </ol>
      </td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>If Power Down was success,</b>
        </p>
        <p>Click on <b>Next</b> button</p>
      </td>
      <td style="text-align:left">
        <p>Should take to Peerplays GPOS Wizad which has Power Up, Power Down , Vote
          and Done buttons.</p>
        <p>If GPOS Balance is 0, then except Power Up and Done button, all others
          should be disabled</p>
        <p>If GPOS Balance &gt; 0, then all button should be enabled</p>
      </td>
      <td style="text-align:left">
        <p><b>Comment</b>:</p>
        <p>Failed case</p>
        <p>When GPOS Balance &gt; 0</p>
        <ol>
          <li>Power Down button is disabled</li>
        </ol>
        <p>
          <img src="https://peerplays.atlassian.net/wiki/plugins/servlet/confluence/placeholder/macro?definition=e2ppcmE6a2V5PVdBTC0zMDJ9&amp;locale=en_GB"
          alt/>
        </p>
      </td>
      <td style="text-align:left">Fail</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Done</b> button</td>
      <td style="text-align:left">
        <p>GPOS Wizard will close.</p>
        <p>In Wallet Main Page</p>
        <ul>
          <li>Verify GPOS metrics - GPOS Balance and Estimated Rake Reward % are updated
            on GPOS Panel
            <ul>
              <li>GPOS Balance = Previous GPOS Balance - Withdraw Balance</li>
              <li>Estimated Rake Reward % = (User GPOS Balance/ Network GPOS Balance) *
                Vesting Factor</li>
              <li>If GPOS Balance = 0, verify Participate button is replaced with Get Started
                button</li>
            </ul>
          </li>
          <li>also main account balance/Available Balances
            <ul>
              <li>Available Balances = Prev Available Balances + Withdraw Balance - Transaction
                Fee</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left"><b>Note</b>: Network/Total GPOS Balance can be fetched using get_gpos_info
        api call</td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Logout and Login and then navigate to Power Down Modal</td>
      <td style="text-align:left">Verify Opening GPOS Balance and Available GPOS balances up to date</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
        <td style="text-align:left"><b>Peerplays-Core-GUI- 1.5.1-alpha</b>
        </td>
    </tr>
  </tbody>
</table>





