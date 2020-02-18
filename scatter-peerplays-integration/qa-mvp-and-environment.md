---
description: >-
  This document outlines the Quality Assurance Minimum Viable Product and
  Environment
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

The Scatter project\(s\) are numerous and only specific ones are required in order to test/develop a plugin. In light of recent conversations, the ScatterBridge project is to be favoured over the ScatterEmbed.

For adequate testing of the Peerplays Scatter plugin, three code bases are required to be compiled:

1. [walletpack](https://github.com/GetScatter/walletpack)
2. [Bridge](https://github.com/GetScatter/Bridge)
3. [ScatterDesktop](https://github.com/GetScatter/ScatterDesktop)

ScatterBridge will point to a local location of walletpack until it has been published on NPM.

### Instruction for Compiling

Justin: add specifics to compiling the application correctly below \(branches, node version, npm version, code changes, etc.\)

#### walletpack

1. switch branch to `peerplays-plugin`
2. open `package.json`
3. change &lt;package&gt; to &lt;package&gt;
4. install node packages: `npm i`
5. etc.

#### Bridge

1. 
#### ScatterDesktop

1. 
{% endtab %}
{% endtabs %}

