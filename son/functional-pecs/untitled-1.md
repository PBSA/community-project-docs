# Functional Specifications - SON rewards

## **1. Purpose**

The purpose of this document is to outline the steps required to pay the SONs for their contribution to the Peerplays network.

## **2. Scope**

The functional requirement listed in this document will be limited to the payment portion of the SON. This will outline the required steps to pay the SONs for the functions performed by them on the Peerplays blockchain. Also outlined here will be the sequence in which the required steps will be performed including:

* any interactions with the user.
* validations to ensure complete and accurate information gathering.

## **3. Background**

The Bitcoin Sidechain functionality has been implemented in the Peerplays blockchain but it doesn't take into account, the change of witnesses. As per the current implementation of Sidechain, a multisig bitcoin address will be created on the bitcoin blockchain to hold the bitcoins that have been deposited into the pBTC accounts of the Peerplays users. Every Peerplays witnesses will have a bitcoin transaction signing key for this multisig bitcoin address and will be required to sign any withdrawal transaction. When a witness changes, the transaction signing key of the outgoing witness needs to be removed from the multisig bitcoin address and the key of the incoming witness needs to be added. The suggested proposal is to make the Sidechain code available as a plugin and assign the responsibility for running the sidechain code to separate nodes called the Sidechain Operating Nodes \(SONs\). The SONs will be independent of the witnesses and don't need to be changed much often.

## **4. Process Overview**

Described here is the process to pay the SONs on the Peerplays Blockchain.

## **5. Flow Diagram**

N/A

## **6. Context**

The SON operators will be paid in PPY from the payment pool set up specifically for payments to SONs. This pool will be replenished by depositing a percentage of all the transaction on the Peerplays network. This percentage should be a chain parameter so that it can be changed. The fee will be distributed at the Maintenance intervals based on transactions signed and weight of voting for each SON. Recommended SON payment is 200 PPY daily \( \`SONS\_DAILY\_MAX\_REWARD\`\).

## **7. Requirements**

**7.1 Supported Transaction Types**

1. **Transfer of crypto from Deposit Address to PW Address**
   1. SONs are to be paid for signed transactions, miner fee is also required
2. **Transfer of crypto from old PW Address to New PW Address**
   1. SONs are to be paid for signed transactions, miner fee is also required
3. **Transfer User Issued Asset \(pBTC\) from one account to another**
   1. On-chain transaction. SONs do not sign transactions and do not get paid. Witness fee is applicable

**7.2 Paying Witnesses**

Whenever a witness generates a new block, reward amount must be immediately deposited into witness account's vesting balance.

The amount must be withdrawn from witness\_budget

**7.2 Collecting Fees**

All operations require a fee to be collected and paid to the network

Fee collection is determined by transaction type:

1. Core asset transaction fees are deducted from payer's account
2. UIA \(pBTC\) transaction fees are converted to core asset using base exchange rate \(note: bBTC to BTC is 1:1\)fee mus

In a scenario where user has 0 PPY, fee must be collected from **fee\_pool**.

**7.2 Calculating budget**

The equation for calculating SON budget is as follows:

**current\_supply = current\_supply + \(required\_witness\_budget + required\_worker\_budget + required\_son\_budget - leftover\_worker\_funds - core\_accumulated\_fee - leftover\_witness\_budget - leftover\_son\_budget\)**

**reserve\_supply = max\_supply - current\_supply**

* required\_witness\_budget - required witness budget till next maintenance interval 
* required\_worker\_budget - required worker budget till next maintenance interval 
* required\_son\_budget - reserved SON budget to be paid out in the next maintenance interval = \(chain\_parameters.son\_pay\_max\)
* leftover\_worker\_funds - Remaining funds from previous worker payout
* core\_accumulated\_fee - Accumulated fee \(after all the cuts removed from it\),  since the last maintenance interval.
* leftover\_witness\_budget -  Leftover funds from previous witness budget \( happens if any block is missed in between \)
* leftover\_son\_budget - Leftover funds from previous son budget \( happens if there are no SON transactions on the network \)

other required variables:

* total\_transactons\_per\_day - tracks number of transactions SON participated in
* SONs\_REWARD\_POOL - stores SON reward amounts
* SONS\_DAILY\_MAX\_REWARD - configurable variable which sets maximum size of reward

**7.2 Determining payout**

Payout must be determined by the number of transactions verified by a node. Higher availability nodes participate in more transactions and therefore receive higher payout.

SONs are paid based on % ratio between total\_transactons\_per\_day and SONS\_DAILY\_MAX\_REWARD, where SON's % share of daily transactions determines what % of SONS\_DAILY\_MAX\_REWARD is paid.

Payout must occur once during every 24 hr \(86,400 seconds\) period.

**7.2 Payment Pool**

The rewards-pool must be created along with the creation of the new asset pBTC. Funds must be allotted by the advisors to be paid out as **SONs\_REWARD\_POOL.** The pool is created every year by moving \`NUMBER\_OF\_DAYS\_OF\_THE\_YEAR\` x \`SONS\_DAILY\_MAX\_REWARD\` from the reserve & will be dispersed to SONs proportional to the number of transactions they sign on a particular sidechain. 

SONS\_DAILY\_MAX\_REWARD must initially be set to 200 PPY. We may to have to change this as per market realities etc. Currently BTC is the only supported cryptocurrency.

