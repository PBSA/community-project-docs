---
description: non-functional requirements
---

# Scatter wallet Acceptance Criteria

### Traceability Matrix

| **Status** | draft |
| :--- | :--- |
| **Product Owner** | @Jonathan Baha'i |
| **Document owner** | @Bobinson Bobby |
| **Stakeholders** | @Jonathan Baha'i |
| **Approver** | @Jonathan Baha'i |
| **Technical Writers** |  |
| **Contributors** |   @bobinson  |

Tickets or the PRs provide the following information. This in addition to the functional requirements and acceptance.

### 1. Major environment/package versions

#### Node Packages

* Babel
  * @babel/core: v7.5.4
  * @babel/preset-env: v7.5.4
  * @babel/runtime: v8.06.0
* Webpack: v4.35.3
* Node: v8.16.1
* Vue: v2.6.10
* Vuex: v3.0.1

Note: Upon installation, all dependencies are bumped to the latest minor \(backwards compatible\) version.

| The packages used must be verified against the [dependency list provided by Gitlab](https://gitlab.com/PBSA/streamersedge/streamersedge-gui/dependencies) in every build. |
| :--- |


Refer [Application Security with GitLab](https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/356319253/Application+Security+with+GitLab) for more details.

### 2. Browsers & Versions

As the Scatter project is delivered via Electron, browser support will be handled by the Electron package, and therefore be Electron/Chromium only.

Operating System support will be the minimum required to run Electron.

Electron version: v5.0.6^ \(bumped to latest minor version\).

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Supported Operating Systems</b>
      </th>
      <th style="text-align:left">Details</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <ul>
          <li><b>Windows</b>
          </li>
        </ul>
      </td>
      <td style="text-align:left">Windows 7 and later are supported, older operating systems are not supported
        (and do not work).</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li><b>macOS</b>
          </li>
        </ul>
      </td>
      <td style="text-align:left">Only 64bit binaries are provided for macOS, and the minimum macOS version
        supported is macOS 10.10 (Yosemite).</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p></p>
        <ul>
          <li><b>Linux</b>
          </li>
        </ul>
      </td>
      <td style="text-align:left">
        <p></p>
        <p>Ubuntu 12.04 and newer</p>
      </td>
    </tr>
  </tbody>
</table>### 3. Screen Resolutions Support

The Electron window can be resized and the elements within should be responsive.

The minimum size of the window is 800x720.

### 4. Code Quality

* Codequality related requirements set by product sponsor [Jonathan Baha'i](https://peerplays.atlassian.net/wiki/people/557058:10859e4a-36e5-4aa3-9b54-82b9cb247baf?ref=confluence) are given below:

6e827d89-1b4a-408a-9ae1-9ad4563fd321DECIDEDa4719ae7-c03c-4d39-8f50-e9693ae416a3Sonarcloud reports should be available for all the PRs & they should be acceptableDECIDED4868850c-dbfe-47af-9f0e-412b998f42f1Codeclimate code quality and complexity rules must be tested via Gitlab and available for all the PRs

* Sonarcloud reports should be available for all the PRs & they should be acceptable
* Codeclimate code quality and complexity rules must be tested via Gitlab and available for all the PRs

### 5. Security

* Security requirements set and expected by the product sponsor/owner [Jonathan Baha'i](https://peerplays.atlassian.net/wiki/people/557058:10859e4a-36e5-4aa3-9b54-82b9cb247baf?ref=confluence) are given below:

702638ee-30db-49b2-863d-3441e27d1fc9DECIDEDebe835b2-c6f3-4d28-a869-d668b1324f2fMinimal OWASP security checklist compliance must be achieved by performing OWASP ZAP or Gitlab SAST based scanning of the application.DECIDED66aa22e6-31e6-4845-9c52-714f7f3588feNo Vulnerabilities should be reported in the code base and it must be verified with with [Gitlab CI Vulnerability report.](https://gitlab.com/PBSA/streamersedge/StreamersEdge/security/dashboard/?project_id=12046101&scope=dismissed&page=1&days=90)DECIDED36708255-022f-4b60-b28b-550c4c76e000ELK based logging must be available for anyone performing feature testing and PR review \( Implement Security Logging and Monitoring\)

* Minimal OWASP security checklist compliance must be achieved by performing OWASP ZAP or Gitlab SAST based scanning of the application.
* No Vulnerabilities should be reported in the code base and it must be verified with with [Gitlab CI Vulnerability report.](https://gitlab.com/PBSA/streamersedge/StreamersEdge/security/dashboard/?project_id=12046101&scope=dismissed&page=1&days=90)
* ELK based logging must be available for anyone performing feature testing and PR review \( Implement Security Logging and Monitoring\)

### 6. Performance

Optional and nice to have action item.

