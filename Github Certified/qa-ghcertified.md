Q:: What is CodeQL?

a) A version control system

b) A code analysis tool

c) A programming language

d) A text editor

A:: <span style="color: #f800f8">**Answer:** B</span>

A code analysis tool

Source: https://codeql.github.com/

Q:: What does `shifting left` mean in the context of Security?

a) Writing code in a language that is commonly used

b) Adopting security practices early in the development cycle

c) Incorporating security practices right before hitting production

d) Writing code without worrying about security

A:: <span style="color: #f800f8">**Answer:** B</span>

Adopting security practices early in the development cycle

Source: https://github.com/readme/guides/github-advanced-security-telus

Q:: What are Repository Security Advisories?

a) A list of security issues that are publicly available for anyone to see and stay away from.

b) It's a place to gather and publicly discuss security issues in the open source community.

c) A private space where repository maintainers can discuss vulnerabilities and security issues within the codebase.

d) GitHub security experts that help GitHub Enterprise users with their security issues.

A:: <span style="color: #f800f8">**Answer:** C</span>

A private space where repository maintainers can discuss vulnerabilities and security issues within the codebase.

Source: https://docs.github.com/en/code-security/security-advisories/working-with-repository-security-advisories/about-repository-security-advisories

Q:: Which tool helps you keep the repository dependencies up to date?

a) Dependabot

b) Security Advisories

c) GitHub Actions

d) CodeQL

A:: <span style="color: #f800f8">**Answer:** A</span>

Dependabot

Source: https://docs.github.com/en/code-security/dependabot

Q:: Which of the following is a curated list of security vulnerabilities found in open source projects?

a) GitHub Security Journal

b) CodeQL

c) GitHub Advisory Database

d) Dependabot

A:: <span style="color: #f800f8">**Answer:** C</span>

GitHub Advisory Database

Source: https://docs.github.com/en/code-security/security-advisories/working-with-global-security-advisories-from-the-github-advisory-database/about-the-github-advisory-database

Q:: Which of these GitHub security features are available for FREE for both public and private personal repositories? (Choose four.)

a) Security advisories

b) Code scanning

c) Secret scanning

d) Dependabot secret scanning

e) Dependabot alerts and security updates

f) Dependabot code scanning

g) Security Policy

h) Dependabot version updates

A:: <span style="color: #f800f8">**Answer(s): G, A, E, H</span>

Security Policy; Security advisories; Dependabot alerts and security updates; Dependabot version updates

Source: https://docs.github.com/en/code-security/getting-started/github-security-features

Q:: Which of these best describes secret scanning?

a) Secret scanning is a git hook that will scan your commits for secrets such as private keys or tokens before they are pushed to GitHub.

b) Secret scanning is a tool for secure secret storage and management.

c) Secret scanning scans your repository for secrets such as private keys or tokens.

d) Secret scanning scans your repository for potential code vulnerabilities that could expose secrets such as private keys or tokens.

A:: <span style="color: #f800f8">**Answer:** C</span>

Secret scanning scans your repository for secrets such as private keys or tokens.

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning

Q:: Which parts of the repository are scanned by secret scanning? (Choose two.)

a) GitHub Environment secrets

b) GitHub Repository secrets

c) Entire git history on all protected branches in the repository

d) Titles, descriptions and comments in open and closed historical issues

e) Entire git history on all branches in the repository

A:: <span style="color: #f800f8">**Answer(s): E, D</span>

Entire git history on all branches in the repository; Titles, descriptions and comments in open and closed historical issues

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning#about-secret-scanning, https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-a-repository, https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-an-environment

Q:: What's the purpose of the Secret scanning partner program?

a) GitHub Partner program allows enterprises and organizations with GitHub Advanced Security license to use GitHub secret scanning to scan their repositories.

b) Service Providers can partner with GitHub so that the format of their secrets can be recognized by GitHub secret scanning.

c) GitHub partners with external security companies to provide secret scanning for GitHub repositories.

d) It's a program where registered security professionals can in good faith report to GitHub any secrets they find in GitHub repositories and get paid rewards for it.

A:: <span style="color: #f800f8">**Answer:** B</span>

Service Providers can partner with GitHub so that the format of their secrets can be recognized by GitHub secret scanning.

Source: https://docs.github.com/en/code-security/secret-scanning/secret-scanning-partner-program

Q:: Public repositories owned by personal users as well as public repositories owned by organizations can use secret scanning for free.

a) False

b) True

A:: <span style="color: #f800f8">**Answer:** B</span>

True

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning#about-secret-scanning

Q:: How can you prevent commits containing cloud provider credentials from being pushed to GitHub?

a) Create a GitHub Action that will scan your commits for secrets before they are pushed to GitHub.

b) Enable a branch protection rule for your repository.

c) Enable a secret scanning push protection rule for your repository or organization.

d) Include a `.gitignore` file in your repository that will ignore files containing secrets.

A:: <span style="color: #f800f8">**Answer:** C</span>

Enable a secret scanning push protection rule for your repository or organization.

Source: https://docs.github.com/en/code-security/secret-scanning/push-protection-for-repositories-and-organizations

Q:: Which of these is true about the GitHub secret scanning partner program? (Choose three.)

a) It is a program where service providers can provide GitHub with the regex patterns of secrets that they issue so GitHub secret scanning can recognize them.

b) The partner can take actions upon receiving notification from GitHub about a leaked secret, such as revoking the secret and informing the owner of the compromised secret.

c) When GitHub identifies a secret from a partnered service provider, it notifies the service provider about the leaked secret.

d) GitHub has the ability to automatically revoke leaked secrets and notify the service provider that they have been invalidated by GitHub.

e) It grants the partner access to the secret GitHub scanning API so that the service provider can scan GitHub repositories for secrets that match their format.

A:: <span style="color: #f800f8">**Answer(s): A, C, B</span>

It is a program where service providers can provide GitHub with the regex patterns of secrets that they issue so GitHub secret scanning can recognize them.; When GitHub identifies a secret from a partnered service provider, it notifies the service provider about the leaked secret.; The partner can take actions upon receiving notification from GitHub about a leaked secret, such as revoking the secret and informing the owner of the compromised secret.

Source: https://docs.github.com/en/code-security/secret-scanning/secret-scanning-partner-program

Q:: How can you exclude certain directories or files from secret scanning?

a) Include these files in the `.gitignore` file

b) By creating a `secret_scanning.yml` file and including paths that should not be scanned

c) By creating a `dependabot.yml` file and including paths which should not be scanned

d) It's not possible to exclude specific files and/or directories from being scanned. Once you enable secret scanning for a repository, all files and directories will be scanned.

A:: <span style="color: #f800f8">**Answer:** B</span>

By creating a `secret_scanning.yml` file and including paths that should not be scanned

Source: https://docs.github.com/en/code-security/secret-scanning/configuring-secret-scanning-for-your-repositories#excluding-directories-from-secret-scanning-alerts-for-users

Q:: You have included some fake secrets in your test code and they have been picked up by GitHub's secret scanning. What can you do to tell GitHub that these are fake secrets used in tests and can be ignored by secret scanning? (Choose two.)

a) By creating a `secret_scanning.yml` file within which you declare paths where fake secrets are located, so scans will omit them

b) In your test files, add a comment `#gh_ignore: fake secret` on the line where the fake secret is located.

c) By creating a `.github/codeql.yml` file within which you declare paths where fake secrets are located, so scans will omit them

d) Close the Secret Scanning Alert with `Used in tests` close reason

A:: <span style="color: #f800f8">**Answer(s): A, D</span>

By creating a `secret_scanning.yml` file within which you declare paths where fake secrets are located, so scans will omit them; Close the Secret Scanning Alert with `Used in tests` close reason

Source: https://docs.github.com/en/code-security/secret-scanning/using-advanced-secret-scanning-and-push-protection-features/excluding-folders-and-files-from-secret-scanning

