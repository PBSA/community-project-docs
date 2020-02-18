---
description: Functional requirements for the Scatter Peerplays plugin.
---

# Functional Requirements

## 1.0 Introduction

### 1.1 Objective

### 1.2 Scope

The scope is defined in the [project scope document](project-scope.md).

### 1.3 Assumptions and Constraints



This document will provide a tabular listing of the Peerplays Scatter Wallet Integration features. The target features for the Scatter Wallet Peerplays plugin will be based on this document. The features that Peerplays Scatter integration will provide is going to be a sub-set of the P[eerplays Wallet Features](https://app.gitbook.com/@peerplays/s/community-project-docs/peerplays-wallet/peerplays-wallet-feature-list).

## **2.0 High Level Requirements**

| Requirement | User Story |
| :--- | :--- |
| Connect to Peerplays blockchain | As a user I should be able to connect to the Peerplays main net. |
| Generate keypair | As a user I should be able to generate a Peerplays keypair. |
| Create Peerplays account | The user must be directed to a faucet to create the peerplays account |
| Import Peerplays Keys | A Given Peerplays private key should be imported by Scatter wallet |
| Support for PPY asset | As a user I should have PPY asset support within the Scatter wallet. |
| Retrieve PPY Balance | As a user I should be able to see my PPY balance within the Scatter wallet. |
| Send PPY | As a user I should be able to send PPY via the Scatter wallet. |
| Receive PPY | As a user I should be able to receive PPY via the Scatter wallet. |

## 3.0 Functional Requirements

This section will provide detailed description, mockups/wireframes/screenshots of requirements provided in section 2. The Quality assurance team will prepare the test plan based on this section.

### 3.1 Connect to Peerplays blockchain:

![The list of networks can be added and removed here.](../.gitbook/assets/image%20%2821%29.png)

### 3.2 Generate Keypair

The generate keypair option will generate a Public-Private Key pair and display under a group. The keypair generation itself doesn't mean any linking with the Peerplays blockchain. Once the keypair is created, a faucet can be used to create a Peerplays blockchain account with a unique user name \(NAI\). The username will be subject to the Peerplays account creation [guidelines](https://github.com/peerplays-network/peerplays/wiki/Account-Names).

![Screen 1](../.gitbook/assets/image%20%289%29.png)

![Screen 2](../.gitbook/assets/image%20%2832%29.png)

### 3.3 Create Peerplays Account

By default, a new Scatter user will not have any Peerplays accounts/keys associated with their Scatter account. In this use-case, the Scatter user either does not have a Peerplays account at all \(will need to make one\) or wishes to create a new one and then import the keys \([3.4](https://app.gitbook.com/@peerplays/s/community-project-docs/scatter-peerplays-integration/functional-requirements#3-4-import-peerplays-keys)\) into their Scatter account.

We will assume that the end-user has already created a Scatter account and is logged into their Scatter wallet with said account.

![Figure 3.3.1: Logged in Scatter user screen](../.gitbook/assets/image%20%2829%29.png)

The first course of action to create a Peerplays account is to click the cog wheel icon in the top right of the ScatterBridge user interface \(UI\).

![Figure 3.3.2: Scatter settings screen](../.gitbook/assets/image%20%2824%29.png)

From the Scatter settings screen, the Scatter user must then click the "ACCOUNTS" tab header.

![Figure 3.3.3: Scatter Accounts setting screen](../.gitbook/assets/image%20%2814%29.png)

If the Peerplays section is greyed out, click the switch to enable Peerplays account\(s\). From this screen, the Scatter user will have to click "Edit Accounts" beside the blockchain they want to alter/add an account to: Peerplays in this case.

![Figure 3.3.4: Edit Accounts screen](../.gitbook/assets/image.png)

A new Scatter user account should see no keys here when they go to create a Peerplays account. From this screen, the Scatter user will have to click the plus icon blue button in the top right of the foremost visible window.

![Figure 3.3.5: Pick Import Method](../.gitbook/assets/image%20%2831%29.png)

On the new modal that appears, we see the first **new** screen required to be added. This modal is based on the original but we show three buttons instead:

#### "Create New Peerplays Account"

![Figure 3.3.9: Create New Peerplays Account \[empty\]](../.gitbook/assets/image%20%282%29.png)

![Figure 3.3.10: Create New Peerplays Account \[filled - errors\]](../.gitbook/assets/image%20%285%29.png)

![Figure 3.3.11: Create New Peerplays Account \[filled\]](../.gitbook/assets/image%20%2812%29.png)

Peerplays account creation will have a similar process as it does on any other Peerplays dapp:

* username field
* code generated password read-only field
* password re-entry field
* download recovery file button
* form submit/create button

However, there are some rules and conditions to this form:

**Errors**

If any form component has an error, their appearance will change to match that of Figure 3.3.10.

**"Account Name" Field**

* string input field
* character limit of 52
* only lower-case characters
* username restrictions:
  * must start with a letter
  * must contain at least one dash, a number, or not contain any vowels

If an "error" occurs within this field, a red error text will appear below the field as seen in Figure 3.3.10 with the error text of:

* "Must start with a letter and contain at least one dash, a number, or no vowels"

**"Your account password is" Field**

* string input field
* read-only
* character limit of 52
* only lower-case alphanumeric characters
* can be highlighted and then copied to the end-users' clipboard
* computer generated using [randomstring](https://www.npmjs.com/package/randomstring) NPM package:
  * length: 52 characters
  * charset: alphanumeric

**"Re-enter generated password" Field**

* string input field
* character limit of 52
* only lower-case alphanumeric characters

If an "error" occurs within this field, a red error text will appear below the field as seen in Figure 3.3.10 with the error text of:

* "These passwords don't match"

**"Download Recovery File" Button**

Clicking this button will download a `.txt` file type that contains only one thing: the randomstring generated password in read-only format from the form. The "download" occurs via a "save file as" dialog window on the end-users' operating system that allows them to save the file \(and/or rename the file\) to a location of their choosing on their computer.

_more details coming_...

#### Cancel

No change in behaviour or appearance for this button.

### 3.4 Import Peerplays Keys

{% hint style="warning" %}
Importing Peerplays keys will have the same user flow from part 3.2 up till figure 3.3.5.
{% endhint %}

The following outline the flow of importing keys into a Scatter account if the end-user opted for the "Login to Import Peerplays Account" button route.

#### Login to Import Peerplays Account

![Figure 3.4.1: Login to Import Peerplays Account \[empty\]](../.gitbook/assets/image%20%284%29.png)

![Figure 3.4.2: Login to Import Peerplays Account \[filled - errors\]](../.gitbook/assets/image%20%286%29.png)

![Figure 3.4.3: Login to Import Peerplays Account \[filled\]](../.gitbook/assets/image%20%2833%29.png)

Peerplays account importing into Scatter will appear the end-user like any other Peerplays dapp login form:

* account name input field
* account password input field
* form submit/login button

**Errors**

If any form component has an error, their appearance will change to match that of Figure 3.4.2.

**"Account Name" Field**

* string input field
* character limit of 52
* only lower-case characters
* username restrictions:
  * must start with a letter
  * must contain at least one dash, a number, or not contain any vowels

If an "error" occurs within this field, a red error text will appear below the field as seen in Figure 3.4.2 with the error text of:

* "Must start with a letter and contain at least one dash, a number, or no vowels"

**"Password" Field**

* string input field
* character limit of 52
* only lower-case alphanumeric characters

If an "error" occurs within this field, a red error text will appear below the field as seen in Figure 3.4.2 with the error text of:

* "Password should be at least 22 symbols \(alphanumeric\)"

_more details coming_...

### 3.5 Support for PPY Asset/Retrieve PPY Balance

![Note: Screenshot not yet available for PPY. This is the screenshot for BTC. ](../.gitbook/assets/image%20%288%29.png)

### 3.6 Send PPY

![Note: Screenshot not yet available for PPY. This is the screenshot for BTC. ](../.gitbook/assets/image%20%2827%29.png)

### 3.7 Receive PPY

![](../.gitbook/assets/image%20%2816%29.png)

