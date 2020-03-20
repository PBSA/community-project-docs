# Functional Specifications - Bitcoin Withdrawal

## 1. Purpose

The purpose of this document is to outline functional specifications for monitoring bitcoin network and handling withdrawals. Result of a withdrawal is conversion of peerplay assets \(pBTC\) to Bitcoin \(BTC\) using 1:1 ratio.

## 2. Scope

Sidechain operating node will monitor Bitcoin network for events of interest, namely transfer of assets to a Peerplays address. When transfer happens, sidechain will process it, in order to pick up information needed to handle it. Handling withdrawals will create certain amount of tokens on a Peerplays network. This amount will match the amount of assets on target sidechain by predefined exchange rate.

Specific functions covered include:

* monitor transactions to a designated sidechain user address
* handle withdrawal via creation of sidechain event data
* create & confirm object proposals
* conversion of BTC to pBTC based on defined exchange rate, with applicable fees
* sign transactions
* withdraw bitcoin for conversion into peerplay tokens

## 3. Background

Withdrawal handling will consist of listener and handler functionality. Listener can identify and report new block, a transaction, or filtered single event \(like specific operation involving specific address\). Handlers will process the event identified by listener.

We have identified three \(3\) distinct scenarios describing how deposits and withdrawals may be implemented. Scenarios are outlined in this article:

[Comparison between scenarios for handling deposits and withdrawals](file:///C:/wiki/spaces/PIX/pages/358187009/Comparison+between+scenarios+for+handling+deposits+and+withdrawals)

Requirements below are describing functional specifications based on Scenario 1 - Multisignature primary wallet controlled by SON network, holding all the funds. All transfers are made to and from this multisignature wallet.

## 4. Process Overview

Described here is the process of monitoring withdrawal address and processing transactions that occur in relation to target address.

pBTC token issue is initiated by Sidechain Listener identifying a Bitcoin withdrawal, passing information to Sidechain Handler .

Steps involved:

1. User initiates withdrawal to convert pBTC to BTC
2. Listener identifies withdrawal type change in the block chain
3. Listener passes event notification to sidechain handler
4. Handler receives event data and creates a withdrawal descriptor object
5. Proposal is blind approved
6. Withdrawal is checked against active SONs
7. Withdrawal whose event data finds a match in other active sidechains is approved. Otherwise, withdrawal is rejected
8. pBTC is converted to BTC using 1:1 rate
9. Amount is sent from primary wallet \(Bitcoin multisig address controlled by active SONs\) to the a Bitcoin address which is registered as a sidechain user address for withdrawals
10. Transaction is signed and sent to bitcoin node
11. User receives BTC amount
12. Withdrawal is marked as processed

## 5. Context

To facilitate conversion of peerplays tokens into bitcoin, SON must include an event listener and an event handler mechanisms to identify specific types of transactions and handle them accordingly. Proposed approach uses multisignature Primary Wallet controlled by SON network, holding all the funds. All transfers are made to and from this multisignature wallet.

## 6. Flow Diagram

\[TBD\]

## 7. Requirements

Refer to [Functional Specification - Bitcoin Deposit Handling](file:///C:/wiki/spaces/PIX/pages/591921180/Functional+Specification+-+Bitcoin+Deposit+Handling) for wallet information

### 7.1 Listener

SON must include a Bitcoin event listener which monitors a designated Bitcoin address registered as a sidechain user address for withdrawals Specifically, listener uses Bitcoin node interface for monitoring changes in the block changes.

Listener must be able to recognize a change that signifies a withdrawal event and capture the following data associated with each transaction of this type:

* Transaction unique identifier
* Transfer operation’s source address
* Transfer operation’s target address
* Transfer amount

### 7.3 Handler

SON must include a Bitcoin event handler which uses information supplied by the Listener to perform a specific operation that’s based on transaction type submitted by listener. When handler receives notification of Withdrawal transaction from the Listener, **sidechain\_event\_data** must be received and passed to **sidechain\_event\_data\_received**. Received sidechain event data must then be used to create proposal for a withdrawal descriptor object **son\_wallet\_withdrawal\_object**.

\[Q1: How does proposal get approved. A1: Current design does blind approve on all proposals \]

\[Q2: Can proposals get rejected and what happens. A2: Transaction is verified against active SONs and is rejected if information does not match. **list\_active\_sons** is used to determine active SONs to verify against \]

* Approved withdrawals must be checked against SON network to determine if withdrawal using same sidechain event data has been created. System must check the following data for matches: **peerplays\_transaction\_id; chain::account\_id\_type peerplays\_from; chain::asset peerplays\_asset;**

If a match is found, withdrawal is confirmed. If a match is not found, new withdrawal descriptor object must be created.

SON must start conversion of withdrawal amount from peerplay tokens into Bitcoin following withdrawal confirmation. Conversion operation must calculate pBTC to BTC conversion using 1:1 rate. Conversion is completed by sending funds from bitcoin address \(sidechain user address for withdrawals\) to primary wallet \(bitcoin multisig address\). Upon completion, bitcoin transaction must be signed and sent to bitcoin node. User will receive bitcoin corresponding to amount of converted pBTC. Lastly, scheduled SON must mark **son\_wallet\_withdrawal\_object** as processed

## 8. Glossary

**pBTC**​ is a peerplay Blockchain Asset, which represents users’ balances in Bitcoin on PeerPlays blockchain. Having a balance of 1 pBTC would mean having it backed by the same amount of Bitcoin on a Witness-controlled Multisig Wallet. New pBTC are NOT ISSUED by OWNER with ​issue ​operation. New pBTC are issued strictly in relation with ​Deposit​ operations.

**PW** \(**Primary Wallet**\) ​is the main Multisig Bitcoin Wallet.

**Multisignature \(multisig\)** refers to requiring more than one key to authorize a Bitcoin transaction. It is generally used to divide up responsibility for possession of bitcoins.

## Related Documentation

[SON status overview 2020-03-11](file:///C:/wiki/spaces/PIX/pages/535592965/SON+status+overview+2020-03-11)

[Comparison between scenarios for handling deposits and withdrawals](file:///C:/wiki/spaces/PIX/pages/358187009/Comparison+between+scenarios+for+handling+deposits+and+withdrawals)

[Bitcoin Withdrawal Handling LLD](file:///C:/wiki/spaces/PIX/pages/352124984/Bitcoin+Withdrawal+Handling+LLD)