Q:: You have accidentally committed your GitHub personal access token to a public repository. What actions should you take to prevent your account from being compromised?

a) Consider the token compromised and delete it immediately

b) Check if this token is used in any of your applications, if so - delete it.

c) Change the token's permissions to read-only

d) Overwrite the git history to mask the token

A:: <span style="color: #f800f8">**Answer:** A</span>

Consider the token compromised and delete it immediately

Source: https://docs.github.com/en/code-security/secret-scanning/managing-alerts-from-secret-scanning#securing-compromised-secrets

Q:: What is the behavior when a new secret pattern is added or updated in the GitHub secret scanning partner program?

a) GitHub will create an issue in all repositories with secret scanning enabled so the maintainers can check the repository for any secrets matching the new pattern

b) GitHub will run a scan of all historical code content in public repositories with secret scanning enabled

c) The GitHub partner has to deal with the historically leaked secrets and GitHub will only scan any new commits for the new pattern

d) GitHub will only scan for the new pattern in newly pushed commits in repositories with secret scanning enabled. If a secret of that pattern was already present in the repository, it will not be detected.

A:: <span style="color: #f800f8">**Answer:** B</span>

GitHub will run a scan of all historical code content in public repositories with secret scanning enabled

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning#accessing-secret-scanning-alerts

Q:: Who will be notified when a NEW secret is pushed and detected in a repository? (Choose five.)

a) Organization owners and enterprise owners, but only if they are administrators of repositories where secrets were leaked

b) Everyone with write access to the repository

c) Security Managers

d) Commit authors

e) Users with custom roles with read/write access

f) Repository Administrators

g) All Organization owners and enterprise owners

A:: <span style="color: #f800f8">**Answer(s): F, C, E, A, D</span>

Repository Administrators; Security Managers; Users with custom roles with read/write access; Organization owners and enterprise owners, but only if they are administrators of repositories where secrets were leaked; Commit authors

Source: https://docs.github.com/en/code-security/secret-scanning/managing-alerts-from-secret-scanning/monitoring-alerts#incremental-scans

Q:: When GitHub runs a scan of all historical code in enterprise repositories what is the notification behavior? (Select two.)

a) GitHub notifies Repository administrators, security managers, and users with custom roles with read/write access whenever a secret is detected in a repository.

b) GitHub notifies the commit authors of the commits that contain exposed secrets.

c) GitHub notifies the enterprise owners and security managers, even if no secrets are found.

d) GitHub notifies the enterprise owners and security managers, only if it detects exposed secrets.

A:: <span style="color: #f800f8">**Answer(s): C, A</span>

GitHub notifies the enterprise owners and security managers, even if no secrets are found.; GitHub notifies Repository administrators, security managers, and users with custom roles with read/write access whenever a secret is detected in a repository.

Source: https://docs.github.com/en/code-security/secret-scanning/managing-alerts-from-secret-scanning/monitoring-alerts#historical-scans

Q:: Does GitHub use the same set of secret scanning patterns for both user alerts and push protection alerts?

a) Yes, its the same set of secret patterns

b) No, these are different sets of secret patterns

A:: <span style="color: #f800f8">**Answer:** B</span>

No, these are different sets of secret patterns

Source: https://docs.github.com/en/code-security/secret-scanning/secret-scanning-patterns#about-secret-scanning-patterns

Q:: What are the three different sets of secret scanning patterns that GitHub maintains? (Select three.)

a) Push protection patterns

b) Open source alert patterns

c) Cloud provider patterns

d) Enterprise alert patterns

e) User alert patterns

f) Partner patterns

A:: <span style="color: #f800f8">**Answer(s): F, E, A</span>

Partner patterns; User alert patterns; Push protection patterns

Source: https://docs.github.com/en/code-security/secret-scanning/secret-scanning-patterns#about-secret-scanning-patterns

Q:: Multiple public repositories that you are contributing to do not have secret scanning push protection option enabled. What can you do to protect yourself from accidentally pushing secrets to these repositories?

a) Add the files containing secrets to `.gitignore` file in all of the repositories

b) It's not possible, push protection has to be enabled on any of repository, organization or enterprise level

c) Enable `Push protection for yourself`, in your personal GitHub account settings

d) Download the GitHub push protection web plugin

A:: <span style="color: #f800f8">**Answer:** C</span>

Enable `Push protection for yourself`, in your personal GitHub account settings

Source: https://docs.github.com/en/code-security/secret-scanning/push-protection-for-users#about-push-protection-for-users

Q:: Your company has internal secrets that should not be pushed to GitHub repositories. The pattern of these secrets is not known by GitHub and therefore is not detected by secret scanning. What can companies do to protect their developers from accidentally pushing these secrets to repositories in their GitHub Organization?

a) In all repositories include `secret_scanning.yml` file which will define these custom secrets that should be scanned for.

b) Define custom GitHub Actions workflows for repositories in the organization that will scan for these secrets.

c) The company should join the GitHub partner program so the pattern of the companies secrets is recognized.

d) Define regex patterns for these secrets and enable custom patterns for secret scanning for the organization.

A:: <span style="color: #f800f8">**Answer:** D</span>

Define regex patterns for these secrets and enable custom patterns for secret scanning for the organization.

Source: https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/defining-custom-patterns-for-secret-scanning#defining-a-custom-pattern-for-an-organization

Q:: What information do Dependabot alerts provide?

a) Dependabot alerts tell you that your repository uses a package that is insecure.

b) Dependabot alerts tell you that your repository uses an untested version of a package.

c) Dependabot alerts tell you that your repository is being used by other public repositories.

d) Dependabot alerts tell you that your repository uses an outdated version of a package

A:: <span style="color: #f800f8">**Answer:** A</span>

Dependabot alerts tell you that your repository uses a package that is insecure.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts

Q:: What is the GitHub dependency graph?

a) There is no such thing as the GitHub dependency graph.

b) It is a GitHub maintained list of known vulnerabilities in open source software packages.

c) It is a tool that automatically proposes version updates to dependencies in a repository.

d) It is a representation of a repository's dependencies and dependents.

A:: <span style="color: #f800f8">**Answer:** D</span>

It is a representation of a repository's dependencies and dependents.

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph

Q:: Is GitHub dependency graph available for free to all repositories?

a) No, it's available for free for public repositories only. Private repositories can use it if they have the GitHub Advanced Security license.

b) Yes, it's available for free for all repositories.

A:: <span style="color: #f800f8">**Answer:** B</span>

Yes, it's available for free for all repositories.

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph#dependency-graph-availability

Q:: How does GitHub Dependency graph know what dependencies your project is using? (Choose two.)

a) Dependencies can be manually added using the Dependency submission API

b) GitHub scans the repository code for import statements of external packages

c) GitHub derives dependencies automatically from manifests and lock files committed to the repository

d) It's required to add a GitHub Actions workflow that uses the official `actions/dependency-graph` GitHub Action to add dependencies to the graph whenever a new commit is pushed to the repository

A:: <span style="color: #f800f8">**Answer(s): C, A</span>

GitHub derives dependencies automatically from manifests and lock files committed to the repository; Dependencies can be manually added using the Dependency submission API

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph#supported-package-ecosystems

Q:: When will the GitHub Dependency graph for your repository be updated? (Choose two.)

a) When your repository publishes a new git tag.

b) When the GitHub Actions workflow that uses the `actions/dependency-graph` GitHub Action is triggered.

c) When you push a commit to the repository's default branch, only if that changes or adds a supported manifest/lockfile.

d) When your repository publishes a new release.

e) When anyone pushes a change to the repository of one of your dependencies.

f) When you push any commit to the repository's default branch.

A:: <span style="color: #f800f8">**Answer(s): E, C</span>

