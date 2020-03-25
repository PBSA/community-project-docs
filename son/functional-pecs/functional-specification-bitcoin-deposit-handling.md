# Functional Specification - Bitcoin Deposit Handling

## 1. Purpose

The purpose of this document is to outline functional specifications for monitoring bitcoin network and handling deposits. Result of a deposit is conversion of Bitcoin \(BTC\) to peerplay assets \(pBTC\).

## 2. Scope

Sidechain operating node will monitor Bitcoin network for events of interest, namely transfer of assets to a Peerplays address. When transfer happens, sidechain will process it, in order to pick up information needed to handle it. Handling deposits will create certain amount of tokens on a Peerplays network. This amount will match the amount of assets on target sidechain by predefined exchange rate.

Specific functions covered include:

* monitor transactions to a designated sidechain user address
* handle deposit via creation of sidechain event data
* create & confirm object proposals
* conversion of BTC to pBTC based on defined exchange rate, with applicable fees
* sign transactions
* withdraw bitcoin for conversion into peerplay tokens

## 3. Background

NOTE: Deposit handling requirements are not final.

Deposit handling will consist of two parts, a BTC Event Listener and a BTC Event Handler. Listener can identify and report new block, a transaction, or filtered single event \(like specific operation involving specific address\). We have identified three \(3\) distinct scenarios describing how deposits and withdrawals may be implemented. Scenarios are outlined in this article:

[Comparison between scenarios for handling deposits and withdrawals](file:///C:/wiki/spaces/PIX/pages/358187009/Comparison+between+scenarios+for+handling+deposits+and+withdrawals)

Requirements below are describing functional specifications based on Scenario 1 - Multisignature primary wallet controlled by SON network, holding all the funds. All transfers are made to and from this multisignature wallet.

## 4. Process Overview

Described here is the process of monitoring deposit address and processing transactions that occur in relation to target address.

pBTC token issue is initiated by Sidechain Listener identifying a Bitcoin deposit, passing information to Sidechain Handler .

Steps involved:

1. User initiates deposit to convert BTC to pBTC
2. Listener identifies deposit type change in the block chain
3. Listener passes event data to handler
4. Handler receives event data and creates a deposit descriptor object
5. Proposal is blind approved
6. Deposit is checked against active SONs
7. Deposits whose event data finds a match in other active sidechains is approved. Otherwise, deposit is rejected
8. BTC is converted to pBTC using 1:1 rate
9. Bitcoin amount is sent from bitcoin address \(sidechain user address for deposits\) to primary wallet \(bitcoin multisig address\)
10. Transaction is signed and sent to bitcoin node
11. User receives pBTC amount
12. Deposit is marked as processed

## 5. Context

To facilitate conversion of bitcoin in to peerplays tokens, SON must include an event listener and an event handler mechanism to identify specific types of transactions and handle them accordingly. Proposed approach uses multisignature Primary Wallet controlled by SON network, holding all the funds. All transfers are made to and from this multisignature wallet.

## 6. Flow Diagram

\[TBD\]

## 7. Requirements

### 7.1 Wallet information

SON must be able to create/update Peerplays multisig account, and create/re-create Bitcoin multisig address controlled by active SONs.

The SONs may change at any maintenance interval when the votes are tallied and the existing SONs are voted out. Since, the bitcoin public keys of the SONs will be used to create the multisig bitcoin wallet, their public keys will have to be changed in order to operate the multisig bitcoin wallet. System must transfer the funds from the old wallet to the new wallet every time an SON changes and incur associated bitcoin transaction fees.

To reduce this additional cost, an m-of-n multisig bitcoin wallet will be created with signatures of 2/3rd SONs required for a bitcoin transaction. Change of public key for the SON in the multisig bitcoin wallet is not needed until 1/3rd of the SONs changes. Once, 1/3rd of the initial SONs changes, we must create a new multisig bitcoin wallet with the public keys of the current SONs and transfer the funds from the previous wallet to the newly created multisig bitcoin wallet.

Requirements below assume use of multisignature primary wallet controlled by SON network, holding all the funds. All transfers are made to and from this multisignature wallet.

SON must be able to keep thie history records of active primary wallets, duration of activity period, and the SOns who control the wall at the time of creation.

### 7.2 Listener

SON must include a Bitcoin event listener which monitors a designated Bitcoin address registered as a sidechain user address for deposits. Specifically, listener uses Bitcoin node interface for monitoring changes in the block changes.

Listener must be able to recognize a change that signifies a deposit event and capture the following data associated with each transaction of this type:

* Transaction unique identifier
* Transfer operation’s source address
* Transfer operation’s target address
* Transfer amount
* Transaction fee \(for transfer operation\)

### 7.3 Handler

SON must include a Bitcoin event handler which uses information supplied by the Listener to perform a specific operation that’s based on transaction type submitted by listener. When handler receives notification of Deposit transaction from the Listener, **sidechain\_event\_data** must be received and passed to **sidechain\_event\_data\_received**. Received sidechain event data must then be used to create proposal for a deposit descriptor object **son\_wallet\_deposit\_object**.

\[Q1: How does proposal get approved. A1: Current design does blind approve on all proposals \]

\[Q2: Can proposals get rejected and what happens. A2: Transaction is verified against active SONs and is rejected if information does not match. **list\_active\_sons** is used to determine active SONs to verify against \]

* Approved deposits must be checked against SON network to determine if deposit using same sidechain event data has been created. System must check the following data for matches: **std::string sidechain\_transaction\_id; std::string sidechain\_from; std::string sidechain\_to; std::string sidechain\_currency; safe&lt;int64\_t&gt; sidechain\_amount;**

If a match is found, deposit is confirmed. If a match is not found, new deposit descriptor object must be created.

SON must start conversion of deposit amount from bitcoin into peerplay tokens following deposit confirmation. Conversion operation must calculate btc to ppy conversion using 1:1 rate. Conversion is completed by sending funds from bitcoin address \(sidechain user address for deposits\) to primary wallet \(bitcoin multisig address\). Upon completion, bitcoin transaction must be signed and sent to bitcoin node. User will receive peerplays core assets matching the amount of depoisted bitcoin. Lastly, scheduled SON must mark **son\_wallet\_deposit\_object** as processed

### CLI Examples:

sending 100 BTC to deposit address:

`bitcoin-core.cli -rpcuser=1 -rpcpassword=1 -rpcwallet= sendtoaddress 2NDN7cDH3E57E1B8TwTYvBgF7CndL4FTBPL 100;`

cli wallet command:

`transfer sonaccount01 son-account 100 TEST "" true`

## 8. Glossary

**pBTC**​ is a peerplay Blockchain Asset, which represents users’ balances in Bitcoin on PeerPlays blockchain. Having a balance of 1 pBTC would mean having it backed by the same amount of Bitcoin on a Witness-controlled Multisig Wallet. New pBTC are NOT ISSUED by OWNER with ​issue ​operation. New pBTC are issued strictly in relation with ​Deposit​ operations.

**PW** \(**Primary Wallet**\) ​is the main Multisig Bitcoin Wallet.

**Multisignature \(multisig\)** refers to requiring more than one key to authorize a Bitcoin transaction. It is generally used to divide up responsibility for possession of bitcoins.

## Related Documentation

[SON status overview 2020-03-11](file:///C:/wiki/spaces/PIX/pages/535592965/SON+status+overview+2020-03-11)

[Comparison between scenarios for handling deposits and withdrawals](file:///C:/wiki/spaces/PIX/pages/358187009/Comparison+between+scenarios+for+handling+deposits+and+withdrawals)

