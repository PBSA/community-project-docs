---
description: >-
  This document outlines the Quality Assurance (QA) Minimum Viable Product (MVP)
  and Environment needed for QA to operate.
---

# QA MVP and Environment

The Quality Assurance team will be testing the Scatter Peerplays plugin via a hosted develop-mode environment. This is due to lack of various pieces of information on how to produce the binaries for the various Scatter code bases \(several are needed to produce a single binary under certain conditions\). As such, the MVP will not be the MVP for Scatter as a whole but rather, just for the Peerplays plugin itself with two accompanying custom forms.

Click on the header to view the content you desire.

{% tabs %}
{% tab title="MVP" %}
All functional requirements are implemented as per documentation with accommodation for the following:

* lack of Font Awesome Pro, there will several missing icons throughout the application the QA team will be working with
  * some code changes are required to allow the application to compile without it
{% endtab %}

{% tab title="Environment" %}
### What to Compile

The Scatter project\(s\) are numerous and only specific ones are required in order to test/develop a plugin. In light of recent conversations, the ScatterBridge project is to be favoured over the ScatterEmbed one.

For adequate testing of the Peerplays Scatter plugin, three codebases are required to be compiled:

1. [walletpack](https://github.com/GetScatter/walletpack)
2. [Bridge](https://github.com/GetScatter/Bridge)
3. [ScatterDesktop](https://github.com/GetScatter/ScatterDesktop)

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
3. create a new `peerplays` directory inside `node_modules > @walletpack`
4. **copy** the output files within the `dist` directory within `packages > peerplays > dist` **\(**in the walletpack repository\) into `node_modules > @walletpack > peerplays`
5. **copy** the other required files from the wallet pack repository into `node_modules > @walletpack > peerplays`: - prepare.js - README.md - package.json
6. install node packages within the directory you just finished copying files into \(`node_modules > @walletpack > peerplays`\): `npm i`
7. **copy** the `.env.example` root file contents to a new root file called `.env` 
8. edit the `VUE_APP_NO_WALLET` parameter in root file `.env` : `VUE_APP_NO_WALLET=1`
9. run the application in dev mode with `npm run start`
10. you can view the application in a chrome web browser at this location for the host machine: [http://localhost:8081/](http://localhost:8081/)

#### **ScatterDesktop \(electron, encryption\)**

No Electron binary production method provided and this process appears to still be under development based on GitHub repository activity. So, only the local development method outlined above is available at this time.
{% endtab %}
{% endtabs %}