When anyone pushes a change to the repository of one of your dependencies.; When you push a commit to the repository's default branch, only if that changes or adds a supported manifest/lockfile.

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-supply-chain-security#what-is-the-dependency-graph

Q:: In what format can you export the GitHub Dependency graph of your repository?

a) JSON

b) SPDX

c) XML

d) YAML

e) CSV

A:: <span style="color: #f800f8">**Answer:** B</span>

SPDX

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/exporting-a-software-bill-of-materials-for-your-repository

Q:: Can your repository use Dependency Graph without using Dependabot Alerts?

a) Yes

b) No

A:: <span style="color: #f800f8">**Answer:** A</span>

Yes

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph#using-the-dependency-graph

Q:: Which feature is a pre-requisite for using Dependabot Alerts on a repository?

a) Dependency graph

b) Dependency review

c) Dependency version updates

d) Dependency security updates

A:: <span style="color: #f800f8">**Answer:** A</span>

Dependency graph

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph#using-the-dependency-graph

Q:: Which of these statements about Dependabot Alerts are true? (Choose three.)

a) Dependabot Alerts are enabled by default for all public repositories

b) Dependabot Alerts are enabled by default for all repositories

c) Dependabot alerts tell you that your repository uses an outdated version of a package

d) When GitHub identifies a vulnerable dependency, they generate a Dependabot alert and display it on the Security tab for the repository

e) To enable Dependabot Alerts you first need to have Dependency Graph enabled on your repository

f) They partially rely on the GitHub Advisory Database

A:: <span style="color: #f800f8">**Answer(s): F, E, D</span>

They partially rely on the GitHub Advisory Database; To enable Dependabot Alerts you first need to have Dependency Graph enabled on your repository; When GitHub identifies a vulnerable dependency, they generate a Dependabot alert and display it on the Security tab for the repository

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts

Q:: What are the primary benefits of the Security Overview feature in GitHub?

a) Automated dependency updates

b) Centralized view of security alerts and policy management in an organization

c) Automatic code review for every push

d) Real-time threat detection

A:: <span style="color: #f800f8">**Answer:** B</span>

Centralized view of security alerts and policy management in an organization

Source: https://docs.github.com/en/code-security/security-overview/about-security-overview

Q:: What is CodeQL?

a) A code analysis engine developed by GitHub

b) A third-party tool for static code analysis

c) A new programming language for security analysis

d) A database used to store code scanning results

A:: <span style="color: #f800f8">**Answer:** A</span>

A code analysis engine developed by GitHub

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql#about-code-scanning-with-codeql

Q:: What do Dependabot alerts indicate in GitHub?

a) Conflicts between different dependencies

b) The presence of a vulnerable dependency or malware in your repository

c) Errors in dependency configuration files

d) Outdated dependencies that need to be updated

A:: <span style="color: #f800f8">**Answer:** B</span>

The presence of a vulnerable dependency or malware in your repository

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts#about-dependabot-alerts

Q:: What is the purpose of code scanning in GitHub?

a) To synchronize code with production servers

b) To identify vulnerabilities and errors in code

c) To review pull requests automatically

d) To check code formatting and style

A:: <span style="color: #f800f8">**Answer:** B</span>

To identify vulnerabilities and errors in code

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning#about-code-scanning

Q:: Is secret scanning available for both public and private repositories on GitHub?

a) No, it is only available for public repositories

b) No, it is only available for private repositories

c) Yes, with no additional requirements

d) Yes, but for private repositories, it requires a license for GitHub Advanced Security

A:: <span style="color: #f800f8">**Answer:** D</span>

Yes, but for private repositories, it requires a license for GitHub Advanced Security

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning#about-secret-scanning

Q:: What does the default CodeQL analysis setup in GitHub do?

a) Automatically chooses languages to analyze, query suite to run, and events that trigger scans

b) Manually requires users to specify languages and queries for each scan

c) Scans code only on a monthly basis

d) Requires separate installation of third-party scanning tools

A:: <span style="color: #f800f8">**Answer:** A</span>

Automatically chooses languages to analyze, query suite to run, and events that trigger scans

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql#about-code-scanning-with-codeql

Q:: What is the main purpose of using the CodeQL CLI?

a) To automatically merge pull requests

b) To schedule regular maintenance tasks in a repository

c) To manage repository settings and permissions

d) To generate a database representation of a codebase, a CodeQL database

A:: <span style="color: #f800f8">**Answer:** D</span>

To generate a database representation of a codebase, a CodeQL database

Source: https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/about-the-codeql-cli#about-the-codeql-cli

Q:: Which of the following languages is NOT supported by CodeQL for code scanning?

a) PHP

b) C/C++

c) Python

d) JavaScript/TypeScript

A:: <span style="color: #f800f8">**Answer:** A</span>

PHP

Source: https://codeql.github.com/docs/codeql-overview/supported-languages-and-frameworks/#languages-and-compilers

Q:: How does CodeQL analyze code in GitHub?

a) It uses machine learning to predict potential vulnerabilities based on past commits

b) It performs manual code reviews submitted by GitHub community members

c) It generates a CodeQL database and runs queries to identify problems, displaying results as code scanning alerts

d) It relies solely on third-party tools for code analysis

A:: <span style="color: #f800f8">**Answer:** C</span>

It generates a CodeQL database and runs queries to identify problems, displaying results as code scanning alerts

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql#about-codeql

Q:: How can CodeQL be used in an external CI system together with GitHub repositories?

a) Run CodeQL CLI in the external CI system to scan code and upload the results to the GitHub repository

b) Upload source code to GitHub for analysis and then download results for use in the CI system

c) CodeQL cannot be used in external CI systems; it is exclusive to GitHub Actions

d) Manually run CodeQL locally and email the results to the GitHub repository administrators

A:: <span style="color: #f800f8">**Answer:** A</span>

Run CodeQL CLI in the external CI system to scan code and upload the results to the GitHub repository

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#about-using-code-scanning-with-your-existing-ci-system

Q:: Which of these statements isn't true about secret scanning on GitHub?

a) Secret scanning is a tool for secure secret storage and management.

b) Secret scanning will scan titles, descriptions, and comments, in open and closed historical issues for secrets.

c) Secret scanning will scan your entire Git history on all branches present in your GitHub repository for secrets.

d) Secret scanning can prevent supported secrets from being pushed into your enterprise, organization, or repository.

A:: <span style="color: #f800f8">**Answer:** A</span>

Secret scanning is a tool for secure secret storage and management.

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning

Q:: Which top-level keys are required in the `dependabot.yml` file?

a) `assignees` and `directory`

b) `updates` and `directory`

c) `version` and `updates`

d) `version` and `package-ecosystem`

A:: <span style="color: #f800f8">**Answer:** C</span>

`version` and `updates`

Source: https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file#about-the-dependabotyml-file

Q:: Which GitHub Action can be used to upload a third-party SARIF file?

a) `github/codeql-action/upload-sarif`

b) `codeql-upload-sarif`

c) `github/codeql-action`

d) `actions/upload-sarif`

A:: <span style="color: #f800f8">**Answer:** A</span>

`github/codeql-action/upload-sarif`

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/uploading-a-sarif-file-to-github#uploading-a-code-scanning-analysis-with-github-actions

Q:: Which tool can be used in a third-party CI system to upload code analysis results to GitHub?

a) GitHub CLI

b) CodeQL API

c) GitHub Actions `github/codeql-action`

d) CodeQL CLI

A:: <span style="color: #f800f8">**Answer:** D</span>

CodeQL CLI

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#about-using-code-scanning-with-your-existing-ci-system

Q:: What is required for a CI server to upload SARIF results to GitHub?

a) A direct connection to the GitHub Advisory Database.

b) A GitHub App or personal access token with `security_events` write permission.

c) A special plugin installed in the CI system.

d) Administrator access to the GitHub repository.

A:: <span style="color: #f800f8">**Answer:** B</span>

