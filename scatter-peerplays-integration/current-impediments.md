# Current Impediments

## Imports not working as expected.

At the moment, attempting to use ScatterDesktop in conjunction with the UI \(Bridge\) leads to an issue. `VUE_APP_NO_WALLET=` should be set within the `.env` file in the Bridge directory. Some libraries do not import properly into the wallet container. This is most noticeable within the Peerplays plugin `signer()` ****function. At the moment, this issue is a roadblock for transfer. Once this issue is resolved, the transfer flow should be looked at again and tweaked to work with any changes that might be made. This is an issue I faced locally in my environment but may not be consistent across all setups.

## Seed issue.

Using ScatterDesktop with the UI \(ScatterBridge\) leads to an issue in which the seed used for decryption is incorrect. The seed should be a value derived from the user's Scatter password, but is observed to be the boolean value `true`. This is an issue I faced locally in my environment but may not be consistent across all setups.



