---
description: Low Level Design Specification (LLD)
---

# Low Level

## Peerplays

### Account

A Peerplays account exists on the Peerplays blockchain and is registered via a faucet which handles requests from a dapp. There are some requirements that must be met when registering a new Peerplays account which can be seen [here](https://github.com/peerplays-network/peerplays/wiki/Account-Names).

### Keys

The Peerplays blockchain makes use of three keys to perform various actions: owner, active, and memo. Every account that is created on the Peerplays blockchain will have these keys generated from the account credentials they provide. 

#### Owner

The owner key is the highest authority key for an account.

#### Active

The active key is the most used key of the three. This key is used to sign any transaction that is generated for a standard user account before being sent to the blockchain.

#### Memo

The memo key is used to encrypt messages sent with a balance transfer. Only the sender and the intended receiver can decrypt a memo. 

## Scatter

### Keypair

\*\*\*\*

## **Scatter + Peerplays**

### **Scatter Keypair Generation**

#### Details of how a Peerplays keypair is generated programmatically within Scatter:

Due to restrictions place upon the Scatter Keypair object that contains the private Wallet Import Format \(WIF\) and public key string, the Peerplays plugin cannot use typical keys. Reason number one for this is that the Peerplays blockchain operates with various authorization levels that are attached to various keys. 

As an example, user "login" on the Peerplays Core GUI wallet is done by comparing a client-side generated active public key with a blockchain retrieved active public key. However, there are instances where we need to also compare a public owner key due to an event where _some_ Peerplays accounts were created with their owner and active keys swapped.

As another example, to send a transfer of funds on the Peerplays blockchain, you are required to have both the active private key and the memo private key. 

To circumvent the requirement for multiple keys but only the ability to store one private key, and its public key counterpart, the Peerplays Scatter plugin will encode all three keys into a single new "master" key for exclusive use within Scatter. The result will be a Scatter Keypair with the following format:

```text
Keypair = {
  privateKey: 'encodedWifKeysHere`,
  publicKeys: [{
    key: 'activePublicKeyHere',
    blockchain: 'ppy'
  }]
}
```

`Keypair.privateKey` contains all three authority level keys in WIF for a Peerplays account \(owner, active, memo\) in an encoded format using `hex` :`Buffer.from('stringtexthere').toString('hex')`

This encoding method essentially cuts the resulting string size in half. This format is required as the Scatter wallet will not encrypt the `Keypair.privateKey` if its length is greater than 100 characters.

`Keypair.publicKeys[0].key` is the active public key which is just a required item for a Scatter wallet Keypair object.