A GitHub App or personal access token with `security_events` write permission.

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#generating-a-token-for-authentication-with-github

Q:: What happens when a second SARIF results file is uploaded to GitHub for a single commit?

a) It replaces the original set of data.

b) It creates a new branch in the repository

c) It appends the results to the existing file.

d) It is ignored by GitHub.

A:: <span style="color: #f800f8">**Answer:** A</span>

It replaces the original set of data.

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#uploading-your-results-to-github

Q:: How can users exclude specific directories from secret scanning alerts on GitHub?

a) By editing the repository's `README.md` file.

b) Through the repository's `Security` tab, in the `Secret scanning` menu.

c) Through the repository's `Settings` tab, in the `Code security and analysis` menu.

d) By configuring a `secret_scanning.yml` file, under the `.github` path in the repository.

A:: <span style="color: #f800f8">**Answer:** D</span>

By configuring a `secret_scanning.yml` file, under the `.github` path in the repository.

Source: https://docs.github.com/en/code-security/secret-scanning/configuring-secret-scanning-for-your-repositories#excluding-directories-from-secret-scanning-alerts-for-users

Q:: Which key should be used in a `secret_scanning.yml` file to exclude directories from secret scanning alerts in GitHub?

a) `ignore-directories`

b) `exclude-paths:`

c) `paths-exclude:`

d) `paths-ignore:`

A:: <span style="color: #f800f8">**Answer:** D</span>

`paths-ignore:`

Source: https://docs.github.com/en/code-security/secret-scanning/configuring-secret-scanning-for-your-repositories#excluding-directories-from-secret-scanning-alerts-for-users

Q:: What is the maximum number of custom patterns that can be defined for secret scanning on GitHub?

a) 100 for organizations/enterprises and 500 for repositories.

b) 100 for organizations, enterprises and repositories.

c) 500 for organizations/enterprises and 100 for repositories.

d) There's no limit to the number of custom patterns you can define for secret scanning in GitHub.

A:: <span style="color: #f800f8">**Answer:** C</span>

500 for organizations/enterprises and 100 for repositories.

Source: https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/defining-custom-patterns-for-secret-scanning#about-custom-patterns-for-secret-scanning

Q:: Fill in the blank: `GitHub __________ is a feature that you can use to analyze code in a GitHub repository to find security vulnerabilities and coding errors.`

a) Vulnerability Detection

b) Dependency Graph

c) Code Scanning

d) Security Advisories

A:: <span style="color: #f800f8">**Answer:** C</span>

Code Scanning

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning

Q:: Which GitHub Advanced Security feature allows you to find, triage, and prioritize fixes for new and existing problems in your code?

a) Code scanning

b) Dependabot alerts

c) Security advisories

d) Security policies

A:: <span style="color: #f800f8">**Answer:** A</span>

Code scanning

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning

Q:: How can you enable code scanning for a repository?

a) Go to the security tab of the repository settings and enable code scanning with default or advanced setup.

b) Go to the security tab of the repository settings and answer a questionnaire about the repository contents. Based on the answers, GitHub will enable code scanning with the appropriate configuration.

c) Go to your user settings and enable code scanning, you can choose to enable it for all or only selected repositories.

d) Add a `.github/codeql.yml`configuration file to the repository.

A:: <span style="color: #f800f8">**Answer:** A</span>

Go to the security tab of the repository settings and enable code scanning with default or advanced setup.

Source: https://docs.github.com/en/code-security/code-scanning/enabling-code-scanning/configuring-default-setup-for-code-scanning

Q:: How can you configure your GitHub repository to run CodeQL analysis on a schedule? (Choose two.)

a) By raising a request with GitHub support to enable scheduled CodeQL analysis for the repository.

b) By adding a `schedule` property to the `.github/codeql.yml` configuration file.

c) By using the default CodeQL analysis setup.

d) By creating a GitHub Actions workflow with a `schedule` trigger. The workflow should leverage actions from the `github/codeql-action` repository.

e) By setting the `codeql.trigger` property in the repository settings to `schedule`.

A:: <span style="color: #f800f8">**Answer(s): D, C</span>

By creating a GitHub Actions workflow with a `schedule` trigger. The workflow should leverage actions from the `github/codeql-action` repository.; By using the default CodeQL analysis setup.

Source: https://docs.github.com/en/code-security/code-scanning/enabling-code-scanning/configuring-default-setup-for-code-scanning#about-default-setup

Q:: An organization has recently started using CodeQL analysis for all pull requests on their repositories as well as running the analysis on an hourly schedule. Since then they are experiencing larger than usual GitHub Actions bills. What is the most likely cause of this?

a) The code scanning analysis is finding more issues than expected and is taking longer to complete.

b) Code scanning can only be run on a daily schedule and the organization is being billed for the additional usage.

c) Code scanning uses GitHub Actions and the organization is being billed for the additional usage.

d) There is no correlation between code scanning and GitHub Actions billing. The organization is being billed for other GitHub Actions workflows.

A:: <span style="color: #f800f8">**Answer:** C</span>

Code scanning uses GitHub Actions and the organization is being billed for the additional usage.

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning#about-billing-for-code-scanning

Q:: If you don't want to use GitHub Actions, you can run code scanning in an external CI system, then upload the results to GitHub.

a) True

b) False

A:: <span style="color: #f800f8">**Answer:** A</span>

True

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#about-using-code-scanning-with-your-existing-ci-system

Q:: When using a third party CI system to run code scanning, what GitHub tool do you need to analyze the codebase?

a) You don't specifically need a GitHub tool, any static analysis tool that can produce results in SARIF format will work.

b) You need to install the GitHub Code Scanning tool.

c) You need to install GitHub CLI

d) You need to install CodeQL CLI

A:: <span style="color: #f800f8">**Answer:** A</span>

You don't specifically need a GitHub tool, any static analysis tool that can produce results in SARIF format will work.

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#about-using-code-scanning-with-your-existing-ci-system

Q:: When using GitHub Actions as your CI system and a third party tool to run code scanning, how can you upload the SARIF results to GitHub?

a) You can only use CodeQL when running code scanning in GitHub Actions. Third party code scanning tools are not supported.

b) By using the `github/codeql-action/upload-sarif` GitHub Action

c) When using GitHub Actions the SARIF results are automatically uploaded to GitHub.

d) By using the `actions/upload-artifact` GitHub Action

A:: <span style="color: #f800f8">**Answer:** B</span>

By using the `github/codeql-action/upload-sarif` GitHub Action

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/uploading-a-sarif-file-to-github#uploading-a-code-scanning-analysis-with-github-actions

Q:: Can you use CodeQL analysis with third party CI systems?

a) No, because it requires using the `github/codeql-action` GitHub Action

b) Yes, you just need to use the CodeQL CLI

A:: <span style="color: #f800f8">**Answer:** B</span>

Yes, you just need to use the CodeQL CLI

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system

Q:: Which of these is true about code scanning? (Choose two.)

a) Code scanning is a replacement for manual code review.

b) Code scanning helps finding any leaked credentials in the codebase such as API keys or cloud credentials.

c) Code scanning can be integrated into the CI pipeline to find security issues early in the development process.

d) Code scanning helps finding insecure code patterns which can be missed by manual code review.

e) Code scanning scans your code to search for all dependencies and their versions to find any vulnerable dependencies.

A:: <span style="color: #f800f8">**Answer(s): D, C</span>

Code scanning helps finding insecure code patterns which can be missed by manual code review.; Code scanning can be integrated into the CI pipeline to find security issues early in the development process.

Source: https://docs.github.com/en/code-security/supply-chain-security/end-to-end-supply-chain/securing-code#scan-your-code-for-vulnerable-patterns

Q:: When using CodeQL analysis in your GitHub Actions workflow, how often is the scan triggered?

a) Code scanning can be triggered on a configurable schedule or on pull requests.

