# Generate Keypair

The generate keypair option will generate a Public-Private Key pair and display under a group. The keypair generation itself doesn't mean any linking with the Peerplays blockchain. Once the keypair is created, a faucet can be used to create a Peerplays blockchain account with a unique user name \(NAI\). The username will be subject to the Peerplays account creation [guidelines](https://github.com/peerplays-network/peerplays/wiki/Account-Names).

To generate a Scatter keypair:

* Login to the Scatter application
* Navigate to the Settings screen
* Click on "Edit Accounts" in the Peerplays row \(Figure 3.2.1\)

![Figure 3.2.1: Scatter settings screen](../../.gitbook/assets/image%20%2853%29.png)

* Click the + button in the top right of the modal that displays after clicking "Edit Accounts" \(Figure 3.2.2\)

![Figure 3.2.2: Scatter Select account screen](../../.gitbook/assets/image%20%286%29.png)

* On the new screen that appears, click one of the two blue buttons to start the keypair generation process. Each button ties to an individual flow with their own section further down in this document: "Login to Import Peerplays Account": [Section 3.4](https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M1aC-V3ASbUAMy9Wl1b/v/master/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys) "Create New Peerplays Account": [Section 3.3](https://app.gitbook.com/@peerplays/s/community-project-docs/v/master/scatter-peerplays-integration/functional-requirements#3-3-create-peerplays-account)

![Figure 3.2.3: Scatter Peerplays Import account screen](../../.gitbook/assets/screen-shot-2020-03-04-at-11.33.22-am%20%281%29.png)

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

