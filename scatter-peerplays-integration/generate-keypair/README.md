---
description: Functional requirements for the Scatter Peerplays plugin.
---

# Functional Requirements

## 1.0 Introduction

### 1.1 Objective

### 1.2 Scope

The scope of this document is to list the functional requirements for the Scatter Project.

This document will provide a tabular listing of the Peerplays Scatter Wallet Integration features. The target features for the Scatter Wallet Peerplays plugin will be based on this document. The features that Peerplays Scatter integration will provide is going to be a sub-set of the [Peerplays Wallet Features](https://app.gitbook.com/@peerplays/s/community-project-docs/peerplays-wallet/peerplays-wallet-feature-list).

The scope of the entire project defined in the [project scope document](../project-scope.md).

### 1.3 Assumptions and Constraints

Assumptions:

* The production version of the application will be built with Electron.
* The production version of the application will use ScatterDesktop for encryption.
* Unless specified otherwise, all features/functions described in this document assume the end-user is logged into the Scatter application.

Constraints:

* The application will not run on outdated operating systems. Specific versions can be found in the acceptance criteria document.

## **2.0 High Level Requirements**

| Requirement | User Story |
| :--- | :--- |
| [Connect to Peerplays blockchain](https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M2il8u16nIr5ISkorpf/scatter-peerplays-integration/generate-keypair/connect-to-peerplays-blockchain) | As a user I should be able to connect to the Peerplays main net. |
| [Generate keypair](https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M2il8u16nIr5ISkorpf/scatter-peerplays-integration/generate-keypair/generate-keypair-1) | As a user I should be able to generate a Peerplays keypair. |
| [Create Peerplays account](https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M2il8u16nIr5ISkorpf/scatter-peerplays-integration/generate-keypair/create-peerplays-account) | The user must be directed to a faucet to create the peerplays account |
| [Import Peerplays Keys](https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M2il8u16nIr5ISkorpf/scatter-peerplays-integration/generate-keypair/import-peerplays-keys) | A Given Peerplays private key should be imported by Scatter wallet |
| [Support for PPY asset](https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M2il8u16nIr5ISkorpf/scatter-peerplays-integration/generate-keypair/support-for-ppy-asset-retreive-ppy-balance) | As a user I should have PPY asset support within the Scatter wallet. |
| [Retrieve PPY Balance](https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M2il8u16nIr5ISkorpf/scatter-peerplays-integration/generate-keypair/support-for-ppy-asset-retreive-ppy-balance) | As a user I should be able to see my PPY balance within the Scatter wallet. |
| [Send PPY](https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M2il8u16nIr5ISkorpf/scatter-peerplays-integration/generate-keypair/send-ppy) | As a user I should be able to send PPY via the Scatter wallet. |
| [Receive PPY](https://app.gitbook.com/@peerplays/s/community-project-docs/~/drafts/-M2il8u16nIr5ISkorpf/scatter-peerplays-integration/generate-keypair/receive-ppy) | As a user I should be able to receive PPY via the Scatter wallet. |