b) Code scanning can be triggered for many different events that happen in the repository.

c) Code scanning is triggered on every push to the repository.

d) Code scanning is triggered on a configurable schedule

A:: <span style="color: #f800f8">**Answer:** B</span>

Code scanning can be triggered for many different events that happen in the repository.

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning#about-code-scanning

Q:: What is the effect of adding the `paths-ignore` keyword to your code scanning GitHub Actions workflow?

a) It tells CodeQL to omit all `*.txt` and `*.md` files from the analysis.

b) Preventing the CodeQL analysis from running on pull requests that change files with the specified extensions.

c) Avoiding unnecessary scans when files that are not relevant to the analysis are changed.

d) Pull request checks will ignore any CodeQL vulnerabilities that are found in `*.txt` and `*.md` files.

A:: <span style="color: #f800f8">**Answer:** C</span>

Avoiding unnecessary scans when files that are not relevant to the analysis are changed.

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#avoiding-unnecessary-scans-of-pull-requests

Q:: CodeQL scanning supports:

a) Only compiled languages

b) Both compiled and interpreted languages

c) Only interpreted languages

d) All programming languages

A:: <span style="color: #f800f8">**Answer:** B</span>

Both compiled and interpreted languages

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql#about-codeql

Q:: What are CodeQL queries used for?

a) CodeQL queries analyze your codebase and are used to create a CodeQL database.

b) CodeQL queries are used for code review purposes in GitHub.

c) CodeQL queries are text-based questions you can ask the CodeQL engine about your codebase.

d) CodeQL queries can be run against a CodeQL database to identify patterns that may indicate coding errors or security vulnerabilities.

A:: <span style="color: #f800f8">**Answer:** D</span>

CodeQL queries can be run against a CodeQL database to identify patterns that may indicate coding errors or security vulnerabilities.

Source: https://codeql.github.com/docs/writing-codeql-queries/about-codeql-queries/

Q:: What is QL?

a) QL is a npm package that is used by CodeQL to scan code

b) QL is a similar product to CodeQL but is used for scanning text files instead of code

c) QL stands for Quality Level and is a metric used by CodeQL

d) QL is a query language that underlies CodeQL

A:: <span style="color: #f800f8">**Answer:** D</span>

QL is a query language that underlies CodeQL

Source: https://codeql.github.com/docs/ql-language-reference/about-the-ql-language/

Q:: What is a CodeQL query suite?

a) CodeQL suite is a collection of CodeQL results

b) CodeQL suite is a collections of CodeQL queries

c) CodeQL suite is a collection of CodeQL supported languages

d) CodeQL suite is a collection of CodeQL databases

A:: <span style="color: #f800f8">**Answer:** B</span>

CodeQL suite is a collections of CodeQL queries

Source: https://docs.github.com/en/code-security/code-scanning/managing-your-code-scanning-configuration/codeql-query-suites#about-codeql-query-suites

Q:: What are the different types of CodeQL packs? (Choose three.)

a) Query packs

b) Model packs

c) Code packs

d) Library packs

e) Language packs

f) Vulnerability packs

A:: <span style="color: #f800f8">**Answer(s): A, D, B</span>

Query packs; Library packs; Model packs

Source: https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/customizing-analysis-with-codeql-packs#about-codeql-packs

Q:: What is a CodeQL query pack?

a) It's a set of results that were generated in the process of analyzing a CodeQL database

b) It's a collection of CodeQL queries

c) It's a library used by CodeQL queries

d) It's a set of pre-compiled queries with all transitive dependencies such as libraries and models

A:: <span style="color: #f800f8">**Answer:** D</span>

It's a set of pre-compiled queries with all transitive dependencies such as libraries and models

Source: https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/customizing-analysis-with-codeql-packs#about-codeql-packs

Q:: What are the steps of CodeQL analysis workflow?

a) Running CodeQL queries -> Interpreting the results

b) Creating a CodeQL database -> Interpreting the results -> Running CodeQL queries

c) Creating a CodeQL database -> Running CodeQL queries -> Interpreting the results

d) Running CodeQL queries -> Creating a CodeQL database -> Interpreting the results

A:: <span style="color: #f800f8">**Answer:** C</span>

Creating a CodeQL database -> Running CodeQL queries -> Interpreting the results

Source: https://codeql.github.com/docs/codeql-overview/about-codeql/#codeql-analysis

Q:: What is extraction in the context of CodeQL code analysis?

a) Extraction is the action of running CodeQL queries against a CodeQL database and extracting the results.

b) Extraction is the process of exporting data from a CodeQL database.

c) Extraction is the process of creating a relational representation of each source file in the codebase.

d) Extraction is the process of creating CodeQL queries specific to the codebase.

A:: <span style="color: #f800f8">**Answer:** C</span>

Extraction is the process of creating a relational representation of each source file in the codebase.

Source: https://codeql.github.com/docs/codeql-overview/about-codeql/#database-creation

Q:: Which of these statements are true regarding running CodeQL analysis on codebases with multiple programming languages? (Choose two.)

a) CodeQL creates one database for all programming languages in the codebase, as long as they are supported by CodeQL

b) CodeQL uses a different extractor for each programming language

c) CodeQL database schema is the same for each programming language

d) CodeQL creates separate databases for each programming language

A:: <span style="color: #f800f8">**Answer(s): B, D</span>

CodeQL uses a different extractor for each programming language; CodeQL creates separate databases for each programming language

Source: https://codeql.github.com/docs/codeql-overview/about-codeql/#database-creation

Q:: What are the differences when running CodeQL database creation for compiled and interpreted languages? (Choose two.)

a) For compiled languages, the extractor runs on the executable file.

b) For interpreted languages, the extractor runs on the executable file.

c) For interpreted languages, the extractor runs directly on the source code.

d) For interpreted languages, extraction works by monitoring the build process. All information is collected each time the interpreter is invoked to process a source file.

e) For compiled languages, the extractor runs directly on the source code.

f) For compiled languages, extraction works by monitoring the build process. All information is collected each time the compiler is invoked to process a source file.

A:: <span style="color: #f800f8">**Answer(s): F, C</span>

For compiled languages, extraction works by monitoring the build process. All information is collected each time the compiler is invoked to process a source file.; For interpreted languages, the extractor runs directly on the source code.

Source: https://codeql.github.com/docs/codeql-overview/about-codeql/#database-creation

Q:: Where can you see when the last CodeQL analysis was run when using the default code scanning setup?

a) In the code scanning tool status page

b) In repository insights

c) You can't see that information with the default setup

d) In the Dependabot tab

A:: <span style="color: #f800f8">**Answer:** A</span>

In the code scanning tool status page

Source: https://docs.github.com/en/code-security/code-scanning/enabling-code-scanning/evaluating-default-setup-for-code-scanning#evaluating-code-scanning-with-the-tool-status-page

Q:: Which of the following statements about enabling CodeQL scanning default setup are true? (Choose three.)

a) GitHub Actions need to be enabled as a prerequisite

b) Default setup will scan the repository on a schedule that you can configure. For event based scanning, you need to configure a GitHub Action workflow

c) You can only use the default query suite with default CodeQL scanning setup

d) You can enable default setup on any repository, regardless of the contents of the repository

e) You can enable default setup for all eligible repositories in an organization at once in the organization settings

f) You can only enable default setup on repositories that contain at least one CodeQL-supported language

A:: <span style="color: #f800f8">**Answer(s): E, A, D</span>

You can enable default setup for all eligible repositories in an organization at once in the organization settings; GitHub Actions need to be enabled as a prerequisite; You can enable default setup on any repository, regardless of the contents of the repository

Source: https://docs.github.com/en/code-security/code-scanning/enabling-code-scanning/configuring-default-setup-for-code-scanning

Q:: How can you customize your advanced CodeQL scanning setup with additional CodeQL query suites? (Choose two.)

a) By defining the customizations in the Security / Code scanning repository settings

