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
  * @babel/core: 6.25.0
  * @babel/preset-react: v6.24.1
  * @babel/preset-env: v1.6.1
  * @babel/runtime: v6.23.0
* React: v16.5.0
* Redux: v3.7.1
* Webpack: v3.10.0
* Node: v8.16.1

| The packages used must be verified against the [dependency list provided by Gitlab](https://gitlab.com/PBSA/streamersedge/streamersedge-gui/dependencies) in every build. |
| :--- |


Refer [Application Security with GitLab](https://peerplays.atlassian.net/wiki/spaces/PROJECTS/pages/356319253/Application+Security+with+GitLab) for more details.

### 2. Browsers & Versions

2ba1fdc6-50bf-4610-a195-aab24de9c020DECIDED584197b8-cd3e-48a3-826a-0a7cf7f67535Browsers & their Versions for V2 is decided.

* Browsers & their Versions for V2 is decided.
* [Jonathan Baha'i](https://peerplays.atlassian.net/wiki/people/557058:10859e4a-36e5-4aa3-9b54-82b9cb247baf?ref=confluence) : The browser and OS versions 5050 V2.0 to be support the following browsers & OSs

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Supported Browsers</b>
      </th>
      <th style="text-align:left"><b>OS Versions</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <ul>
          <li><b>Google Chrome Stable</b> (chromium based)</li>
          <li>&gt;= 70</li>
        </ul>
      </td>
      <td style="text-align:left">Windows 10 (&gt;= 1803)</td>
    </tr>
    <tr>
      <td style="text-align:left">
        <ul>
          <li><b>Firefox Stable</b>
            <ul>
              <li>&gt;= 70</li>
            </ul>
          </li>
        </ul>
      </td>
      <td style="text-align:left">Windows 10 (&gt;= 1803)</td>
    </tr>
  </tbody>
</table>### 3. Screen Resolutions to be supported in 5050 V2

* Resolutions related requirements by [Jonathan Baha'i](https://peerplays.atlassian.net/wiki/people/557058:10859e4a-36e5-4aa3-9b54-82b9cb247baf?ref=confluence) are given below.

382ef26b-71d7-467b-bdcc-1b18e21effe7DECIDED7acff6ee-d603-41a7-8c86-d0c2cb7a6d50We will be using the same UI design for all the resolutions in V2DECIDEDbbd17b50-617d-445b-b63f-179ae8b58ec4For smaller screens, no re-arrangement or components, buttons or icons will be madeDECIDEDb3ad67b7-8527-46cd-8b60-29bb744f97ebSmallest Screen size supported should be 1020x400

* We will be using the same UI design for all the resolutions in V2
* For smaller screens, no re-arrangement or components, buttons or icons will be made
* Smallest Screen size supported should be 1020x400

Supporting document is [Twitch UI behaviour](https://peerplays.atlassian.net/wiki/spaces/PIX/pages/361463869/Twitch+UI+behaviour)

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

Frontend developers are to make use of the newer React Dev Tools add-ons for their browsers and make use of the [profiling tools](https://scotch.io/tutorials/use-the-react-profiler-for-performance) to ensure their code is performant.

