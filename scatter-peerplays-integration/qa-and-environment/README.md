---
description: >-
  This document outlines the Quality Assurance (QA) scope and Environment needed
  for QA to operate.
---

# QA

The Quality Assurance team will be testing the Scatter Peerplays plugin via a hosted develop-mode environment. This is due to lack of various pieces of information on how to produce the binaries for the various Scatter code bases \(several are needed to produce a single binary under certain conditions\). As such, the MVP will not be the MVP for Scatter as a whole but rather, just for the Peerplays plugin itself with two accompanying custom forms.

Click on the header to view the content you desire.

{% tabs %}
{% tab title="Scope" %}
A refer to the [Functional Requirements](https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M23Hq7zBNFDpF_nvv14/scatter-peerplays-integration/functional-requirements) for details of testing.

* Connect to Peerplays blockchain
  * connection is passive
  * no UI errors should appear related to connections within a Scatter account settings page
* Generate keypair
  * passive, verified with successful:
    * Peerplays account login
    * Peerplays account registration
* Create Peerplays account
  * no errors and Peerplays account can be seen as "imported" if it appears in Scatter account settings page &gt; Peerplays &gt; edit accounts
* Import Peerplays Keys
  * see "Create Peerplays account" above
* Support for PPY asset
  * PPY logo can be seen \(functional requirements needs update to indicate which image\)
* Retrieve PPY Balance
  * Peerplays account balance can be seen
    * must have imported a Peerplays account first
* Send PPY
* Receive PPY
  * see "Retrieve PPY Balance" above
{% endtab %}

{% tab title="Environment" %}
### What to Compile

The Scatter project\(s\) are numerous and only specific ones are required in order to test/develop a plugin. In light of recent conversations, the ScatterBridge project is to be favoured over the ScatterEmbed one.

For adequate testing of the Peerplays Scatter plugin, three codebases are required to be compiled:

1. [walletpack](https://github.com/GetScatter/walletpack)
2. [Bridge](https://github.com/GetScatter/Bridge)
3. ~~~~[ScatterDesktop](https://github.com/GetScatter/ScatterDesktop)

ScatterBridge will point to a local location of walletpack until it has been published on NPM.

### Instruction for Compiling

Justin: add specifics to compiling the application correctly below \(branches, node version, npm version, code changes, etc.\)

#### walletpack \(plugins\)

Node Version: `10.15.3`

1. switch branch to `peerplays-plugin`
2. install node packages: `npm i`
3. create the production files of the peerplays plugin with `npm run build` in the root

#### Bridge \(UI\)

Node Version: `10.15.3`

1. switch branch to `peerplays-support`
2. install node packages: `npm i`
3. create a new `peerplays` directory inside `node_modules > @walletpack` with another child directory called `dist`
4. **copy** the output files within the `dist` directory within `packages > peerplays > dist` **\(**in the walletpack repository\) into `node_modules > @walletpack > peerplays > dist`
5. **copy** the other required files from the wallet pack repository into `node_modules > @walletpack > peerplays`: - prepare.js - README.md - package.json
6. **replace** the files within `node_modules > @walletpack > core` with the `dist` directory files from the walletpack project: `// 1. delete the existing one to ensure it gets replaced rm -rf node_modules/@walletpack/core` `// 2. recursive copy to new location cp -R ../getscatter-walletpack/packages/core/dist/ ./node_modules/@walletpack/core/`
7. Your new `peerplays` directory within the Bridge project inside `node_modules > @walletpack` should now look like this: `node_modules --- @walletpack ------ bitcoin ------ core ------ eosio ------ ethereum ------ peerplays --------- dist ------------ _PPY.js ------------ peerplays.js ------------ PPYKeypairService.js --------- package.json --------- prepare.js --------- README.md`
8. install node packages within the directory you just finished copying files into \(`node_modules > @walletpack > peerplays`\): `npm i`
9. **rename** the `.env.example` root file to `.env` 
10. edit the `VUE_APP_NO_WALLET` parameter in root file `.env` : `VUE_APP_NO_WALLET=1`
11. run the application in dev mode with `npm run start`
12. you can view the application in a chrome web browser at this location for the host machine: [http://localhost:8081/](http://localhost:8081/)

#### **ScatterDesktop \(electron, encryption\)**

~~No Electron binary production method provided and this process appears to still be under development based on GitHub repository activity. So, only the local development method outlined above is available at this time.~~  
Recent communications reveal that we required production environment emulation and thus requires pipelines for Electron compilation.

Node Version: `10.15.3`

1. Install node packages: `yarn install` \(README.md file recommends using yarn on this repository\)
2. Uncomment the first line in the `.env` file in the root:`LOCAL_TESTING=http://localhost:8081/` 

{% hint style="warning" %}
Before continuing, ensure you have completed the above two sections \(walletpack & Bridge\).
{% endhint %}

1. Inside the Bridge project, update an entry within the `.env` file; `VUE_APP_NO_WALLET=` should be the new line text \(remove the `1` you added earlier\)
{% endtab %}
{% endtabs %}