b) By using the CodeQL CLI with a custom configuration file to run the analysis

c) By defining the customizations in the CodeQL analysis GitHub Actions workflow as input parameters to the `github/codeql-action/init` action

d) By using the `github/codeql-customizations` GitHub Action

e) By using a custom configuration file and defining additional queries there

A:: <span style="color: #f800f8">**Answer(s): E, C</span>

By using a custom configuration file and defining additional queries there; By defining the customizations in the CodeQL analysis GitHub Actions workflow as input parameters to the `github/codeql-action/init` action

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning

Q:: When running CodeQL analysis in GitHub Actions, what Actions should you use? (Choose three.)

a) `github/codeql-action/autobuild` only for compiled programming languages

b) `github/codeql-action/init`

c) `github/codeql-action/analyze` only for interpreted programming languages

d) `github/codeql-action/autobuild`

e) `github/codeql-action/init` only for compiled programming languages

f) `github/codeql-action/analyze`

A:: <span style="color: #f800f8">**Answer(s): B, F, A</span>

`github/codeql-action/init`; `github/codeql-action/analyze`; `github/codeql-action/autobuild` only for compiled programming languages

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/codeql-code-scanning-for-compiled-languages#about-the-codeql-analysis-workflow-and-compiled-languages

Q:: What is the simplest method to execute CodeQL analysis concurrently for each language in a multi-language repository using GitHub Actions?

a) Define the parallelism in the `github/codeql-action/analyze` action

b) By creating a separate workflow for each language

c) By creating a `languages` matrix for the job and then reference it in the `github/codeql-action/init` action's `languages` input parameter

d) By calling the `github/codeql-action/analyze` action in separate steps for each language

A:: <span style="color: #f800f8">**Answer:** C</span>

By creating a `languages` matrix for the job and then reference it in the `github/codeql-action/init` action's `languages` input parameter

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#changing-the-languages-that-are-analyzed

Q:: How can you use a custom CodeQL configuration file in a GitHub Actions workflow?

a) By storing the configuration in `.github/codeql/config-config.yml` file. The `github/codeql-action/init` action will automatically detect the file and use it

b) By uploading that file in the Code Scanning section of the Security tab in the repository

c) By storing the configuration in `.github/workflows/codeql-analysis.yml` file. The `github/codeql-action/init` action will automatically detect the file and use it

d) By explicitly providing the configuration file path in the `config-file` input parameter of the `github/codeql-action/init` action

A:: <span style="color: #f800f8">**Answer:** D</span>

By explicitly providing the configuration file path in the `config-file` input parameter of the `github/codeql-action/init` action

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#using-a-custom-configuration-file

Q:: Where can you specify the CodeQL queries to run in a GitHub Actions workflow? (Choose two.)

a) In the `codeql` field of the `.github/settings.yml` file

b) In the Code Scanning section of the Security tab in the repository

c) In a CodeQL configuration YAML file

d) In the `queries` input parameter of the `github/codeql-action/init` action

e) In the `paths` input parameter of the `github/codeql-action/queries` action

A:: <span style="color: #f800f8">**Answer(s): D, C</span>

In the `queries` input parameter of the `github/codeql-action/init` action; In a CodeQL configuration YAML file

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#running-additional-queries

Q:: What is the purpose of the `external-repository-token` parameter in `github/codeql-action/init` GitHub Action?

a) It allows the action to upload the generated CodeQL database to a private GitHub repository.

b) It allows the action to access a private GitHub repository that contains configuration files, queries or packs that are required for the analysis.

c) It allows the action to upload the results of the analysis to a private GitHub repository.

d) It allows the action to access a private GitHub repository that contains the source code to be analyzed.

A:: <span style="color: #f800f8">**Answer:** B</span>

It allows the action to access a private GitHub repository that contains configuration files, queries or packs that are required for the analysis.

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#using-queries-in-ql-packs

Q:: What CodeQL CLI command is used to create a CodeQL database?

a) `qlcli database create`

b) `codeql database create`

c) `ql database generate`

d) `gh codeql-database create`

A:: <span style="color: #f800f8">**Answer:** B</span>

`codeql database create`

Source: https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/preparing-your-code-for-codeql-analysis#running-codeql-database-create

Q:: What is the purpose of the `codeql database analyze` command in CodeQL CLI?

a) Analyzing a CodeQL database and uploading the results to GitHub.

b) Analyzing a CodeQL database, producing results usually in the form of a SARIF file.

c) Analyzing a CodeQL database, producing results usually in the form of security advisories.

d) Analyzing the source code, producing a CodeQL database.

A:: <span style="color: #f800f8">**Answer:** B</span>

Analyzing a CodeQL database, producing results usually in the form of a SARIF file.

Source: https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/analyzing-your-code-with-codeql-queries#running-codeql-database-analyze

Q:: As part of your Jenkins CI pipeline you've successfully created and then analyzed a CodeQL database, therefore producing a SARIF file. How can you upload the SARIF file to GitHub? (Choose two.)

a) By committing the SARIF file to the GitHub repository

b) Using the `github/codeql-action/upload-sarif` GitHub Action

c) Using the GitHub REST API `POST /repos/{owner}/{repo}/code-scanning/sarifs` endpoint

d) Using the `gh codeql upload-results` command from GitHub CLI

e) Using the `codeql github upload-results` command from CodeQL CLI

A:: <span style="color: #f800f8">**Answer(s): E, C</span>

Using the `codeql github upload-results` command from CodeQL CLI; Using the GitHub REST API `POST /repos/{owner}/{repo}/code-scanning/sarifs` endpoint

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/uploading-a-sarif-file-to-github#about-sarif-file-uploads-for-code-scanning

Q:: What details can you find on a code scanning alert page? (Choose three.)

a) Information how many times the vulnerability has been exploited

b) Highlighted vulnerable code

c) Branches affected by the vulnerability

d) Severity of the vulnerability

e) ID of the CodeQL database that was used to find the vulnerability

f) Assigned developer to fix the vulnerability

A:: <span style="color: #f800f8">**Answer(s): C, B, D</span>

Branches affected by the vulnerability; Highlighted vulnerable code; Severity of the vulnerability

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/about-code-scanning-alerts#about-alert-details

Q:: Which of these statements regarding viewing the results of a CodeQL analysis are true? (Choose two.)

a) Anyone with read permission for a repository can see code scanning annotations on pull requests.

b) Anyone with read permissions for a repository can view code scanning alerts in the Security tab.

c) You need write permission to view a summary of all the alerts for a repository in the Security tab.

d) You need write permission to view code scanning annotations on pull requests.

e) Only the repository owner can see the code scanning alerts in the Security tab.

A:: <span style="color: #f800f8">**Answer(s): C, A</span>

You need write permission to view a summary of all the alerts for a repository in the Security tab.; Anyone with read permission for a repository can see code scanning annotations on pull requests.

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/managing-code-scanning-alerts-for-your-repository#viewing-the-alerts-for-a-repository

Q:: When a CodeQL analysis GitHub Actions workflow detects a new vulnerability on a pull request, where can you find the information about that vulnerability?

a) In the workflow run logs

b) The CodeQL analysis workflow will fail and produce an artifact with the results

c) Directly in the pull request in the form of a PR comment and a check failure

d) In the security tab of the repository

A:: <span style="color: #f800f8">**Answer:** C</span>

Directly in the pull request in the form of a PR comment and a check failure

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/triaging-code-scanning-alerts-in-pull-requests#about-code-scanning-results-on-pull-requests

Q:: When viewing a code scanning alert what is the `Show paths` option used for?

a) It will show recommendations on how to fix the vulnerability

b) It will display the path through the code that leads to the issue causing the alert.

c) It's used for showing the paths to the CodeQL queries that were used to find the vulnerability

d) It's used for showing the file path to the CodeQL database that was used to find the vulnerability

