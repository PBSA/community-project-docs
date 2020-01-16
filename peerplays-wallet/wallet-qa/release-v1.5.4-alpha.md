# release v1.5.4-alpha

**Release Notes:** [https://github.com/peerplays-network/peerplays-core-gui/releases/tag/v1.5.4-alpha](https://github.com/peerplays-network/peerplays-core-gui/releases/tag/v1.5.3-alpha)

{% hint style="info" %}
This build has the GPOS features and is the first Wallet code base with GPOS to be released to public
{% endhint %}

## **Sanity Testing**

### **Power Up/Power Down**

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
    </tr>
    <tr>
      <td style="text-align:left">Click on &quot;<b>GET STARTED</b>&quot; button in the GPOS Panel</td>
      <td
      style="text-align:left">Peerplays GPOS Wizard will open with Power Up, Power Down and Cancel buttons</td>
        <td
        style="text-align:left"></td>
          <td style="text-align:left">Pass</td>
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
    </tr>
    <tr>
      <td style="text-align:left">Click on CANCEL and Logout</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
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
    </tr>
    <tr>
      <td style="text-align:left">Click on &quot;<b>PARTICIPATE</b>&quot; button in the GPOS Panel</td>
      <td
      style="text-align:left">Peerplays GPOS Wizard will open with Power Up, Power Down and Cancel buttons</td>
        <td
        style="text-align:left">No Cancel Button. Vote button instead of cancel.</td>
          <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on CANCEL and Logout</td>
      <td style="text-align:left">Should logout successfully</td>
      <td style="text-align:left">No Cancel Button. Done button used</td>
      <td style="text-align:left">Pass</td>
    </tr>
  </tbody>
</table>## \*\*\*\*

### **Vote**

\*\*\*\*

**Pre-requisite**: Valid Peerplays wallet account with GPOS balance

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
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet</b>d App with a valid username and password</td>
      <td
      style="text-align:left">Should login successfully and display Home page/My Funds page</td>
        <td
        style="text-align:left"></td>
          <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">In GPOS Panel, Click on <b>Participate </b>button</td>
      <td style="text-align:left"><b>Peerplays GPOS Wizard</b> will open</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <p>Vote screen/dialog/modal will be loaded with three tabs <b>Proxy</b>, <b>Witnesses</b> and <b>Advisors</b>
        </p>
        <p>By default Proxy tab will be selected in Vote screen</p>
        <p>Verify proxy search filed is there</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Cancel</b> button</td>
      <td style="text-align:left">Return to Participate screen</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Vote </b>button</td>
      <td style="text-align:left">Vote screen will open</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Witnesses</b> Tab</td>
      <td style="text-align:left">
        <p>Should load witnesses tab without any error</p>
        <p>Verify Witness search field, Witnesses approved by user and Witnesses
          not approved by user sections are there</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Cancel</b> button</td>
      <td style="text-align:left">Return to Participate screen</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Vote </b>button</td>
      <td style="text-align:left">Vote screen will open</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Advisors </b>Tab</td>
      <td style="text-align:left">
        <p>Should load Advisors tab without any error</p>
        <p>Verify Advisors search field, Advisors approved by user and Advisors not
          approved by user sections are there</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Cancel</b> button</td>
      <td style="text-align:left">Return to Participate screen</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
  </tbody>
</table>## \*\*\*\*

## **Functional Testing**

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
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet</b> dApp with user2 and password</td>
      <td style="text-align:left">Should login successfully and display home page</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>GPOS Panel</b> exists in right side of the wallet home page</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
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
    </tr>
    <tr>
      <td style="text-align:left">Verify GPOS Balance</td>
      <td style="text-align:left">should be 0</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Verify Voting Performance</td>
      <td style="text-align:left">No Rewards in Dark Red</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Verify Quality Reward %</td>
      <td style="text-align:left">should be 0%</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Verify Estimated rake reward %</td>
      <td style="text-align:left">should be 0%</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Logout and Login to <b>PeerPlays Wallet</b> dApp with user1 and password</td>
      <td
      style="text-align:left">Should login successfully and display home page</td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>GPOS Panel</b> exists in right side of the wallet home page</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
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
    </tr>
    <tr>
      <td style="text-align:left">Verify GPOS Balance</td>
      <td style="text-align:left">should be total amount vested of type GPOS</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
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
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">Quality Reward % = vesting factor * 100</td>
      <td style="text-align:left"><b>Note</b>: if there decimal places it should display only first two
        decimals</td>
      <td style="text-align:left">Pass</td>
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
    </tr>
  </tbody>
</table>### **Getting Started/Power Up**

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
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>CANCEL</b> button</td>
      <td style="text-align:left">returns to previous step - &quot;Getting Started&quot;</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Get Started</b> button</td>
      <td style="text-align:left">Getting Started dialog will open</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Opening GPOS Balance</b>
      </td>
      <td style="text-align:left">should be 0 PPY</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>New GPOS Balance</b>
      </td>
      <td style="text-align:left">same as Opening GPOS Balance</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
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
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
      <td style="text-align:left">Pass</td>
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
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
      <td style="text-align:left">Pass</td>
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
    </tr>
  </tbody>
</table>### **Participate/Power Up**

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
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
      <td style="text-align:left">Pass</td>
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
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Opening GPOS Balance</b>
      </td>
      <td style="text-align:left">should be current gpos balance of the user say X PPY/TEST</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Current GPOS Balance</b>
      </td>
      <td style="text-align:left">should be same Opening GPOS Balance</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
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
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
      <td style="text-align:left">Pass</td>
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
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
      <td style="text-align:left">Pass</td>
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
    </tr>
  </tbody>
</table>### **Participate/Power Down**

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
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Opening GPOS Balance</b>
      </td>
      <td style="text-align:left">should be current gpos balance of the user say X TEST</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Available GPOS Balance</b>
      </td>
      <td style="text-align:left">should be withdrawable gpos balance (Vesting balances which have crossed
        lock in period) of the user say X TEST</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
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
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
      <td style="text-align:left">Pass</td>
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
      <td style="text-align:left">&lt;b&gt;&lt;/b&gt;</td>
      <td style="text-align:left">Pass</td>
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
    </tr>
    <tr>
      <td style="text-align:left">Logout and Login and then navigate to Power Down Modal</td>
      <td style="text-align:left">Verify Opening GPOS Balance and Available GPOS balances up to date</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
  </tbody>
</table>



### **Vote for Proxy**

**Pre-requisite**: Valid Peerplays wallet account with GPOS balance

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
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet </b>dApp with a valid username and password</td>
      <td
      style="text-align:left">Should login successfully and display home page/My Funds page</td>
        <td
        style="text-align:left"></td>
          <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">In GPOS Panel, Click on <b>Participate </b>button</td>
      <td style="text-align:left"><b>Peerplays GPOS Wizard</b> will open</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Vote </b>button</td>
      <td style="text-align:left">
        <p>Vote screen will open</p>
        <p>By default Proxy tab will be selected in Vote screen</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">In the Proxy search field, enter a valid peerplays account name other
        than self account</td>
      <td style="text-align:left"><b>ADD </b>button next to search field is enabled</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on ADD button</td>
      <td style="text-align:left">Proxy will be added to the proxy display table</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Verify that the Remove button appears next to the added Account&apos;s
        name in the table</td>
      <td style="text-align:left">Once the new Proxy candidate account is added to the table the Remove
        button is enabled</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Select the proxy Account&apos;s name and click on Remove button.
        <br />
        <br />Verify the result.</td>
      <td style="text-align:left">The account is removed from the table</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Try adding proxy again as such previous steps</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left">Try to add multiple proxies</td>
      <td style="text-align:left">The app should not allow multiple proxies</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Press on <b>Reset Changes </b>button and verify the result.</td>
      <td style="text-align:left">Refreshes the page without committing the changes.
        <br />
        <br />The new updated information for the tested accounts in the previous step
        is not relevant anymore.</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Add valid account to the list, using the Account Name field on the <b>Proxy </b>screen
        and click on <b>Publish Changes </b>button
        <br />
        <br />Verify the result</td>
      <td style="text-align:left">
        <p>Clicking on &quot;Add&quot; button adds that account to the list.</p>
        <p>Clicking on <b>Publish Changes </b>button opens the Transaction confirmation
          window with the charging fees.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Press on Cancel button and verify the result</td>
      <td style="text-align:left">Clicking on Cancel button cancels the new Proxy voting operation.</td>
      <td
      style="text-align:left">
        <p><b>Comment</b>:</p>
        <p>If I set a proxy and then add another proxy but press cancel button before
          publishing changes then publish changes button gets disabled. Publish button
          shouldn&apos;t get disabled according to ideal condition.</p>
        </td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Add valid account to the list, using the Account Name field on the <b>Proxy </b>screen
          and press on <b>Publish Changes</b>button.</p>
        <p>Confirm the Transaction by clicking on Confirm button and verify the result</p>
      </td>
      <td style="text-align:left">The Proxy entry will be added successfully</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Finish </b>button</td>
      <td style="text-align:left">&quot;Thank you for Voting&quot; modal/dialog will show up</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Verify the content of the &quot;Thank you for Voting&quot; dialog</td>
      <td
      style="text-align:left">
        <p>Expected content:</p>
        <p>This is now your blockchain as part of the decentralized autonomous cooperative.
          The value it brings is what you and others bring to it, so go out and:</p>
        <ul>
          <li>Share Peerplays with others</li>
          <li>Share your voting decisions with the community, including why you voted
            the way you did</li>
          <li>Visit Peerplays social media and like, share, or retweet our latest posts,
            and provide feedback</li>
        </ul>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Ok</b> button</td>
      <td style="text-align:left">Dialogue closes and return to Participate Screen</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on Done</td>
      <td style="text-align:left">
        <p>Wallet home page is loaded.</p>
        <p>In GPOS Panel, Verify Voting Performance, Qualified Rewards % and Estimated
          Rake Rewards % is updated</p>
        <p>Voting Performance = &lt;&lt;Voting Performance of Proxy account&gt;&gt;</p>
        <p>Qualified Rewards % = &lt;&lt;Qualified Rewards % of Proxy account&gt;&gt;</p>
        <p>Estimated Rake Reward % = (User GPOS balance/Network GPOS balance) * Qualified
          Rewards %</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Wait for the next maintenance interval to pass , navigate to votes dialog.</td>
      <td
      style="text-align:left"><em>Verify <b>votes of each of the witnesses and advisors, proxy account has voted</b> is equal to <b>(user_gpos_balance + proxy_gpos_balance) * proxy_vesting_factor</b></em>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Perform previous two steps validations in next sub-periods of current vesting period</b>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
  </tbody>
</table>### **Vote for Witness** 

**Pre-requisite**: Valid Peerplays wallet account with GPOS balance

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
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet </b>dApp with a valid username and password</td>
      <td
      style="text-align:left">Should login successfully and display home page/My Funds page</td>
        <td
        style="text-align:left"></td>
          <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">In GPOS Panel, Click on <b>Participate </b>button</td>
      <td style="text-align:left"><b>Peerplays GPOS Wizard</b> will open</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Vote </b>button</td>
      <td style="text-align:left">
        <p>Power Up should be successful and should take user to Vote screen with
          3 tabs :</p>
        <ul>
          <li><b>Proxy</b>
          </li>
          <li><b>Witness</b>
          </li>
          <li><b>Advisors</b>
          </li>
        </ul>
        <p>By default <b>Proxy </b>tab will be selected in Vote screen</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Select the <b>Witness </b>tab and verify the information on the page.</td>
      <td
      style="text-align:left">The content for the Witness page is loaded and includes the option to
        add a Witness and the list of available Witnesses on the BlockChain</td>
        <td
        style="text-align:left"></td>
          <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Input the valid Witness account to the Account Name field on the <b>Witness </b>screen</td>
      <td
      style="text-align:left">ADD button will be enabled</td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Press on ADD button next to the search Account Name bar</td>
      <td style="text-align:left">
        <p>ADD button adds account from the search result to the <b>Witnesses approved by &lt;&lt;user account&gt;&gt;</b>table</p>
        <p>Verify that the Remove button appears next to the added Account&apos;s
          name in the table</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Select the added Account&apos;s name and press on Remove button.
        <br />
        <br />Verify the result.</td>
      <td style="text-align:left">The account is removed as a witness from the list</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Add a valid witness account again</td>
      <td style="text-align:left">Witness details appears under approved witness list
        <br />
        <br />
        <br />
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Reset Changes </b>button</td>
      <td style="text-align:left">Resets unpublished changes</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Add valid witness account to the list, using the Account Name field on
          the <b>Witness </b>screen.</p>
        <p>Click on <b>Publish Changes </b>button and verify the result.
          <br />
          <br />
        </p>
      </td>
      <td style="text-align:left">
        <p>Add button adds account from the search result to the <b>Witnesses approved by &lt;&lt;user account&gt;&gt;</b>table</p>
        <p>Note down the Votes of added witness account
          <br />
          <br />Clicking on <b>Publish Changes </b>button opens the Transaction confirmation
          window with the transaction fees.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on Cancel button</td>
      <td style="text-align:left">Closes confirmation window</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Publish Changes </b>button and <b>Confirm </b>the Transaction.</td>
      <td
      style="text-align:left">
        <p>Clicking on <b>Publish Changes </b>button opens the Transaction confirmation
          window with the transaction fees.</p>
        <p>After transaction is confirmed, witness will appear under <b>Witnesses approved by &lt;&lt;user account&gt;&gt;</b>table</p>
        <p>note: If user doesn&apos;t have enough account balance to pay the fee,
          then transaction fails</p>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Finish </b>button</td>
      <td style="text-align:left">&quot;Thank you for Voting&quot; modal/dialog will show up</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Verify the content of the &quot;Thank you for Voting&quot; pop up</td>
      <td
      style="text-align:left">
        <p>Expected content:</p>
        <p>This is now your blockchain as part of the decentralized autonomous cooperative.
          The value it brings is what you and others bring to it, so go out and:</p>
        <ul>
          <li>Share Peerplays with others</li>
          <li>Share your voting decisions with the community, including why you voted
            the way you did</li>
          <li>Visit Peerplays social media and like, share, or retweet our latest posts,
            and provide feedback</li>
        </ul>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Ok</b> button</td>
      <td style="text-align:left">Dialogue closes and return to Participate Screen</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on Done</td>
      <td style="text-align:left">
        <p>Wallet home page is loaded.</p>
        <p>In GPOS Panel, Verify Voting Performance, Qualified Rewards % and Estimated
          Rake Rewards % is updated</p>
        <p>Voting Performance = Max Rewards</p>
        <p>Qualified Rewards % = 100%</p>
        <p>Estimated Rake Reward % = (user gpos balance/network gpos balance) * 100%</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Wait for the next maintenance interval to pass , navigate to votes modal.</td>
      <td
      style="text-align:left"><em>Verify votes of each of the witnesses and advisors user has voted is equal to current gpos balance</em>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Perform previous two steps validations in next sub-periods of vesting period</b>
      </td>
      <td style="text-align:left">
        <p><b>Note</b>: since user is not participating in voting in upcoming sub-periods,
          his vesting_factor goes down in each sub-period and</p>
        <p>vesting factor affects all the above parameters value</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
  </tbody>
</table>### **Vote for Advisors**

**Pre-requisite**: Valid Peerplays wallet account with GPOS balance

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
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet </b>dApp with a valid username and password</td>
      <td
      style="text-align:left">Should login successfully and display home page/My Funds page</td>
        <td
        style="text-align:left"></td>
          <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">In GPOS Panel, Click on <b>Participate </b>button</td>
      <td style="text-align:left"><b>Peerplays GPOS Wizard</b> will open</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Vote </b>button</td>
      <td style="text-align:left">
        <p>Power Up should be successful and should take user to Vote screen with
          3 tabs :</p>
        <ul>
          <li><b>Proxy</b>
          </li>
          <li><b>Witness</b>
          </li>
          <li><b>Advisors</b>
          </li>
        </ul>
        <p>By default <b>Proxy </b>tab will be selected in Vote screen</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Select the <em><b>Advisors </b></em>tab and verify the information on the
        page.</td>
      <td style="text-align:left">The content for the Advisor tab is loaded and includes the option to add
        a advisor and the list of available advisors on the BlockChain</td>
      <td
      style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Input the valid <em><b>Advisor </b></em>account to the Account Name field
        on the <em><b>Advisors </b></em>screen</td>
      <td style="text-align:left">ADD button will be enabled</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Press on ADD button next to the search Account Name bar</td>
      <td style="text-align:left">
        <p>ADD button adds account from the search result to the <em><b>Advisors </b></em><b>approved by &lt;&lt;user account&gt;&gt;</b>table</p>
        <p>Verify that the Remove button appears next to the added Account&apos;s
          name in the table</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Select the added Account&apos;s name and press on Remove button.
        <br />
        <br />Verify the result.</td>
      <td style="text-align:left">The account is removed as a advisor from the list</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Add a valid <em><b>Advisor </b></em>account again</td>
      <td style="text-align:left"><em><b>Advisor </b></em>details appears under approved advisors list
        <br
        />
        <br />
        <br />
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Reset Changes </b>button</td>
      <td style="text-align:left">Resets unpublished changes</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p>Add valid advisor account to the list, using the Account Name field on
          the <em><b>Advisors </b></em>screen.</p>
        <p>Click on <b>Publish Changes </b>button and verify the result.
          <br />
          <br />
        </p>
      </td>
      <td style="text-align:left">
        <p>Add button adds account from the search result to the <em><b>Advisors </b></em><b>approved by &lt;&lt;user account&gt;&gt;</b>table</p>
        <p>Note down the Votes of added advisor
          <br />
          <br />Clicking on <b>Publish Changes </b>button opens the Transaction confirmation
          window with the transaction fees.</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on Cancel button</td>
      <td style="text-align:left">Closes confirmation window</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Publish Changes </b>button and <b>Confirm </b>the Transaction.</td>
      <td
      style="text-align:left">
        <p>Clicking on <b>Publish Changes </b>button opens the Transaction confirmation
          window with the transaction fees.</p>
        <p>After transaction is confirmed, advisor will appear under <em><b>Advisors </b></em><b>approved by &lt;&lt;user account&gt;&gt;</b>table</p>
        <p>note: If user doesn&apos;t have enough account balance to pay the fee,
          then transaction fails</p>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Finish </b>button</td>
      <td style="text-align:left">&quot;Thank you for Voting&quot; modal/dialog will show up</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Verify the content of the &quot;Thank you for Voting&quot; pop up and
        click on Ok.</td>
      <td style="text-align:left">
        <p>Expected content:</p>
        <p>This is now your blockchain as part of the decentralized autonomous cooperative.
          The value it brings is what you and others bring to it, so go out and</p>
        <ul>
          <li>Share Peerplays with others</li>
          <li>Share your voting decisions with the community, including why you voted
            the way you did</li>
          <li>Visit Peerplays social media and like, share, or retweet our latest posts,
            and provide feedback</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Ok</b> button</td>
      <td style="text-align:left">Dialogue closes and return to Participate Screen</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on Done</td>
      <td style="text-align:left">
        <p>Wallet home page is loaded.</p>
        <p>In GPOS Panel, Verify Voting Performance, Qualified Rewards % and Estimated
          Rake Rewards % is updated</p>
        <p>Voting Performance = Max Rewards</p>
        <p>Qualified Rewards % = 100%</p>
        <p>Estimated Rake Reward % = (user gpos balance/network gpos balance) * 100%</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Wait for the next maintenance interval to pass , navigate to votes modal.</td>
      <td
      style="text-align:left"><em>Verify votes of each of the witnesses and advisors user has voted is equal to current gpos balance</em>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>Perform previous two steps validations in the next sub-periods of current vesting period</b>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
  </tbody>
</table>

## Wallet 1.5 other enhancements

### Display wallet build version 

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
      <td style="text-align:left">Login to <b>PeerPlays Wallet </b>dApp</td>
      <td style="text-align:left">Should login successfully and display home page</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>1.5.4-alpha</b>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"></td>
      <td style="text-align:left">
        <ul>
          <li>version number should be displayed in the middle of menu bar</li>
          <li>Text color is the same as that of the &quot;Settings&quot; text on the
            upper right.</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
      <td style="text-align:left"><b>1.5.4-alpha</b>
      </td>
    </tr>
  </tbody>
</table>### Pending Balances 

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
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Login to <b>PeerPlays Wallet </b>dApp with user account which has <b>pending balance( vesting balances other than GPOS balance) and GPOS balance</b>
      </td>
      <td style="text-align:left">Should login successfully and display home page</td>
      <td style="text-align:left">
        <p><b>Note</b>:only witnesses can see this section. so login with witness
          account</p>
        <ol>
          <li>create an account and make him as witness</li>
          <li>transfer 90% of fund to this account from nathan</li>
        </ol>
      </td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Validate <b>Pending Balances </b> exists</td>
      <td style="text-align:left">
        <p><b>Pending Balances </b>section should exist right below GPOS Panel</p>
        <p>and show Total &amp; Claimable balance</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>claim balance</b> button</td>
      <td style="text-align:left">
        <p>vesting balances table is loaded with vesting balance object with details</p>
        <p>Should not display any gpos vesting balances</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Claim</b> button associated with the vesting balance object</td>
      <td
      style="text-align:left">Transaction confirmation pop up will be loaded</td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Click on <b>Confirm</b>
      </td>
      <td style="text-align:left">Transaction should go through, cliamed/withdrawed balance should reflect
        in the account balance as well as vesting balance</td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Logout and Login with regular account which has some GPOS balance</td>
      <td
      style="text-align:left">
        <p>Should login successfully and display home page</p>
        <p><b>Pending Balances </b>section shouldn&apos;t exist</p>
        </td>
        <td style="text-align:left"></td>
        <td style="text-align:left">Pass</td>
    </tr>
    <tr>
      <td style="text-align:left">Logout and Login with newly created account</td>
      <td style="text-align:left">
        <p>Should login successfully and display home page</p>
        <p><b>Pending Balances </b>section shouldn&apos;t exist</p>
      </td>
      <td style="text-align:left"></td>
      <td style="text-align:left">Pass</td>
    </tr>
  </tbody>
</table>## New Bugs Reported

[https://peerplays.atlassian.net/browse/GPOS-65](https://peerplays.atlassian.net/browse/GPOS-65)

