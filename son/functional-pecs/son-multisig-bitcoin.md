# Functional Specifications - SON Multisig Bitcoin Wallet

## Purpose

The purpose of this document is to outline the steps required to create and change the multisig bitcoin wallet for Peerplays bitcoin sidechain.

## Scope

The functional requirement listed in this document will be limited to the Multisig Bitcoin Wallet \(Primary Wallet\) portion of the SON. This will outline the required steps that will be performed by the Peerplays blockchain to create a multisig bitcoin wallet using the bitcoin signatures of the SONs and changing the signatures in the multisig wallet when required. Also outlined here will be the sequence in which the required steps will be performed including:

* any interactions with the user.
* validations to ensure complete and accurate information gathering.

## Background

The Bitcoin Sidechain functionality has been implemented in the Peerplays blockchain but it doesn't take into account, the change of witnesses. As per the current implementation of Sidechain, a multisig bitcoin wallet will be created on the bitcoin blockchain to hold the bitcoins that have been deposited into the pBTC accounts of the Peerplays users. Every Peerplays witnesses will have a bitcoin transaction signing key for this multisig bitcoin wallet and will be required to sign any withdrawal transaction. When a witness changes, the transaction signing key of the outgoing witness needs to be removed from the multisig bitcoin wallet and the key of the incoming witness needs to be added. The suggested proposal is to make the Sidechain code available as a plugin and assign the responsibility for running the sidechain code to separate nodes called the Sidechain Operating Nodes \(SONs\). The SONs will be independent of the witnesses and don't need to be changed much often.

## Process Overview

Described here is the process to create the mutlisig bitcoin wallet with the SONs signatures and changing the signatures when required.

## Context

In the sidechain implementation, at the beginning of the sidechain fork, a multisig bitcoin wallet called the Primary Wallet is created on the bitcoin blockchain to store the funds transferred by the users to their pBTC accounts. This multisig bitcoin wallet should be created by using the bitcoin public keys of the SONs instead of the public keys of the witnesses. We will also have to use the Hash Time Locked Contracts \(HTLC\) for this address so that if a user transfers the funds to their pBTC accounts and due to some error/downtime, the funds cannot be accepted into the multisig bitcoin address, they should be returned to the user.

The below scenarios related to the multisig bitcoin wallet need to be handled in the implementation:

1. **SON Change**: The SONs may change at any maintenance interval when the votes are tallied and the existing SONs are voted out. Since, the bitcoin public keys of the SONs will be used to create the multisig bitcoin wallet, their public keys will have to be changed in order to operate the multisig bitcoin wallet. But if we change the public keys, a new multisig bitcoin wallet will be created because the multisig bitcoin wallet address is dependant on the public keys. So, we'll have to transfer the funds from the old wallet to the new wallet every time an SON changes which will incur bitcoin transaction fees.

   To reduce this additional cost, we will create an m-of-n multisig bitcoin wallet with signatures of 2/3rd SONs required for a bitcoin transaction. So, we won't need to change the public key of the SON in the multisig bitcoin wallet until 1/3rd of the SONs don't change. Once, 1/3rd of the initial SONs change, we will create a new multisig bitcoin wallet with the public keys of the current SONs and transfer the funds from the previous wallet to the newly created multisig bitcoin wallet.

2. **SON Downtime**: The SONs might stop functioning or go into maintenance. We should provide a mechanism to the SONs to announce any planned maintenance so that the community knows about it. In any case, the maximum continuous downtime allowed for an SON will be 12 hours \(This should be a chain parameter\). If the downtime exceed 12 hours, the SON will be deregistered. During the downtime, the SON will not be able to sign any transactions. If more than 1/3rd SONs are not able to sign the bitcoin transactions, the withdrawal operations can't be completed. That's when the revert operation of the sidechain will come into play and revert the pBTC to the user.

   Similarly, if 50% or more SONs are down, the incoming bitcoin transactions can't be published on the Peerplays blockchain and the funds cannot be accepted. In this scenario, the HTLC contract will kick in and the bitcoins will be returned to the user.

3. **SON Communication Problem**: In case of a communication problem between the all SONs and the witnesses which might be caused due to a DOS attack or for any other reason, the sidechain functionality might come to a standstill for a period of time. In this scenario, any incoming funds into the multisig bitcoin wallet should not be accepted and returned to the original user.

