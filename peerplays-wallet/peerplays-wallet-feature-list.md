# Peerplays wallet feature list

## Traceability

This section will provide a list of related documents, Peerplays GUI wallet releases etc

* [Wallet v1.5 - Design & Requirements Document](https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/341475470)
* [Informal Supporting Documentation/Research](https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/319160332)

### Features

<table>
  <thead>
    <tr>
      <th style="text-align:center"><b>Feature ID</b>
      </th>
      <th style="text-align:left"><b>Short Descriptions</b>
      </th>
      <th style="text-align:left"><b>short comments</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">PW001</td>
      <td style="text-align:left">Claim ICO tokens (pre-login &amp; post-login)</td>
      <td style="text-align:left">Functionality not verified</td>
    </tr>
    <tr>
      <td style="text-align:center">PW002</td>
      <td style="text-align:left">Create Peerplays Account</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:center">PW003</td>
      <td style="text-align:left">Login to Peerplays GUI Wallet</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:center">PW004</td>
      <td style="text-align:left">Balance Claims</td>
      <td style="text-align:left">Under Settings if logged in else, can be accessed from login screen</td>
    </tr>
    <tr>
      <td style="text-align:center">PW005</td>
      <td style="text-align:left">Send funds from a user specified currency</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:center">PW006</td>
      <td style="text-align:left">Assigning a Proxy to for votes</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:center">PW007</td>
      <td style="text-align:left">Voting for Witnesses</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:center">PW008</td>
      <td style="text-align:left">Voting for Advisors/Committee members</td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:center">PW009</td>
      <td style="text-align:left">Show the logged in users&apos; recent actions/transactions</td>
      <td style="text-align:left">Filters: Transactions, Tournaments</td>
    </tr>
    <tr>
      <td style="text-align:center">PW010</td>
      <td style="text-align:left">Show the logged in users&apos; balances</td>
      <td style="text-align:left">Core, UIA&#x2019;s, other cryptos (SON&#x2019;s)</td>
    </tr>
    <tr>
      <td style="text-align:center">PW011</td>
      <td style="text-align:left">Help/FAQ</td>
      <td style="text-align:left">Thorough Help section viewable within a modal that covers our terminology</td>
    </tr>
    <tr>
      <td style="text-align:center">PW012</td>
      <td style="text-align:left">Notices</td>
      <td style="text-align:left">When configured, can post notices to all wallet users using memo/transfer
        system.</td>
    </tr>
    <tr>
      <td style="text-align:center">PW013</td>
      <td style="text-align:left">
        <p>Simple Explorer</p>
        <ul>
          <li>current block number</li>
          <li>last block generation time</li>
          <li>transactions per second</li>
          <li>average confirmation time</li>
          <li>active witnesses</li>
          <li>active committee/advisors</li>
          <li>transaction per block</li>
          <li>recently missed blocks</li>
          <li>current supply of core token</li>
          <li>stealth supply</li>
          <li>graphs
            <ul>
              <li>block times</li>
              <li>transactions per block</li>
            </ul>
          </li>
          <li>recent activity table
            <ul>
              <li>all user recent activity</li>
            </ul>
          </li>
          <li>recent blocks table
            <ul>
              <li>block id, date, witness, transaction count</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:center">PW014</td>
      <td style="text-align:left">
        <p>Account lookup</p>
        <ul>
          <li>table results headers
            <ul>
              <li>account name (string username)</li>
              <li>id (1.2.xx)</li>
              <li>core token balance</li>
              <li>percent of total core token supply</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li>account username search (&apos;mcs2&apos;)</li>
          <li>id (&apos;1.2.21&apos;) string search not supported</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center">PW015</td>
      <td style="text-align:left">
        <p>Fee schedule</p>
        <ul>
          <li>show Peerplays blockchain fees</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:center">PW016</td>
      <td style="text-align:left">
        <p>Logged in user GPOS info display (GPOS Panel)</p>
        <ul>
          <li>GPOS Balance</li>
          <li>Voting Performance (depends on qualified reward %)</li>
          <li>Qualified Reward % (vesting_factor)</li>
          <li>Estimated Rake Reward %</li>
        </ul>
      </td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:center">PW017</td>
      <td style="text-align:left">
        <p>GPOS Participation Mechanism</p>
        <ul>
          <li>Participate/GetStarted from dashboard</li>
        </ul>
      </td>
      <td style="text-align:left">
        <ul>
          <li>starts the procedure for creating/withdrawing a gpos type vesting balance</li>
          <li>is how voting system is accessed</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center">PW018</td>
      <td style="text-align:left">
        <p>GPOS Power Up</p>
        <ul>
          <li>display of current users total GPOS balance</li>
          <li>display of current users new GPOS balance based on form data (provided
            form submission succeeds)</li>
        </ul>
      </td>
      <td style="text-align:left">vesting_balance_create</td>
    </tr>
    <tr>
      <td style="text-align:center">PW019</td>
      <td style="text-align:left">
        <p>GPOS Power Down</p>
        <ul>
          <li>display of available GPOS that the current user can currently be withdraw</li>
          <li>display of total GPOS that the current user has</li>
          <li>display of current users new GPOS balance based on form data (provided
            form submission succeeds)</li>
        </ul>
      </td>
      <td style="text-align:left">vesting_balance_withdraw</td>
    </tr>
    <tr>
      <td style="text-align:center">PW020</td>
      <td style="text-align:left">Manual transaction signing</td>
      <td style="text-align:left">Requires wallet to be unlocked by the user to providing their login password</td>
    </tr>
    <tr>
      <td style="text-align:center">PW021</td>
      <td style="text-align:left">Automatic transaction signing</td>
      <td style="text-align:left">
        <p>On login, required data is generated from login form value to allow background
          transaction signing</p>
        <ul>
          <li>ultimately, background wallet unlock</li>
          <li>used for GPOS power up/down</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:center">PW022</td>
      <td style="text-align:left">peerplaysjs-lib integration to allow communication with the blockchain</td>
      <td
      style="text-align:left">
        <p>Initiates the connection using websocket technologies on application launch.</p>
        <ul>
          <li>several other items included that make the wallet work from the lib</li>
        </ul>
        </td>
    </tr>
  </tbody>
</table>