A:: <span style="color: #f800f8">**Answer:** B</span>

It will display the path through the code that leads to the issue causing the alert.

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/managing-code-scanning-alerts-for-your-repository#viewing-the-alerts-for-a-repository

Q:: What does it mean to dismiss a code scanning alert?

a) Closing an alert that you don't think needs to be fixed

b) Closing the alert after fixing the vulnerability in the code

A:: <span style="color: #f800f8">**Answer:** A</span>

Closing an alert that you don't think needs to be fixed

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/managing-code-scanning-alerts-for-your-repository#dismissing--alerts1. [x] Single-Choice Correct Answer

Q:: Which of these is NOT a valid approach one can take to reduce the time it takes for CodeQL analysis workflow to complete?

a) Parallelize the analysis for multi-language codebases

b) Reduce the number of queries that are run

c) Run the analysis on every push event

d) Ignore irrelevant files and directories from the analysis

e) Use runners with more CPU/RAM resources

A:: <span style="color: #f800f8">**Answer:** C</span>

Run the analysis on every push event

Source: https://docs.github.com/en/code-security/code-scanning/troubleshooting-code-scanning/analysis-takes-too-long

Q:: What is the purpose of defining a SARIF category?

a) Use a different category for each file that has been analyzed to easily track back the vulnerabilities to the files that contain them.

b) Use the category to distinguish files that contain vulnerabilities from files that do not contain vulnerabilities.

c) Use the category to distinguish between multiple analyses for the same tool or commit, but performed on different languages or different parts of the code.

d) Use the category to distinguish files that have been analyzed from files that have not been analyzed.

A:: <span style="color: #f800f8">**Answer:** C</span>

Use the category to distinguish between multiple analyses for the same tool or commit, but performed on different languages or different parts of the code.

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/sarif-support-for-code-scanning#uploading-more-than-one-sarif-file-for-a-commit

Q:: How can you enable GitHub Advanced Security features on GitHub Enterprise Server? (Choose two.)

a) By connecting directly to the GitHub Enterprise Server instance through SSH and using the administrative shell `ghe-config` commands.

b) By setting the `github.advanced_security.enabled` configuration option to `true` in the `config.yml` file in the `.github` repository.

c) In the Security tab of the Site admin management console

d) By requesting an upgrade from GitHub Support

e) By setting the `github.advanced_security.enabled` configuration option to `true` in the `config.yml` file in the `/etc/github` directory on the GitHub Enterprise Server instance.

A:: <span style="color: #f800f8">**Answer(s): C, A</span>

In the Security tab of the Site admin management console; By connecting directly to the GitHub Enterprise Server instance through SSH and using the administrative shell `ghe-config` commands.

Source: https://docs.github.com/en/enterprise-server@3.3/admin/code-security/managing-github-advanced-security-for-your-enterprise/enabling-github-advanced-security-for-your-enterprise

Q:: How can you enable GitHub Advanced Security features for all repositories in an organization in GitHub Enterprise Cloud?

a) By requesting an upgrade from GitHub Support

b) In the Site admin page of your enterprise account

c) In `Code security and analysis` section of the organization settings

d) By connecting directly to the GitHub Enterprise Cloud instance through SSH and using the administrative shell `ghe-config` commands.

A:: <span style="color: #f800f8">**Answer:** C</span>

In `Code security and analysis` section of the organization settings

Source: https://docs.github.com/en/enterprise-cloud@latest/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/managing-security-and-analysis-settings-for-your-organization#enabling-or-disabling-a-feature-for-all-existing-repositories

Q:: As a repository maintainer where should you put instructions on how to report a security vulnerability in your codebase?

a) In the `SECURITY.md` file

b) In the `CODE_OF_CONDUCT.md` file

c) In the `CONTRIBUTING.md` file

d) In the `README.md` file

A:: <span style="color: #f800f8">**Answer:** A</span>

In the `SECURITY.md` file

Source: https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository#about-security-policies

Q:: What is a GitHub security policy?

a) It's a tool for automatically fixing security vulnerabilities in your code.

b) A GitHub security policy is a subscription service that provides antivirus protection for your projects.

c) It's a document that instructs users on how to responsibly report security vulnerabilities in a project. It's typically defined in a `SECURITY.md` file in a repository.

d) It's a feature that allows you to encrypt your repository.

A:: <span style="color: #f800f8">**Answer:** C</span>

It's a document that instructs users on how to responsibly report security vulnerabilities in a project. It's typically defined in a `SECURITY.md` file in a repository.

Source: https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository#about-security-policies

Q:: How can you set a default security policy for all repositories in `my-org` GitHub Organization?

a) You can set a default security policy for all repositories in `my-org` GitHub Organization by adding a `SECURITY.md` file to each individual repository.

b) By editing the security policy in the organization's `Code Security and analysis` settings

c) Default security policies can only be set by GitHub support

d) By creating a `SECURITY.md` file in the `my-org/.github` repository

A:: <span style="color: #f800f8">**Answer:** D</span>

By creating a `SECURITY.md` file in the `my-org/.github` repository

Source: https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file#supported-file-types

Q:: Which API endpoint can be used to retrieve a list of all Dependabot alerts for an enterprise?

a) `GET /enterprises/{enterprise}/dependabot/alerts`

b) `GET /repos/{owner}/{repo}/dependabot/alerts`

c) `GET /github/{enterprise}/dependabot/alerts`

d) `GET /orgs/{org}/dependabot/alerts`

A:: <span style="color: #f800f8">**Answer:** A</span>

`GET /enterprises/{enterprise}/dependabot/alerts`

Source: https://docs.github.com/en/rest/dependabot/alerts?apiVersion=2022-11-28#list-dependabot-alerts-for-an-enterprise

Q:: Which API endpoint can be used to retrieve a list of all secret scanning alerts for an organization?

a) `GET /repos/{owner}/{repo}/secret-scanning/alerts`

b) `GET /github/{org}/secret-scanning/alerts`

c) `GET /orgs/{org}/secret-scanning/alerts`

d) `GET /enterprises/{enterprise}/secret-scanning/alerts`

A:: <span style="color: #f800f8">**Answer:** C</span>

`GET /orgs/{org}/secret-scanning/alerts`

Source: https://docs.github.com/en/rest/secret-scanning/secret-scanning?apiVersion=2022-11-28#list-secret-scanning-alerts-for-an-organization

Q:: Which API endpoint can be used to retrieve a list of all code scanning alerts for a repository?

a) `GET /github/{repo}/code-scanning/alerts`

b) `GET /repos/{owner}/{repo}/code-scanning/alerts`

c) `GET /orgs/{org}/{repo}/code-scanning/alerts`

d) `GET /{enterprise}/{org}/{repo}/code-scanning/alerts`

A:: <span style="color: #f800f8">**Answer:** B</span>

`GET /repos/{owner}/{repo}/code-scanning/alerts`

Source: https://docs.github.com/en/rest/code-scanning/code-scanning?apiVersion=2022-11-28#list-code-scanning-alerts-for-a-repository

Q:: Which of these statements best defines a vulnerable dependency?

a) A vulnerable dependency is dependency that a project relies on, which is not verified by GitHub.

b) A vulnerable dependency is dependency that a project relies on, which contains security flaws that could potentially be exploited, compromising the project's security.

c) A vulnerable dependency is dependency that a project relies on, which has not been updated in a long time.

d) A vulnerable dependency is dependency that a project relies on, which is not widely used or popular.

A:: <span style="color: #f800f8">**Answer:** B</span>

A vulnerable dependency is dependency that a project relies on, which contains security flaws that could potentially be exploited, compromising the project's security.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts

Q:: What are Dependabot security updates?

a) It's a Dependabot feature that automatically creates pull requests to update vulnerable dependencies in your repository.

b) It's a Dependabot feature that creates a list of vulnerable dependencies in your repository.

