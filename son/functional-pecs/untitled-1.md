# Functional Specifications - SON rewards

## Purpose

The purpose of this document is to outline the steps required to pay the SONs.

## Scope

The functional requirement listed in this document will be limited to the payment portion of the SON. This will outline the required steps to pay the SONs for the functions performed by them on the Peerplays blockchain. Also outlined here will be the sequence in which the required steps will be performed including:

* any interactions with the user.
* validations to ensure complete and accurate information gathering.

## Background

The Bitcoin Sidechain functionality has been implemented in the Peerplays blockchain but it doesn't take into account, the change of witnesses. As per the current implementation of Sidechain, a multisig bitcoin address will be created on the bitcoin blockchain to hold the bitcoins that have been deposited into the pBTC accounts of the Peerplays users. Every Peerplays witnesses will have a bitcoin transaction signing key for this multisig bitcoin address and will be required to sign any withdrawal transaction. When a witness changes, the transaction signing key of the outgoing witness needs to be removed from the multisig bitcoin address and the key of the incoming witness needs to be added. The suggested proposal is to make the Sidechain code available as a plugin and assign the responsibility for running the sidechain code to separate nodes called the Sidechain Operating Nodes \(SONs\). The SONs will be independent of the witnesses and don't need to be changed much often.

## Process Overview

Described here is the process to pay the SONs on the Peerplays Blockchain.

## Context

The SON operators will be paid in PPY from the payment pool set up specifically for payments to SONs. This pool will be replenished by depositing a percentage of all the transaction on the Peerplays network. This percentage should be a chain parameter so that it can be changed. The fee will be distributed at the Maintenance intervals based on transactions signed and weight of voting for each SON. Recommended SON payment is 200 PPY daily \( \`SONS\_DAILY\_MAX\_REWARD\`\).

## Flow Diagram

![C:\6576f0bc3d3de8c50be5af38593bbd1d](../../.gitbook/assets/0%20%286%29.png)

## **Payment Pool creation and distribution of SON fees**

The SONs must be encouraged to keep their infrastructure up and running at all points in time. SONS\_DAILY\_MAX\_REWARD is initially proposed to be 200 PPY which will be distributed among the participating SONs. This is expected to keep the node operators profitable and thus maintain a healthy network. The rewards which are paid out as son\_fee can be reviewed and rest to reflect market conditions. 

The rewards-pool will be created along with the creation of the new asset pBTC and funds will be allotted by the advisors to be paid out as **SONs\_REWARD\_POOL.** The pool is created every year by moving \`NUMBER\_OF\_DAYS\_OF\_THE\_YEAR\` x \`SONS\_DAILY\_MAX\_REWARD\` from the reserve & will be dispersed to SONs proportional to the number of transactions they sign on a particular sidechain. 

SONS\_DAILY\_MAX\_REWARD = 200 PPY as of now. We may to have to change this as per market realities etc. Also this is ONLY for the Bitcoin side chain at this point.

### SON fee distribution

The SON fees will be paid out promotional to the number of transactions verified by a node. This ensures that the node which is the most available gets higher rewards even if its ranking is lower than others. If a SON confirms 10% of the total\_transactons\_per\_day, then the node will receive, 10 of the SONS\_DAILY\_MAX\_REWARD . The term total\_transaction\_per\_day will vary depending upon the number of transactions. At this point in time, we are considering only Bitcoin to Peerplays transactions \(which is to say, in the future we may bring other chains like Etherium, EOS, Bitshares &  Steem\).

The SON rewards will be paid once in 24 hours \(86,400 seconds\). This to support the calculation of the percentage of reward each SON will receive.

**TODO**: The reserve is controlled by the advisors. So the mechanism \(commands\) to submit the above proposal and move funds to the SON pool must be identified, documented and tested

