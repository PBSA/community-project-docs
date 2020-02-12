# Release Strategy

{% hint style="info" %}
The following proposition will allow PBSA/Peerplays Global to produce public releases once a month on project X.

* every two weeks: two releases are made at a minimum; one private \(alpha\); one public \(beta\)
  * steps 1-8
* every six weeks: a new full release
  * steps 1-8 \(alpha & beta\) pre-requisite then steps 9-10

Step 6 outlines the alpha release process \(under “Steps for Peerplays Teams”\)  
Step 7 outlines the beta release process  
Step 8 outlines the main-net release process
{% endhint %}

### Steps for Peerplays Teams

All steps outlined below are mandatory.

0. This step is re-used for informing relevant parties of a new release

* inform either the Quality Assurance team or the Marketing team of the new alpha or beta release and:
  * provide the relevant team with release notes
  * provide the relevant team with download links/binaries

1. Peerplays developer will create a new branch from a projects repository `pbsa-develop` branch with the name format: `feature/ISSUE-ID` or `bug/ISSUE-ID`
2. Peerplays developer will do the necessary work on this new branch to complete the task at hand
3. Peerplays developer will create a pull request \(PR\) to merge their new branch code into `pbsa-develop`
4. Peerplays developer will request code review from one or more other developers on the PR they opened in step _3._
5. Peerplays developer will merge their PR into `pbsa-develop` once another developer has approved their PR
6. Peerplays developer or DevOps engineer will:
   1. create a new release branch with the name format: `release/vX.X.X-alpha` from `pbsa-develop`
   2. create a new git pre-release **draft** from the branch created in step _6.1._ \(this will create a new git tag\)
      1. **no binaries are to be attached** to this git release as these binaries are pointing to private Peerplays test-nets
   3. produce the binaries from the new release generated in step six pointing to private Peerplays test-nets
      1. these binaries are sent to the Quality Assurance team directly
   4. publish the drafted git pre-release created in step _6.2._
   5. Complete step _0_ for the QA team for a private alpha release
7. After QA process has been completed:
   1. Peerplays developer or DevOps engineer will open pull requests to merge the release branch generated in step six into:
      1. `master`
      2. `develop` \(third-party development branch\)
   2. DevOps engineer will approve and merge the PR’s into `master` and `develop`
   3. Peerplays developer or DevOps engineer will:
      1. create a new release branch with the name format: `release/vX.X.X-beta` from `master`
      2. create a new git pre-release **draft** from the branch created in step 7_.3.1._ with the name format: `vX.X.X-beta` \(this will create a new git tag\)
      3. produce the binaries from the new branch generated in step _7.3.1._ pointing to the public Peerplays test-net \(Beatrice\)
      4. attach the produced binaries to the newly drafted git pre-release in step _7.3.2._
      5. publish the drafted git pre-release created in step _7.3.2._
      6. Complete step _0_ for the Marketing team for a public beta release
8. Two weeks after the step _7_ beta pre-release has been completed, Peerplays developer or DevOps engineer will:
   1. create a new release branch with the name format: `release/X.X.X` from `master`
   2. create a new git release **draft** with the name format: `vX.X.X` \(this will create a new git tag\)
   3. produce the binaries from the new branch generated in step _8.1._ pointing to the Peerplays main-net \(Alice\)
   4. attach the produced binaries to the newly drafted git release in step _8.2._
   5. publish the drafted git release created in step _8.2._
   6. Complete step _0_ for the Marketing team for a public main-net release

### Steps for 3rd Party Developers

If you are a third party developer contributing to one of the Peerplays Network git repositories, the release strategy is similar.  
All steps outlined below are mandatory.

1. Third party developer will create a new branch from a projects repository `develop` branch with the name format: `feature/ISSUE-ID` or `bug/ISSUE-ID`
2. Third party developer will do the necessary work on this new branch to complete the task at hand
3. Third party developer will create a pull request \(PR\) to merge their new branch code into `develop`
   1. This PR **must** contain some release notes:
      1. within the CHANGELOG.md for the repository the PR belongs to
      2. within the PR description they have just created following the format seen on previous releases within the repository the PR belongs to
4. Third party developer will request code review from one or more other developers on the PR they opened in step _3._
5. Third party developer will merge their PR into `develop` once another developer has approved their PR
6. On a set time interval, a Peerplays developer will do some due diligence on the third party `develop` branch after which they will open a PR for `develop` into `pbsa-develop`.
   1. ensure the `develop` branch code compiles for:
      1. local development
      2. binary creation
   2. check for security vulnerabilities on the `develop` branch
   3. ensure unit tests pass on the `develop` branch

After step _6_ in the third party developer steps, the process continues on with the Peerplays team starting from step _6_ in the Peerplays Teams section at the start of this guide.