c) It's a Dependabot feature that automatically creates pull requests to update dependencies in your repository when they release a new version.

d) It's a Dependabot feature that creates alerts when a security vulnerability is detected in one of your dependencies.

A:: <span style="color: #f800f8">**Answer:** A</span>

It's a Dependabot feature that automatically creates pull requests to update vulnerable dependencies in your repository.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-security-updates/about-dependabot-security-updates

Q:: Dependabot Alerts are enabled by default on:

a) Only public repositories.

b) All repositories.

c) Only private repositories.

d) Dependabot Alerts are not enabled by default on any repositories.

A:: <span style="color: #f800f8">**Answer:** D</span>

Dependabot Alerts are not enabled by default on any repositories.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts#configuration-of-dependabot-alerts

Q:: Who can enable Dependabot alerts on a repository?

a) Only the repository owner

b) Dependabot alerts are enabled on all repositories by GitHub and can't be disabled or enabled by any individual.

c) Dependabot alerts are enabled by adding a GitHub Action to the repository, so anyone with write access to the repository can enable them.

d) Repository owners and people with admin access

A:: <span style="color: #f800f8">**Answer:** D</span>

Repository owners and people with admin access

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts#configuration-of-dependabot-alerts

Q:: What's the lowest access level needed to see Dependabot alerts in a repository within an organization?

a) Admin

b) Read

c) Write

d) Maintain

e) Triage

A:: <span style="color: #f800f8">**Answer:** C</span>

Write

Source: https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/repository-roles-for-an-organization#access-requirements-for-security-features

Q:: To enable Dependabot Alerts on all repositories in an organization you should:

a) On all repositories in the organization - run the `actions/enable-ghas` GitHub Action with `alerts` parameter set to `true`

b) Make all repositories in the organization private.

c) Go to the organization's `Code security and analysis` settings and enable Dependabot Alerts for all repositories at once.

d) Create a script that will enable Dependabot Alerts on all repositories in the organization.

A:: <span style="color: #f800f8">**Answer:** C</span>

Go to the organization's `Code security and analysis` settings and enable Dependabot Alerts for all repositories at once.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/configuring-dependabot-alerts#enabling-or-disabling-dependabot-alerts-for-all-existing-repositories

Q:: Which of these is a valid `dependabot.yml` configuration file?

a) Code block (yaml):
version: 2
    config:
    - package-ecosystem: "npm"
        directory: "/"
        schedule:
          interval: "daily"

b) Code block (yaml):
version: 2
    updates:
    - package-ecosystem: "npm"
        directory: "/"
        schedule:
          interval: "daily"

c) Code block (yaml):
version: 2
    updates:
    - package-ecosystem: "npm"
        directory: "/"
        schedule:
          interval: "everyday"

d) Code block (yaml):
version: 2
    config:
    - directory: "/"
        schedule:
          interval: "daily"

A:: <span style="color: #f800f8">**Answer:** B</span>

Code block (yaml):
version: 2
    updates:
    - package-ecosystem: "npm"
        directory: "/"
        schedule:
          interval: "daily"

Source: https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file

Q:: Which of these is not a GitHub supported channel for receiving Dependabot alerts?

a) SMS/Call

b) GitHub Mobile

c) github.com notification inbox

d) Email

e) GitHub CLI

A:: <span style="color: #f800f8">**Answer:** A</span>

SMS/Call

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/configuring-notifications-for-dependabot-alerts#configuring-notifications-for-dependabot-alerts

Q:: What are Dependabot auto-triage rules?

a) Auto-triage rules are defined in the `dependabot.yml` configuration file to specify which package managers should be used to scan your project for vulnerabilities.

b) Auto triage rules define how often Dependabot should scan your project for vulnerabilities.

c) It's a feature that allows Dependabot to automatically dismiss Dependabot alerts that match certain criteria.

d) Dependabot auto-triage rules are used for automatically deleting old dependencies in your project.

A:: <span style="color: #f800f8">**Answer:** C</span>

It's a feature that allows Dependabot to automatically dismiss Dependabot alerts that match certain criteria.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-auto-triage-rules/about-dependabot-auto-triage-rules

Q:: How can you automate dismissing low severity Dependabot alerts?

a) By setting the `severity` field in `dependabot.yml` file to high

b) By using Dependabot's auto-triage rules.

c) By setting the `dismiss-severity` field in `dependabot.yml` file to low

d) By removing all dependencies that cause low severity alerts

A:: <span style="color: #f800f8">**Answer:** B</span>

By using Dependabot's auto-triage rules.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-auto-triage-rules/about-dependabot-auto-triage-rules

Q:: To enable Dependabot security updates on all repositories in an organization you should:

a) Make all repositories in the organization private.

b) Run the `actions/enable-ghas` GitHub Action with `security-updates` parameter set to `true` on all repositories in the organization.

c) Go to the organization's `Code security and analysis` settings and enable Dependabot Security Updates for all repositories at once.

d) Create a script that will enable Dependabot Security Updates on all repositories in the organization.

A:: <span style="color: #f800f8">**Answer:** C</span>

Go to the organization's `Code security and analysis` settings and enable Dependabot Security Updates for all repositories at once.

Source: https://docs.github.com/en/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/managing-security-and-analysis-settings-for-your-organization#enabling-or-disabling-a-feature-for-all-existing-repositories

Q:: The tool that checks if a pull request introduces any dependencies with security vulnerabilities is called:

a) Dependency Review

b) Dependabot Alerts

c) Dependabot Security Updates

d) Dependabot Version Updates

A:: <span style="color: #f800f8">**Answer:** A</span>

Dependency Review

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-dependency-review

Q:: You need GitHub Actions enabled for

a) Dependabot Security Updates

b) Dependency Review

c) Dependabot Version Updates

d) All of these

e) None of these

A:: <span style="color: #f800f8">**Answer:** B</span>

Dependency Review

Source: https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/about-dependabot-version-updates#about-dependabot-version-updates

Q:: What does `CVSS` stand for?

a) `Cybersecurity Validation Scoring Scheme`

b) `Common Vulnerability Scoring System`

c) `Code Verification Security System`

d) `Critical Vulnerability Scanning Service`

A:: <span style="color: #f800f8">**Answer:** B</span>

`Common Vulnerability Scoring System`

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/about-code-scanning-alerts#about-alert-severity-and-security-severity-levels

Q:: What does `CVE` stand for?

a) `Common Vulnerabilities and Exposures`

b) `Common Virus Elimination`

c) `Cybersecurity Verification Entity`

d) `Code Validation and Enumeration`

A:: <span style="color: #f800f8">**Answer:** A</span>

`Common Vulnerabilities and Exposures`

Source: https://docs.github.com/en/code-security/security-advisories/working-with-repository-security-advisories/about-repository-security-advisories#cve-identification-numbers

Q:: What does `CWE` stand for?

a) `Cybersecurity Weakness Enumeration`

b) `Critical Web Elements`

c) `Code Wrapping Engine`

d) `Common Weakness Enumeration`

A:: <span style="color: #f800f8">**Answer:** D</span>

`Common Weakness Enumeration`

Source: https://cwe.mitre.org/

Q:: Which Dependabot comment command will get a pull request successfully completed?

a) `@dependabot close`

b) `@dependabot cancel merge`

c) `@dependabot merge`

d) `@dependabot rebase`

A:: <span style="color: #f800f8">**Answer:** C</span>

`@dependabot merge`

Source: https://docs.github.com/en/code-security/dependabot/working-with-dependabot/managing-pull-requests-for-dependency-updates#managing-dependabot-pull-requests-with-comment-commands

Q:: Jobs that run on macOS runners that GitHub hosts consume minutes at __ rate as Linux runners consume

a) the same

b) 2x

c) 5x

d) 10x

A:: <span style="color: #f800f8">**Answer:** D</span>

10x

Source: https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions#minute-multipliers


