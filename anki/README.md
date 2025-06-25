# MGAS - Github advanced security - microsoft learn

## Questions

### Part I - Github Advanced Security Part 1 Of 2

#### Chapter 1 - 1 Introduction To Github Advanced Security

Q:: What is the fundamental shift in security philosophy that GitHub Advanced Security (GHAS) promotes, moving away from traditional methods?
A:: GHAS shifts security from being a final, separate step (like an inspection after a building is finished) to an integrated, continuous process built into every stage of development. This "shift-left" approach makes finding and fixing vulnerabilities faster, cheaper, and less disruptive.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/4-respond-to-security-alerts)

Q:: In the analogy of building a house, what role does Code Scanning play, and why is this role most effective early in the construction process?
A:: Code Scanning acts as the "blueprint inspector." It's most effective early because it finds structural weaknesses (vulnerabilities) in the code (the "blueprints") *before* they are built into the final product. Fixing a flaw on paper is much easier and cheaper than fixing a crack in the foundation of a finished house.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/4-respond-to-security-alerts)

Q:: Which GitHub Advanced Security feature is specifically designed to act as a "password guard," preventing sensitive information like API keys or passwords from being accidentally left in the code?
A:: Secret Scanning. Its job is to detect and even block commits that contain secrets, ensuring they don't become part of the project's public history.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/2-what-is-github-advanced-security)

Q:: How do the Dependency Graph and Dependabot work together to secure a project's software supply chain?
A:: The Dependency Graph acts as a complete "parts list" for the software. Dependabot reads this list and cross-references it with the GitHub Advisory Database (a list of known vulnerabilities) to check for any unsafe parts. If a match is found, it raises an alert, much like a safety recall notice for a faulty car part.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/3-create-culture-around-security)

Q:: At what specific point in a developer's workflow does GitHub Advanced Security typically intervene to check for vulnerabilities?
A:: GHAS intervenes when a developer submits new code in a "pull request," *before* it is merged into the main project. This allows developers to see and fix security issues immediately within their normal workflow, while the context is still fresh in their minds.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/4-respond-to-security-alerts)

Q:: Why is it a security risk for a project to have outdated dependencies?
A:: Outdated dependencies are a risk because new vulnerabilities are constantly being discovered in software components. An old version of a component might contain a known security flaw that attackers can exploit. Dependabot helps mitigate this risk by flagging outdated dependencies that have known security advisories.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/3-create-culture-around-security)

Q:: (Cloze) To secure a project, GHAS uses Code Scanning to inspect the {{c1::code's blueprints}}, Secret Scanning to protect {{c2::secrets}}, and Dependabot to manage the security of its {{c3::dependencies}}.
A:: (Cloze) To secure a project, GHAS uses Code Scanning to inspect the code's blueprints (for vulnerabilities), Secret Scanning to protect secrets (like passwords and keys), and Dependabot to manage the security of its dependencies (third-party parts).
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/6-summary)

#### Chapter 2 - 2 Configure Dependabot Security Updates On Your Github Repo

Q:: Why is it crucial for a developer to manage not just the direct dependencies they choose, but also the indirect dependencies they don't?
A:: A project's security is only as strong as its weakest link. An indirect dependency (a "part-of-a-part") can contain a vulnerability, and even if you didn't choose it directly, it's still running in your software. Failing to track and update these hidden dependencies can leave a significant security hole.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/2-manage-your-dependencies-github)

Q:: What is the key difference in function between Dependabot and Dependency Review when securing a project's dependencies?
A:: Dependency Review is **proactive**; it acts as a "gatekeeper" on pull requests to *prevent* new vulnerable dependencies from being introduced. Dependabot is **reactive**; it acts as a "recall manager" for dependencies *already in* the project, alerting you when an existing part is found to be unsafe.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/6-dependency-review)

Q:: What are the two primary events that will trigger Dependabot to generate a new security alert for your repository?
A:: An alert is generated when: 1) A new vulnerability affecting one of your existing dependencies is published to the GitHub Advisory Database, or 2) You add a new dependency to your project, which is then scanned and found to have a pre-existing vulnerability.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/3-dependabot-alerts)

Q:: Using the analogy of building a car, what is the difference between a direct and an indirect dependency?
A:: A **direct dependency** is a major component you explicitly choose, like selecting an engine from Ford. An **indirect dependency** is a component that comes included with your choice, like the specific spark plugs inside that Ford engine, which you did not select yourself.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/2-manage-your-dependencies-github)

Q:: For Dependabot security updates to be enabled automatically on a repository for free, what condition must that repository meet?
A:: The repository must be public. This feature is provided by GitHub to help secure the open-source software ecosystem.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/4-dependabot-security-updates)

Q:: To manage your workflow in the security notifications inbox, what search query would you use to filter the view to show only the alerts that you have already processed and marked as resolved?
A:: You would use the search filter `is:done`. This helps organize the inbox by separating active alerts from those that have already been handled.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/5-manage-dependabot-notifications-reporting)

Q:: What is the primary source of information that Dependabot cross-references with your project's "parts list" (manifest) to identify security vulnerabilities?
A:: The GitHub Advisory Database. This is a comprehensive, constantly updated global database of known security vulnerabilities in software packages.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/3-dependabot-alerts)

#### Chapter 3 - 3 Configure And Use Secret Scanning In Your Github Repository

Q:: What is the primary difference in how standard Secret Scanning and "Push Protection" operate when a developer tries to commit code containing a secret?
A:: Standard Secret Scanning is **reactive**; it finds and alerts you about a secret *after* it has been committed. Push Protection is **proactive**; it acts as a gatekeeper that *blocks* the developer from committing the code in the first place, preventing the secret from ever entering the repository's history.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/4-use-secret-scanning)

Q:: Why are the settings for Secret Scanning locked and unchangeable on a public repository?
A:: The settings are locked because GitHub provides Secret Scanning as a free, standardized service to protect the entire public open-source community. This ensures a consistent baseline of security for all public projects. To gain control over the settings, the repository must be private and have a GitHub Advanced Security license.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/3-configure-secret-scanning)

Q:: When Secret Scanning finds a potential secret, what additional, crucial information does the "Validity Check" feature provide to help you prioritize your response?
A:: The Validity Check confirms whether the discovered secret is still **active** and can actually be used to access a service. This helps you prioritize alerts, allowing you to immediately address the most critical, live credentials over old, expired ones.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/4-use-secret-scanning)

Q:: What specific problem do "custom patterns" solve for an organization?
A:: They solve the problem of an organization using unique, internal secret formats that the default scanner wouldn't recognize. Custom patterns allow you to "teach" the scanner what your company-specific secrets look like, extending its detection capabilities beyond common, public service tokens.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/3-configure-secret-scanning)

Q:: The "security guard" analogy for Secret Scanning highlights that it searches more than just the current code. What other parts of a repository does it inspect?
A:: It inspects the project's entire history, developer notes (in "issues" and "pull requests"), and public comments. This comprehensive search ensures that secrets aren't hiding anywhere within the repository's data.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/2-what-is-secret-scanning)

Q:: To ensure the correct security team is notified when a secret is found, where in the repository settings must you go to configure the list of alert recipients?
A:: You must go to the **Advanced Security settings** of the repository. This is the central location for managing the configuration of all advanced security features, including who receives alerts.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/4-use-secret-scanning)

Q:: (Cloze) For a single organization, you can define up to {{c1::500 custom patterns}} to extend Secret Scanning's capabilities to find unique, internally-defined credentials.
A:: (Cloze) For a single organization, you can define up to 500 custom patterns to extend Secret Scanning's capabilities to find unique, internally-defined credentials.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/3-configure-secret-scanning)


#### Chapter 4 - 4 Configure Code Scanning On Github

Q:: What is the strategic difference between using a **triggered** code scan versus a **scheduled** code scan?
A:: A **triggered** scan provides immediate feedback on new changes (like in a pull request), catching vulnerabilities the moment they are introduced. A **scheduled** scan provides a periodic, comprehensive review of the entire codebase, which is useful for finding existing issues and checking against the very latest security rules.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/4-configure-code-scanning)

Q:: What is the purpose of the SARIF file format in the context of GitHub Code Scanning?
A:: SARIF acts as a standardized "inspection report." Its purpose is to provide a common format for any analysis tool (whether it's GitHub's native CodeQL or a third-party tool) to report its findings. This allows GitHub to ingest and display results from many different sources in one unified security interface.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/3-enable-code-scanning-with-third-party-tools)

Q:: In the code scanning process, what is the fundamental difference between a tool like `ESLint` and a tool like `GitHub Actions`?
A:: A tool like `ESLint` is an **analyzer** that *creates* the inspection report (the SARIF file) by checking the code for issues. `GitHub Actions` is a **delivery mechanism** or orchestrator that *runs the analyzer and uploads* that report to GitHub so the results can be displayed. One generates the findings, the other delivers them.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/3-enable-code-scanning-with-third-party-tools)

Q:: In the context of GitHub's native code scanning, what is the role of CodeQL?
A:: CodeQL is the powerful analysis engine that acts as GitHub's own native "code inspector." It treats code as data and queries it to find security vulnerabilities and coding errors, generating the results that are then displayed as code scanning alerts.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/2-what-code-scanning)

Q:: How does integrating Code Scanning into a pull request workflow prevent security issues from reaching the main codebase?
A:: By automatically scanning the code within a pull request *before* it is merged, it acts as an automated quality gate. It presents any discovered vulnerabilities directly to the developer in their workflow, allowing them to fix the issue immediately, thus preventing the flawed code from ever being integrated into the main branch.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/4-configure-code-scanning)

Q:: Besides using GitHub Actions and the CodeQL CLI, what is the third primary method for uploading a SARIF file to GitHub?
A:: The code scanning API. This method is used for programmatic or custom integrations where an external system needs to push analysis results directly to GitHub without using a standard workflow or command-line tool.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/3-enable-code-scanning-with-third-party-tools)

### Part II - Github Advanced Security Part 2 Of 2

#### Chapter 1 - 1 Identify Security Vulnerabilities In Your Codebase By Using Codeql

Q:: Using the "code detective" analogy, what are the three fundamental steps a developer must perform when using the CodeQL CLI to investigate a codebase?
A:: The three steps are: 1) **Create a database** to organize the code into a searchable format, 2) **Run queries** to ask specific questions and look for patterns, and 3) **Analyze the results** to identify vulnerabilities.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/2-how-prepare-database-codeql)

Q:: Why is the initial step of "creating a database" so crucial for CodeQL's analysis, rather than simply searching the raw code files?
A:: Creating a database transforms the raw code into a structured, relational model. This allows CodeQL to understand the relationships between different parts of the code (like data flow and function calls), enabling it to find complex vulnerabilities that a simple text search would miss.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/2-how-prepare-database-codeql)

Q:: What is a CodeQL "query," and what is its role in the security analysis process?
A:: A CodeQL query is a question written in a special language that is used to "ask" the CodeQL database for specific code patterns. Its role is to act as the detective's instruction, guiding the search for known types of vulnerabilities, bugs, or other errors.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/3-run-codeql-database)

Q:: In an automated pull request check, what is the function of the default failure threshold, and which severity level triggers it?
A:: The function is to act as an automated quality gate that prevents code with significant issues from being merged into the main branch. By default, this check is triggered to fail if CodeQL finds any problem with a severity level of **Error**.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/4-understand-results)

Q:: What is the most direct way to optimize a slow CodeQL analysis without changing the amount of code being scanned?
A:: The most direct way is to increase the system resources available to the analysis, specifically by **increasing the memory (RAM)** and/or the number of CPU cores. More resources allow the CodeQL engine to process the database and queries more quickly.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/5-troubleshoot-your-results)

Q:: (Cloze) The hierarchical command structure for using the CodeQL command-line tool follows the format codeql {{c1::[command]}} {{c2::[subcommand]}}.
A:: (Cloze) The hierarchical command structure for using the CodeQL command-line tool follows the format codeql [command] [subcommand].
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/3-run-codeql-database)

#### Chapter 2 - 2 Code Scanning With Github Codeql

Q:: What is the key philosophical difference between the QL language and a standard imperative language like Python?
A:: QL is **declarative**, meaning you describe *what* pattern you want to find, not the step-by-step process of *how* to find it. This makes it highly optimized for finding complex relationships and data-flow patterns in code, which is ideal for security analysis.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/4-what-is-ql)

Q:: Briefly describe the three distinct stages CodeQL uses to transform raw source code into an actionable security alert.
A:: 1) **Database Creation:** It first extracts the code into a structured, relational database. 2) **Query Execution:** It runs queries (the inspection rules) against this database to find patterns. 3) **Result Interpretation:** It translates the raw query results into user-friendly alerts that pinpoint the exact location and nature of the potential issue.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/3-how-does-codeql-analyze-code)

Q:: What key capabilities does a custom `codeql-config.yml` file offer that make it more powerful than simply adding queries directly to a workflow file?
A:: A custom configuration file allows for more advanced control, such as **disabling the default queries**, specifying files or directories to **ignore** during a scan, and excluding specific unwanted rules from the default set.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/6-customize-your-scanning-workflow-with-codeql)

Q:: For a repository containing both Python and JavaScript, what feature can you use to optimize the CodeQL scanning time, and what principle does it operate on?
A:: You can use a **language matrix** in the GitHub Actions workflow. It operates on the principle of **parallelization**, running two separate analysis jobs (one for Python, one for JavaScript) at the same time, which is significantly faster than running them sequentially.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/10-custom-build-steps-for-code-scanning)

Q:: When does CodeQL's `autobuild` feature typically fail, and what must a developer provide in the workflow to overcome this failure for compiled languages?
A:: The `autobuild` feature typically fails when a project has a complex, non-standard, or unique build process. To overcome this, the developer must provide their own **custom build steps** in the workflow file, explicitly telling CodeQL how to compile the code before it can be analyzed.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/10-custom-build-steps-for-code-scanning)

Q:: (Cloze) To achieve advanced customization, such as disabling default queries or ignoring specific directories, you would use a dedicated {{c1::custom configuration file}} instead of modifying the main workflow.
A:: (Cloze) To achieve advanced customization, such as disabling default queries or ignoring specific directories, you would use a dedicated custom configuration file (or codeql-config.yml file) instead of modifying the main workflow.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/6-customize-your-scanning-workflow-with-codeql)

#### Chapter 3 - 3 Github Administration For Github Advanced Security

Q:: What is the core principle of the "shift-left" philosophy, and how does GitHub Advanced Security (GHAS) facilitate it?
A:: The "shift-left" philosophy is about integrating security checks early in the development timeline, rather than leaving them for the end. GHAS facilitates this by providing automated security tools (like Code and Secret Scanning) that run directly in the developer's workflow, making security a continuous and proactive part of development.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/2-what-is-github-advanced-security)

Q:: Why is the Security Overview dashboard a feature exclusive to GHAS licenses and not available on individual public repositories?
A:: The Security Overview is an organizational management tool designed to give a high-level, aggregate view of security risks across *many* repositories. This function is specific to the needs of a managed organization, whereas features like Code Scanning directly benefit the security of a single public project.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/5-manage-github-advanced-security-features-alerts)

Q:: As a GitHub administrator, where would you navigate to enable GitHub Advanced Security for all new repositories across your entire organization?
A:: You would navigate to the organization's settings and find the **Code security and analysis** section. This is the central control panel for enabling and managing GHAS features at the organizational level.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/3-enable-github-advanced-security)

Q:: What is the most effective administrative mechanism for ensuring consistent adoption and usage of security tools across all teams in an organization?
A:: The most effective mechanism is to **set a security policy at the organization level**. This allows an administrator to centrally enable or require specific security features for all or a subset of repositories, ensuring a consistent security posture without manual intervention on each project.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/4-manage-access-github-advanced-security)

Q:: When configuring a security workflow in GitHub Actions, what is the critical security principle you should apply to the `GITHUB_TOKEN`?
A:: You must apply the **principle of least privilege** by correctly setting up the permissions for the `GITHUB_TOKEN`. The token should only be granted the minimum permissions necessary for the workflow to complete its job, which reduces the potential risk if the workflow were ever compromised.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/5-manage-github-advanced-security-features-alerts)

Q:: (Cloze) To enforce the use of GHAS features across your company, you can create organization-wide {{c1::security policies}}.
A:: (Cloze) To enforce the use of GHAS features across your company, you can create organization-wide security policies.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/4-manage-access-github-advanced-security)

#### Chapter 4 - 4 Manage Sensitive Data And Security Policies Within Github

Q:: What is the primary purpose of a `SECURITY.md` file, and how does it differ from a `CONTRIBUTING.md` file?
A:: The `SECURITY.md` file's purpose is to provide a clear, responsible disclosure policy, detailing which project versions are supported and how to privately report vulnerabilities. This is distinct from a `CONTRIBUTING.md` file, which provides instructions for developers on how to contribute code to the project.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/2-set-security-policies)

Q:: How does a tool like Dependabot embody the principle of security automation within a project's lifecycle?
A:: Dependabot embodies automation by continuously and automatically monitoring a project's third-party dependencies for known vulnerabilities. Instead of requiring manual, periodic checks, it proactively alerts developers and often creates pull requests with fixes, integrating security maintenance directly into the development workflow.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/3-scrub-sensitive-data-from-repository)

Q:: To enable users to effectively assess their risk, what two critical pieces of information must a well-formed security advisory contain?
A:: It must contain the **product and versions affected** (so users know if they are impacted) and the **severity level** of the vulnerability (so they know how urgently they need to act).
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/4-report-logs)

Q:: During a security incident investigation, what two fundamental questions about any event does the GitHub audit log help you answer?
A:: The audit log answers "who" (**the user that performed the action**) and "when" (**the date and time of the action**). This is crucial for establishing a timeline of events and attributing actions to specific users.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/4-report-logs)

Q:: If you discover that sensitive data has been accidentally committed to a repository, which GitHub administrative tool is essential for tracing how and when it was introduced?
A:: The **audit log**. It provides a detailed, time-stamped record of all repository actions, allowing you to identify the specific user and commit that introduced the sensitive data, which is the critical first step in the incident response process.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/4-report-logs)

Q:: (Cloze) To communicate security policies, such as supported versions and how to report a flaw, you should create a {{c1::SECURITY.md}} file in your repository.
A:: (Cloze) To communicate security policies, such as supported versions and how to report a flaw, you should create a SECURITY.md file in your repository.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/2-set-security-policies)

### Part III - Extra: GitHub Certified Advanced Security

#### Chapter 1 - Exam preparation questions

Q:: What is CodeQL?

a) A code analysis tool

b) A programming language

c) A text editor

d) A version control system

A:: **Answer:** A

A code analysis tool

Source: https://codeql.github.com/

Q:: What does `shifting left` mean in the context of Security?

a) Adopting security practices early in the development cycle

b) Writing code in a language that is commonly used

c) Incorporating security practices right before hitting production

d) Writing code without worrying about security

A:: **Answer:** A

Adopting security practices early in the development cycle

Source: https://github.com/readme/guides/github-advanced-security-telus

Q:: What are Repository Security Advisories?

a) A private space where repository maintainers can discuss vulnerabilities and security issues within the codebase.

b) GitHub security experts that help GitHub Enterprise users with their security issues.

c) A list of security issues that are publicly available for anyone to see and stay away from.

d) It's a place to gather and publicly discuss security issues in the open source community.

A:: **Answer:** A

A private space where repository maintainers can discuss vulnerabilities and security issues within the codebase.

Source: https://docs.github.com/en/code-security/security-advisories/working-with-repository-security-advisories/about-repository-security-advisories

Q:: Which tool helps you keep the repository dependencies up to date?

a) Dependabot

b) Security Advisories

c) CodeQL

d) GitHub Actions

A:: **Answer:** A

Dependabot

Source: https://docs.github.com/en/code-security/dependabot

Q:: Which of the following is a curated list of security vulnerabilities found in open source projects?

a) GitHub Advisory Database

b) CodeQL

c) Dependabot

d) GitHub Security Journal

A:: **Answer:** A

GitHub Advisory Database

Source: https://docs.github.com/en/code-security/security-advisories/working-with-global-security-advisories-from-the-github-advisory-database/about-the-github-advisory-database

Q:: Which of these GitHub security features are available for FREE for both public and private personal repositories? (Choose four.)

a) Security Policy

b) Security advisories

c) Dependabot alerts and security updates

d) Dependabot version updates

e) Dependabot code scanning

f) Dependabot secret scanning

g) Secret scanning

h) Code scanning

A:: **Answer(s):** A, B, C, D

Security Policy; Security advisories; Dependabot alerts and security updates; Dependabot version updates

Source: https://docs.github.com/en/code-security/getting-started/github-security-features

Q:: Which of these best describes secret scanning?

a) Secret scanning scans your repository for secrets such as private keys or tokens.

b) Secret scanning scans your repository for potential code vulnerabilities that could expose secrets such as private keys or tokens.

c) Secret scanning is a tool for secure secret storage and management.

d) Secret scanning is a git hook that will scan your commits for secrets such as private keys or tokens before they are pushed to GitHub.

A:: **Answer:** A

Secret scanning scans your repository for secrets such as private keys or tokens.

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning

Q:: Which parts of the repository are scanned by secret scanning? (Choose two.)

a) Entire git history on all branches in the repository

b) Titles, descriptions and comments in open and closed historical issues

c) GitHub Repository secrets

d) GitHub Environment secrets

e) Entire git history on all protected branches in the repository

A:: **Answer(s):** A, B

Entire git history on all branches in the repository; Titles, descriptions and comments in open and closed historical issues

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning#about-secret-scanning, https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-a-repository, https://docs.github.com/en/actions/security-guides/using-secrets-in-github-actions#creating-secrets-for-an-environment

Q:: What's the purpose of the Secret scanning partner program?

a) Service Providers can partner with GitHub so that the format of their secrets can be recognized by GitHub secret scanning.

b) GitHub Partner program allows enterprises and organizations with GitHub Advanced Security license to use GitHub secret scanning to scan their repositories.

c) GitHub partners with external security companies to provide secret scanning for GitHub repositories.

d) It's a program where registered security professionals can in good faith report to GitHub any secrets they find in GitHub repositories and get paid rewards for it.

A:: **Answer:** A

Service Providers can partner with GitHub so that the format of their secrets can be recognized by GitHub secret scanning.

Source: https://docs.github.com/en/code-security/secret-scanning/secret-scanning-partner-program

Q:: Public repositories owned by personal users as well as public repositories owned by organizations can use secret scanning for free.

a) True

b) False

A:: **Answer:** A

True

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning#about-secret-scanning

Q:: How can you prevent commits containing cloud provider credentials from being pushed to GitHub?

a) Enable a secret scanning push protection rule for your repository or organization.

b) Include a `.gitignore` file in your repository that will ignore files containing secrets.

c) Create a GitHub Action that will scan your commits for secrets before they are pushed to GitHub.

d) Enable a branch protection rule for your repository.

A:: **Answer:** A

Enable a secret scanning push protection rule for your repository or organization.

Source: https://docs.github.com/en/code-security/secret-scanning/push-protection-for-repositories-and-organizations

Q:: Which of these is true about the GitHub secret scanning partner program? (Choose three.)

a) It is a program where service providers can provide GitHub with the regex patterns of secrets that they issue so GitHub secret scanning can recognize them.

b) When GitHub identifies a secret from a partnered service provider, it notifies the service provider about the leaked secret.

c) The partner can take actions upon receiving notification from GitHub about a leaked secret, such as revoking the secret and informing the owner of the compromised secret.

d) It grants the partner access to the secret GitHub scanning API so that the service provider can scan GitHub repositories for secrets that match their format.

e) GitHub has the ability to automatically revoke leaked secrets and notify the service provider that they have been invalidated by GitHub.

A:: **Answer(s):** A, B, C

It is a program where service providers can provide GitHub with the regex patterns of secrets that they issue so GitHub secret scanning can recognize them.; When GitHub identifies a secret from a partnered service provider, it notifies the service provider about the leaked secret.; The partner can take actions upon receiving notification from GitHub about a leaked secret, such as revoking the secret and informing the owner of the compromised secret.

Source: https://docs.github.com/en/code-security/secret-scanning/secret-scanning-partner-program

Q:: How can you exclude certain directories or files from secret scanning?

a) By creating a `secret_scanning.yml` file and including paths that should not be scanned

b) It's not possible to exclude specific files and/or directories from being scanned. Once you enable secret scanning for a repository, all files and directories will be scanned.

c) Include these files in the `.gitignore` file

d) By creating a `dependabot.yml` file and including paths which should not be scanned

A:: **Answer:** A

By creating a `secret_scanning.yml` file and including paths that should not be scanned

Source: https://docs.github.com/en/code-security/secret-scanning/configuring-secret-scanning-for-your-repositories#excluding-directories-from-secret-scanning-alerts-for-users

Q:: You have included some fake secrets in your test code and they have been picked up by GitHub's secret scanning. What can you do to tell GitHub that these are fake secrets used in tests and can be ignored by secret scanning? (Choose two.)

a) By creating a `secret_scanning.yml` file within which you declare paths where fake secrets are located, so scans will omit them

b) Close the Secret Scanning Alert with `Used in tests` close reason

c) In your test files, add a comment `#gh_ignore: fake secret` on the line where the fake secret is located.

d) By creating a `.github/codeql.yml` file within which you declare paths where fake secrets are located, so scans will omit them

A:: **Answer(s):** A, B

By creating a `secret_scanning.yml` file within which you declare paths where fake secrets are located, so scans will omit them; Close the Secret Scanning Alert with `Used in tests` close reason

Source: https://docs.github.com/en/code-security/secret-scanning/using-advanced-secret-scanning-and-push-protection-features/excluding-folders-and-files-from-secret-scanning

Q:: You have accidentally committed your GitHub personal access token to a public repository. What actions should you take to prevent your account from being compromised?

a) Consider the token compromised and delete it immediately

b) Change the token's permissions to read-only

c) Overwrite the git history to mask the token

d) Check if this token is used in any of your applications, if so - delete it.

A:: **Answer:** A

Consider the token compromised and delete it immediately

Source: https://docs.github.com/en/code-security/secret-scanning/managing-alerts-from-secret-scanning#securing-compromised-secrets

Q:: What is the behavior when a new secret pattern is added or updated in the GitHub secret scanning partner program?

a) GitHub will run a scan of all historical code content in public repositories with secret scanning enabled

b) GitHub will only scan for the new pattern in newly pushed commits in repositories with secret scanning enabled. If a secret of that pattern was already present in the repository, it will not be detected.

c) The GitHub partner has to deal with the historically leaked secrets and GitHub will only scan any new commits for the new pattern

d) GitHub will create an issue in all repositories with secret scanning enabled so the maintainers can check the repository for any secrets matching the new pattern

A:: **Answer:** A

GitHub will run a scan of all historical code content in public repositories with secret scanning enabled

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning#accessing-secret-scanning-alerts

Q:: Who will be notified when a NEW secret is pushed and detected in a repository? (Choose five.)

a) Repository Administrators

b) Security Managers

c) Users with custom roles with read/write access

d) Organization owners and enterprise owners, but only if they are administrators of repositories where secrets were leaked

e) Commit authors

f) Everyone with write access to the repository

g) All Organization owners and enterprise owners

A:: **Answer(s):** A, B, C, D, E

Repository Administrators; Security Managers; Users with custom roles with read/write access; Organization owners and enterprise owners, but only if they are administrators of repositories where secrets were leaked; Commit authors

Source: https://docs.github.com/en/code-security/secret-scanning/managing-alerts-from-secret-scanning/monitoring-alerts#incremental-scans

Q:: When GitHub runs a scan of all historical code in enterprise repositories what is the notification behavior? (Select two.)

a) GitHub notifies the enterprise owners and security managers, even if no secrets are found.

b) GitHub notifies Repository administrators, security managers, and users with custom roles with read/write access whenever a secret is detected in a repository.

c) GitHub notifies the enterprise owners and security managers, only if it detects exposed secrets.

d) GitHub notifies the commit authors of the commits that contain exposed secrets.

A:: **Answer(s):** A, B

GitHub notifies the enterprise owners and security managers, even if no secrets are found.; GitHub notifies Repository administrators, security managers, and users with custom roles with read/write access whenever a secret is detected in a repository.

Source: https://docs.github.com/en/code-security/secret-scanning/managing-alerts-from-secret-scanning/monitoring-alerts#historical-scans

Q:: Does GitHub use the same set of secret scanning patterns for both user alerts and push protection alerts?

a) No, these are different sets of secret patterns

b) Yes, its the same set of secret patterns

A:: **Answer:** A

No, these are different sets of secret patterns

Source: https://docs.github.com/en/code-security/secret-scanning/secret-scanning-patterns#about-secret-scanning-patterns

Q:: What are the three different sets of secret scanning patterns that GitHub maintains? (Select three.)

a) Partner patterns

b) User alert patterns

c) Push protection patterns

d) Enterprise alert patterns

e) Open source alert patterns

f) Cloud provider patterns

A:: **Answer(s):** A, B, C

Partner patterns; User alert patterns; Push protection patterns

Source: https://docs.github.com/en/code-security/secret-scanning/secret-scanning-patterns#about-secret-scanning-patterns

Q:: Multiple public repositories that you are contributing to do not have secret scanning push protection option enabled. What can you do to protect yourself from accidentally pushing secrets to these repositories?

a) Enable `Push protection for yourself`, in your personal GitHub account settings

b) Download the GitHub push protection web plugin

c) It's not possible, push protection has to be enabled on any of repository, organization or enterprise level

d) Add the files containing secrets to `.gitignore` file in all of the repositories

A:: **Answer:** A

Enable `Push protection for yourself`, in your personal GitHub account settings

Source: https://docs.github.com/en/code-security/secret-scanning/push-protection-for-users#about-push-protection-for-users

Q:: Your company has internal secrets that should not be pushed to GitHub repositories. The pattern of these secrets is not known by GitHub and therefore is not detected by secret scanning. What can companies do to protect their developers from accidentally pushing these secrets to repositories in their GitHub Organization?

a) Define regex patterns for these secrets and enable custom patterns for secret scanning for the organization.

b) The company should join the GitHub partner program so the pattern of the companies secrets is recognized.

c) Define custom GitHub Actions workflows for repositories in the organization that will scan for these secrets.

d) In all repositories include `secret_scanning.yml` file which will define these custom secrets that should be scanned for.

A:: **Answer:** A

Define regex patterns for these secrets and enable custom patterns for secret scanning for the organization.

Source: https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/defining-custom-patterns-for-secret-scanning#defining-a-custom-pattern-for-an-organization

Q:: What information do Dependabot alerts provide?

a) Dependabot alerts tell you that your repository uses a package that is insecure.

b) Dependabot alerts tell you that your repository is being used by other public repositories.

c) Dependabot alerts tell you that your repository uses an untested version of a package.

d) Dependabot alerts tell you that your repository uses an outdated version of a package

A:: **Answer:** A

Dependabot alerts tell you that your repository uses a package that is insecure.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts

Q:: What is the GitHub dependency graph?

a) It is a representation of a repository's dependencies and dependents.

b) There is no such thing as the GitHub dependency graph.

c) It is a tool that automatically proposes version updates to dependencies in a repository.

d) It is a GitHub maintained list of known vulnerabilities in open source software packages.

A:: **Answer:** A

It is a representation of a repository's dependencies and dependents.

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph

Q:: Is GitHub dependency graph available for free to all repositories?

a) Yes, it's available for free for all repositories.

b) No, it's available for free for public repositories only. Private repositories can use it if they have the GitHub Advanced Security license.

A:: **Answer:** A

Yes, it's available for free for all repositories.

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph#dependency-graph-availability

Q:: How does GitHub Dependency graph know what dependencies your project is using? (Choose two.)

a) GitHub derives dependencies automatically from manifests and lock files committed to the repository

b) Dependencies can be manually added using the Dependency submission API

c) GitHub scans the repository code for import statements of external packages

d) It's required to add a GitHub Actions workflow that uses the official `actions/dependency-graph` GitHub Action to add dependencies to the graph whenever a new commit is pushed to the repository

A:: **Answer(s):** A, B

GitHub derives dependencies automatically from manifests and lock files committed to the repository; Dependencies can be manually added using the Dependency submission API

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph#supported-package-ecosystems

Q:: When will the GitHub Dependency graph for your repository be updated? (Choose two.)

a) When anyone pushes a change to the repository of one of your dependencies.

b) When you push a commit to the repository's default branch, only if that changes or adds a supported manifest/lockfile.

c) When you push any commit to the repository's default branch.

d) When your repository publishes a new release.

e) When your repository publishes a new git tag.

f) When the GitHub Actions workflow that uses the `actions/dependency-graph` GitHub Action is triggered.

A:: **Answer(s):** A, B

When anyone pushes a change to the repository of one of your dependencies.; When you push a commit to the repository's default branch, only if that changes or adds a supported manifest/lockfile.

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-supply-chain-security#what-is-the-dependency-graph

Q:: In what format can you export the GitHub Dependency graph of your repository?

a) SPDX

b) YAML

c) JSON

d) XML

e) CSV

A:: **Answer:** A

SPDX

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/exporting-a-software-bill-of-materials-for-your-repository

Q:: Can your repository use Dependency Graph without using Dependabot Alerts?

a) Yes

b) No

A:: **Answer:** A

Yes

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph#using-the-dependency-graph

Q:: Which feature is a pre-requisite for using Dependabot Alerts on a repository?

a) Dependency graph

b) Dependency review

c) Dependency security updates

d) Dependency version updates

A:: **Answer:** A

Dependency graph

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph#using-the-dependency-graph

Q:: Which of these statements about Dependabot Alerts are true? (Choose three.)

a) They partially rely on the GitHub Advisory Database

b) To enable Dependabot Alerts you first need to have Dependency Graph enabled on your repository

c) When GitHub identifies a vulnerable dependency, they generate a Dependabot alert and display it on the Security tab for the repository

d) Dependabot Alerts are enabled by default for all repositories

e) Dependabot Alerts are enabled by default for all public repositories

f) Dependabot alerts tell you that your repository uses an outdated version of a package

A:: **Answer(s):** A, B, C

They partially rely on the GitHub Advisory Database; To enable Dependabot Alerts you first need to have Dependency Graph enabled on your repository; When GitHub identifies a vulnerable dependency, they generate a Dependabot alert and display it on the Security tab for the repository

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts

Q:: What are the primary benefits of the Security Overview feature in GitHub?

a) Centralized view of security alerts and policy management in an organization

b) Automatic code review for every push

c) Real-time threat detection

d) Automated dependency updates

A:: **Answer:** A

Centralized view of security alerts and policy management in an organization

Source: https://docs.github.com/en/code-security/security-overview/about-security-overview

Q:: What is CodeQL?

a) A code analysis engine developed by GitHub

b) A new programming language for security analysis

c) A database used to store code scanning results

d) A third-party tool for static code analysis

A:: **Answer:** A

A code analysis engine developed by GitHub

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql#about-code-scanning-with-codeql

Q:: What do Dependabot alerts indicate in GitHub?

a) The presence of a vulnerable dependency or malware in your repository

b) Outdated dependencies that need to be updated

c) Errors in dependency configuration files

d) Conflicts between different dependencies

A:: **Answer:** A

The presence of a vulnerable dependency or malware in your repository

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts#about-dependabot-alerts

Q:: What is the purpose of code scanning in GitHub?

a) To identify vulnerabilities and errors in code

b) To check code formatting and style

c) To review pull requests automatically

d) To synchronize code with production servers

A:: **Answer:** A

To identify vulnerabilities and errors in code

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning#about-code-scanning

Q:: Is secret scanning available for both public and private repositories on GitHub?

a) Yes, but for private repositories, it requires a license for GitHub Advanced Security

b) Yes, with no additional requirements

c) No, it is only available for public repositories

d) No, it is only available for private repositories

A:: **Answer:** A

Yes, but for private repositories, it requires a license for GitHub Advanced Security

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning#about-secret-scanning

Q:: What does the default CodeQL analysis setup in GitHub do?

a) Automatically chooses languages to analyze, query suite to run, and events that trigger scans

b) Manually requires users to specify languages and queries for each scan

c) Scans code only on a monthly basis

d) Requires separate installation of third-party scanning tools

A:: **Answer:** A

Automatically chooses languages to analyze, query suite to run, and events that trigger scans

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql#about-code-scanning-with-codeql

Q:: What is the main purpose of using the CodeQL CLI?

a) To generate a database representation of a codebase, a CodeQL database

b) To manage repository settings and permissions

c) To schedule regular maintenance tasks in a repository

d) To automatically merge pull requests

A:: **Answer:** A

To generate a database representation of a codebase, a CodeQL database

Source: https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/about-the-codeql-cli#about-the-codeql-cli

Q:: Which of the following languages is NOT supported by CodeQL for code scanning?

a) PHP

b) JavaScript/TypeScript

c) C/C++

d) Python

A:: **Answer:** A

PHP

Source: https://codeql.github.com/docs/codeql-overview/supported-languages-and-frameworks/#languages-and-compilers

Q:: How does CodeQL analyze code in GitHub?

a) It generates a CodeQL database and runs queries to identify problems, displaying results as code scanning alerts

b) It uses machine learning to predict potential vulnerabilities based on past commits

c) It performs manual code reviews submitted by GitHub community members

d) It relies solely on third-party tools for code analysis

A:: **Answer:** A

It generates a CodeQL database and runs queries to identify problems, displaying results as code scanning alerts

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql#about-codeql

Q:: How can CodeQL be used in an external CI system together with GitHub repositories?

a) Run CodeQL CLI in the external CI system to scan code and upload the results to the GitHub repository

b) CodeQL cannot be used in external CI systems; it is exclusive to GitHub Actions

c) Upload source code to GitHub for analysis and then download results for use in the CI system

d) Manually run CodeQL locally and email the results to the GitHub repository administrators

A:: **Answer:** A

Run CodeQL CLI in the external CI system to scan code and upload the results to the GitHub repository

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#about-using-code-scanning-with-your-existing-ci-system

Q:: Which of these statements isn't true about secret scanning on GitHub?

a) Secret scanning is a tool for secure secret storage and management.

b) Secret scanning will scan your entire Git history on all branches present in your GitHub repository for secrets.

c) Secret scanning will scan titles, descriptions, and comments, in open and closed historical issues for secrets.

d) Secret scanning can prevent supported secrets from being pushed into your enterprise, organization, or repository.

A:: **Answer:** A

Secret scanning is a tool for secure secret storage and management.

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning

Q:: Which top-level keys are required in the `dependabot.yml` file?

a) `version` and `updates`

b) `version` and `package-ecosystem`

c) `assignees` and `directory`

d) `updates` and `directory`

A:: **Answer:** A

`version` and `updates`

Source: https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file#about-the-dependabotyml-file

Q:: Which GitHub Action can be used to upload a third-party SARIF file?

a) `github/codeql-action/upload-sarif`

b) `codeql-upload-sarif`

c) `github/codeql-action`

d) `actions/upload-sarif`

A:: **Answer:** A

`github/codeql-action/upload-sarif`

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/uploading-a-sarif-file-to-github#uploading-a-code-scanning-analysis-with-github-actions

Q:: Which tool can be used in a third-party CI system to upload code analysis results to GitHub?

a) CodeQL CLI

b) CodeQL API

c) GitHub Actions `github/codeql-action`

d) GitHub CLI

A:: **Answer:** A

CodeQL CLI

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#about-using-code-scanning-with-your-existing-ci-system

Q:: What is required for a CI server to upload SARIF results to GitHub?

a) A GitHub App or personal access token with `security_events` write permission.

b) A direct connection to the GitHub Advisory Database.

c) Administrator access to the GitHub repository.

d) A special plugin installed in the CI system.

A:: **Answer:** A

A GitHub App or personal access token with `security_events` write permission.

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#generating-a-token-for-authentication-with-github

Q:: What happens when a second SARIF results file is uploaded to GitHub for a single commit?

a) It replaces the original set of data.

b) It appends the results to the existing file.

c) It creates a new branch in the repository

d) It is ignored by GitHub.

A:: **Answer:** A

It replaces the original set of data.

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#uploading-your-results-to-github

Q:: How can users exclude specific directories from secret scanning alerts on GitHub?

a) By configuring a `secret_scanning.yml` file, under the `.github` path in the repository.

b) Through the repository's `Security` tab, in the `Secret scanning` menu.

c) Through the repository's `Settings` tab, in the `Code security and analysis` menu.

d) By editing the repository's `README.md` file.

A:: **Answer:** A

By configuring a `secret_scanning.yml` file, under the `.github` path in the repository.

Source: https://docs.github.com/en/code-security/secret-scanning/configuring-secret-scanning-for-your-repositories#excluding-directories-from-secret-scanning-alerts-for-users

Q:: Which key should be used in a `secret_scanning.yml` file to exclude directories from secret scanning alerts in GitHub?

a) `paths-ignore:`

b) `paths-exclude:`

c) `ignore-directories`

d) `exclude-paths:`

A:: **Answer:** A

`paths-ignore:`

Source: https://docs.github.com/en/code-security/secret-scanning/configuring-secret-scanning-for-your-repositories#excluding-directories-from-secret-scanning-alerts-for-users

Q:: What is the maximum number of custom patterns that can be defined for secret scanning on GitHub?

a) 500 for organizations/enterprises and 100 for repositories.

b) 100 for organizations/enterprises and 500 for repositories.

c) 100 for organizations, enterprises and repositories.

d) There's no limit to the number of custom patterns you can define for secret scanning in GitHub.

A:: **Answer:** A

500 for organizations/enterprises and 100 for repositories.

Source: https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/defining-custom-patterns-for-secret-scanning#about-custom-patterns-for-secret-scanning

Q:: Fill in the blank: `GitHub __________ is a feature that you can use to analyze code in a GitHub repository to find security vulnerabilities and coding errors.`

a) Code Scanning

b) Dependency Graph

c) Security Advisories

d) Vulnerability Detection

A:: **Answer:** A

Code Scanning

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning

Q:: Which GitHub Advanced Security feature allows you to find, triage, and prioritize fixes for new and existing problems in your code?

a) Code scanning

b) Dependabot alerts

c) Security policies

d) Security advisories

A:: **Answer:** A

Code scanning

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning

Q:: How can you enable code scanning for a repository?

a) Go to the security tab of the repository settings and enable code scanning with default or advanced setup.

b) Go to your user settings and enable code scanning, you can choose to enable it for all or only selected repositories.

c) Add a `.github/codeql.yml`configuration file to the repository.

d) Go to the security tab of the repository settings and answer a questionnaire about the repository contents. Based on the answers, GitHub will enable code scanning with the appropriate configuration.

A:: **Answer:** A

Go to the security tab of the repository settings and enable code scanning with default or advanced setup.

Source: https://docs.github.com/en/code-security/code-scanning/enabling-code-scanning/configuring-default-setup-for-code-scanning

Q:: How can you configure your GitHub repository to run CodeQL analysis on a schedule? (Choose two.)

a) By creating a GitHub Actions workflow with a `schedule` trigger. The workflow should leverage actions from the `github/codeql-action` repository.

b) By using the default CodeQL analysis setup.

c) By setting the `codeql.trigger` property in the repository settings to `schedule`.

d) By adding a `schedule` property to the `.github/codeql.yml` configuration file.

e) By raising a request with GitHub support to enable scheduled CodeQL analysis for the repository.

A:: **Answer(s):** A, B

By creating a GitHub Actions workflow with a `schedule` trigger. The workflow should leverage actions from the `github/codeql-action` repository.; By using the default CodeQL analysis setup.

Source: https://docs.github.com/en/code-security/code-scanning/enabling-code-scanning/configuring-default-setup-for-code-scanning#about-default-setup

Q:: An organization has recently started using CodeQL analysis for all pull requests on their repositories as well as running the analysis on an hourly schedule. Since then they are experiencing larger than usual GitHub Actions bills. What is the most likely cause of this?

a) Code scanning uses GitHub Actions and the organization is being billed for the additional usage.

b) The code scanning analysis is finding more issues than expected and is taking longer to complete.

c) Code scanning can only be run on a daily schedule and the organization is being billed for the additional usage.

d) There is no correlation between code scanning and GitHub Actions billing. The organization is being billed for other GitHub Actions workflows.

A:: **Answer:** A

Code scanning uses GitHub Actions and the organization is being billed for the additional usage.

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning#about-billing-for-code-scanning

Q:: If you don't want to use GitHub Actions, you can run code scanning in an external CI system, then upload the results to GitHub.

a) True

b) False

A:: **Answer:** A

True

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#about-using-code-scanning-with-your-existing-ci-system

Q:: When using a third party CI system to run code scanning, what GitHub tool do you need to analyze the codebase?

a) You don't specifically need a GitHub tool, any static analysis tool that can produce results in SARIF format will work.

b) You need to install the GitHub Code Scanning tool.

c) You need to install CodeQL CLI

d) You need to install GitHub CLI

A:: **Answer:** A

You don't specifically need a GitHub tool, any static analysis tool that can produce results in SARIF format will work.

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system#about-using-code-scanning-with-your-existing-ci-system

Q:: When using GitHub Actions as your CI system and a third party tool to run code scanning, how can you upload the SARIF results to GitHub?

a) By using the `github/codeql-action/upload-sarif` GitHub Action

b) When using GitHub Actions the SARIF results are automatically uploaded to GitHub.

c) You can only use CodeQL when running code scanning in GitHub Actions. Third party code scanning tools are not supported.

d) By using the `actions/upload-artifact` GitHub Action

A:: **Answer:** A

By using the `github/codeql-action/upload-sarif` GitHub Action

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/uploading-a-sarif-file-to-github#uploading-a-code-scanning-analysis-with-github-actions

Q:: Can you use CodeQL analysis with third party CI systems?

a) Yes, you just need to use the CodeQL CLI

b) No, because it requires using the `github/codeql-action` GitHub Action

A:: **Answer:** A

Yes, you just need to use the CodeQL CLI

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/using-code-scanning-with-your-existing-ci-system

Q:: Which of these is true about code scanning? (Choose two.)

a) Code scanning helps finding insecure code patterns which can be missed by manual code review.

b) Code scanning can be integrated into the CI pipeline to find security issues early in the development process.

c) Code scanning is a replacement for manual code review.

d) Code scanning helps finding any leaked credentials in the codebase such as API keys or cloud credentials.

e) Code scanning scans your code to search for all dependencies and their versions to find any vulnerable dependencies.

A:: **Answer(s):** A, B

Code scanning helps finding insecure code patterns which can be missed by manual code review.; Code scanning can be integrated into the CI pipeline to find security issues early in the development process.

Source: https://docs.github.com/en/code-security/supply-chain-security/end-to-end-supply-chain/securing-code#scan-your-code-for-vulnerable-patterns

Q:: When using CodeQL analysis in your GitHub Actions workflow, how often is the scan triggered?

a) Code scanning can be triggered for many different events that happen in the repository.

b) Code scanning is triggered on every push to the repository.

c) Code scanning is triggered on a configurable schedule

d) Code scanning can be triggered on a configurable schedule or on pull requests.

A:: **Answer:** A

Code scanning can be triggered for many different events that happen in the repository.

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning#about-code-scanning

Q:: What is the effect of adding the `paths-ignore` keyword to your code scanning GitHub Actions workflow?

a) Avoiding unnecessary scans when files that are not relevant to the analysis are changed.

b) It tells CodeQL to omit all `*.txt` and `*.md` files from the analysis.

c) Preventing the CodeQL analysis from running on pull requests that change files with the specified extensions.

d) Pull request checks will ignore any CodeQL vulnerabilities that are found in `*.txt` and `*.md` files.

A:: **Answer:** A

Avoiding unnecessary scans when files that are not relevant to the analysis are changed.

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#avoiding-unnecessary-scans-of-pull-requests

Q:: CodeQL scanning supports:

a) Both compiled and interpreted languages

b) Only compiled languages

c) Only interpreted languages

d) All programming languages

A:: **Answer:** A

Both compiled and interpreted languages

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning-with-codeql#about-codeql

Q:: What are CodeQL queries used for?

a) CodeQL queries can be run against a CodeQL database to identify patterns that may indicate coding errors or security vulnerabilities.

b) CodeQL queries analyze your codebase and are used to create a CodeQL database.

c) CodeQL queries are used for code review purposes in GitHub.

d) CodeQL queries are text-based questions you can ask the CodeQL engine about your codebase.

A:: **Answer:** A

CodeQL queries can be run against a CodeQL database to identify patterns that may indicate coding errors or security vulnerabilities.

Source: https://codeql.github.com/docs/writing-codeql-queries/about-codeql-queries/

Q:: What is QL?

a) QL is a query language that underlies CodeQL

b) QL stands for Quality Level and is a metric used by CodeQL

c) QL is a similar product to CodeQL but is used for scanning text files instead of code

d) QL is a npm package that is used by CodeQL to scan code

A:: **Answer:** A

QL is a query language that underlies CodeQL

Source: https://codeql.github.com/docs/ql-language-reference/about-the-ql-language/

Q:: What is a CodeQL query suite?

a) CodeQL suite is a collections of CodeQL queries

b) CodeQL suite is a collection of CodeQL databases

c) CodeQL suite is a collection of CodeQL results

d) CodeQL suite is a collection of CodeQL supported languages

A:: **Answer:** A

CodeQL suite is a collections of CodeQL queries

Source: https://docs.github.com/en/code-security/code-scanning/managing-your-code-scanning-configuration/codeql-query-suites#about-codeql-query-suites

Q:: What are the different types of CodeQL packs? (Choose three.)

a) Query packs

b) Library packs

c) Model packs

d) Code packs

e) Language packs

f) Vulnerability packs

A:: **Answer(s):** A, B, C

Query packs; Library packs; Model packs

Source: https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/customizing-analysis-with-codeql-packs#about-codeql-packs

Q:: What is a CodeQL query pack?

a) It's a set of pre-compiled queries with all transitive dependencies such as libraries and models

b) It's a library used by CodeQL queries

c) It's a collection of CodeQL queries

d) It's a set of results that were generated in the process of analyzing a CodeQL database

A:: **Answer:** A

It's a set of pre-compiled queries with all transitive dependencies such as libraries and models

Source: https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/customizing-analysis-with-codeql-packs#about-codeql-packs

Q:: What are the steps of CodeQL analysis workflow?

a) Creating a CodeQL database -> Running CodeQL queries -> Interpreting the results

b) Running CodeQL queries -> Creating a CodeQL database -> Interpreting the results

c) Running CodeQL queries -> Interpreting the results

d) Creating a CodeQL database -> Interpreting the results -> Running CodeQL queries

A:: **Answer:** A

Creating a CodeQL database -> Running CodeQL queries -> Interpreting the results

Source: https://codeql.github.com/docs/codeql-overview/about-codeql/#codeql-analysis

Q:: What is extraction in the context of CodeQL code analysis?

a) Extraction is the process of creating a relational representation of each source file in the codebase.

b) Extraction is the action of running CodeQL queries against a CodeQL database and extracting the results.

c) Extraction is the process of creating CodeQL queries specific to the codebase.

d) Extraction is the process of exporting data from a CodeQL database.

A:: **Answer:** A

Extraction is the process of creating a relational representation of each source file in the codebase.

Source: https://codeql.github.com/docs/codeql-overview/about-codeql/#database-creation

Q:: Which of these statements are true regarding running CodeQL analysis on codebases with multiple programming languages? (Choose two.)

a) CodeQL uses a different extractor for each programming language

b) CodeQL creates separate databases for each programming language

c) CodeQL creates one database for all programming languages in the codebase, as long as they are supported by CodeQL

d) CodeQL database schema is the same for each programming language

A:: **Answer(s):** A, B

CodeQL uses a different extractor for each programming language; CodeQL creates separate databases for each programming language

Source: https://codeql.github.com/docs/codeql-overview/about-codeql/#database-creation

Q:: What are the differences when running CodeQL database creation for compiled and interpreted languages? (Choose two.)

a) For compiled languages, extraction works by monitoring the build process. All information is collected each time the compiler is invoked to process a source file.

b) For interpreted languages, the extractor runs directly on the source code.

c) For interpreted languages, extraction works by monitoring the build process. All information is collected each time the interpreter is invoked to process a source file.

d) For compiled languages, the extractor runs directly on the source code.

e) For compiled languages, the extractor runs on the executable file.

f) For interpreted languages, the extractor runs on the executable file.

A:: **Answer(s):** A, B

For compiled languages, extraction works by monitoring the build process. All information is collected each time the compiler is invoked to process a source file.; For interpreted languages, the extractor runs directly on the source code.

Source: https://codeql.github.com/docs/codeql-overview/about-codeql/#database-creation

Q:: Where can you see when the last CodeQL analysis was run when using the default code scanning setup?

a) In the code scanning tool status page

b) In repository insights

c) In the Dependabot tab

d) You can't see that information with the default setup

A:: **Answer:** A

In the code scanning tool status page

Source: https://docs.github.com/en/code-security/code-scanning/enabling-code-scanning/evaluating-default-setup-for-code-scanning#evaluating-code-scanning-with-the-tool-status-page

Q:: Which of the following statements about enabling CodeQL scanning default setup are true? (Choose three.)

a) You can enable default setup for all eligible repositories in an organization at once in the organization settings

b) GitHub Actions need to be enabled as a prerequisite

c) You can enable default setup on any repository, regardless of the contents of the repository

d) You can only enable default setup on repositories that contain at least one CodeQL-supported language

e) Default setup will scan the repository on a schedule that you can configure. For event based scanning, you need to configure a GitHub Action workflow

f) You can only use the default query suite with default CodeQL scanning setup

A:: **Answer(s):** A, B, C

You can enable default setup for all eligible repositories in an organization at once in the organization settings; GitHub Actions need to be enabled as a prerequisite; You can enable default setup on any repository, regardless of the contents of the repository

Source: https://docs.github.com/en/code-security/code-scanning/enabling-code-scanning/configuring-default-setup-for-code-scanning

Q:: How can you customize your advanced CodeQL scanning setup with additional CodeQL query suites? (Choose two.)

a) By using a custom configuration file and defining additional queries there

b) By defining the customizations in the CodeQL analysis GitHub Actions workflow as input parameters to the `github/codeql-action/init` action

c) By using the CodeQL CLI with a custom configuration file to run the analysis

d) By defining the customizations in the Security / Code scanning repository settings

e) By using the `github/codeql-customizations` GitHub Action

A:: **Answer(s):** A, B

By using a custom configuration file and defining additional queries there; By defining the customizations in the CodeQL analysis GitHub Actions workflow as input parameters to the `github/codeql-action/init` action

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning

Q:: When running CodeQL analysis in GitHub Actions, what Actions should you use? (Choose three.)

a) `github/codeql-action/init`

b) `github/codeql-action/analyze`

c) `github/codeql-action/autobuild` only for compiled programming languages

d) `github/codeql-action/autobuild`

e) `github/codeql-action/init` only for compiled programming languages

f) `github/codeql-action/analyze` only for interpreted programming languages

A:: **Answer(s):** A, B, C

`github/codeql-action/init`; `github/codeql-action/analyze`; `github/codeql-action/autobuild` only for compiled programming languages

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/codeql-code-scanning-for-compiled-languages#about-the-codeql-analysis-workflow-and-compiled-languages

Q:: What is the simplest method to execute CodeQL analysis concurrently for each language in a multi-language repository using GitHub Actions?

a) By creating a `languages` matrix for the job and then reference it in the `github/codeql-action/init` action's `languages` input parameter

b) By calling the `github/codeql-action/analyze` action in separate steps for each language

c) By creating a separate workflow for each language

d) Define the parallelism in the `github/codeql-action/analyze` action

A:: **Answer:** A

By creating a `languages` matrix for the job and then reference it in the `github/codeql-action/init` action's `languages` input parameter

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#changing-the-languages-that-are-analyzed

Q:: How can you use a custom CodeQL configuration file in a GitHub Actions workflow?

a) By explicitly providing the configuration file path in the `config-file` input parameter of the `github/codeql-action/init` action

b) By storing the configuration in `.github/codeql/config-config.yml` file. The `github/codeql-action/init` action will automatically detect the file and use it

c) By uploading that file in the Code Scanning section of the Security tab in the repository

d) By storing the configuration in `.github/workflows/codeql-analysis.yml` file. The `github/codeql-action/init` action will automatically detect the file and use it

A:: **Answer:** A

By explicitly providing the configuration file path in the `config-file` input parameter of the `github/codeql-action/init` action

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#using-a-custom-configuration-file

Q:: Where can you specify the CodeQL queries to run in a GitHub Actions workflow? (Choose two.)

a) In the `queries` input parameter of the `github/codeql-action/init` action

b) In a CodeQL configuration YAML file

c) In the `paths` input parameter of the `github/codeql-action/queries` action

d) In the Code Scanning section of the Security tab in the repository

e) In the `codeql` field of the `.github/settings.yml` file

A:: **Answer(s):** A, B

In the `queries` input parameter of the `github/codeql-action/init` action; In a CodeQL configuration YAML file

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#running-additional-queries

Q:: What is the purpose of the `external-repository-token` parameter in `github/codeql-action/init` GitHub Action?

a) It allows the action to access a private GitHub repository that contains configuration files, queries or packs that are required for the analysis.

b) It allows the action to upload the results of the analysis to a private GitHub repository.

c) It allows the action to access a private GitHub repository that contains the source code to be analyzed.

d) It allows the action to upload the generated CodeQL database to a private GitHub repository.

A:: **Answer:** A

It allows the action to access a private GitHub repository that contains configuration files, queries or packs that are required for the analysis.

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#using-queries-in-ql-packs

Q:: What CodeQL CLI command is used to create a CodeQL database?

a) `codeql database create`

b) `gh codeql-database create`

c) `ql database generate`

d) `qlcli database create`

A:: **Answer:** A

`codeql database create`

Source: https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/preparing-your-code-for-codeql-analysis#running-codeql-database-create

Q:: What is the purpose of the `codeql database analyze` command in CodeQL CLI?

a) Analyzing a CodeQL database, producing results usually in the form of a SARIF file.

b) Analyzing a CodeQL database, producing results usually in the form of security advisories.

c) Analyzing the source code, producing a CodeQL database.

d) Analyzing a CodeQL database and uploading the results to GitHub.

A:: **Answer:** A

Analyzing a CodeQL database, producing results usually in the form of a SARIF file.

Source: https://docs.github.com/en/code-security/codeql-cli/getting-started-with-the-codeql-cli/analyzing-your-code-with-codeql-queries#running-codeql-database-analyze

Q:: As part of your Jenkins CI pipeline you've successfully created and then analyzed a CodeQL database, therefore producing a SARIF file. How can you upload the SARIF file to GitHub? (Choose two.)

a) Using the `codeql github upload-results` command from CodeQL CLI

b) Using the GitHub REST API `POST /repos/{owner}/{repo}/code-scanning/sarifs` endpoint

c) Using the `gh codeql upload-results` command from GitHub CLI

d) By committing the SARIF file to the GitHub repository

e) Using the `github/codeql-action/upload-sarif` GitHub Action

A:: **Answer(s):** A, B

Using the `codeql github upload-results` command from CodeQL CLI; Using the GitHub REST API `POST /repos/{owner}/{repo}/code-scanning/sarifs` endpoint

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/uploading-a-sarif-file-to-github#about-sarif-file-uploads-for-code-scanning

Q:: What details can you find on a code scanning alert page? (Choose three.)

a) Branches affected by the vulnerability

b) Highlighted vulnerable code

c) Severity of the vulnerability

d) Information how many times the vulnerability has been exploited

e) Assigned developer to fix the vulnerability

f) ID of the CodeQL database that was used to find the vulnerability

A:: **Answer(s):** A, B, C

Branches affected by the vulnerability; Highlighted vulnerable code; Severity of the vulnerability

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/about-code-scanning-alerts#about-alert-details

Q:: Which of these statements regarding viewing the results of a CodeQL analysis are true? (Choose two.)

a) You need write permission to view a summary of all the alerts for a repository in the Security tab.

b) Anyone with read permission for a repository can see code scanning annotations on pull requests.

c) You need write permission to view code scanning annotations on pull requests.

d) Anyone with read permissions for a repository can view code scanning alerts in the Security tab.

e) Only the repository owner can see the code scanning alerts in the Security tab.

A:: **Answer(s):** A, B

You need write permission to view a summary of all the alerts for a repository in the Security tab.; Anyone with read permission for a repository can see code scanning annotations on pull requests.

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/managing-code-scanning-alerts-for-your-repository#viewing-the-alerts-for-a-repository

Q:: When a CodeQL analysis GitHub Actions workflow detects a new vulnerability on a pull request, where can you find the information about that vulnerability?

a) Directly in the pull request in the form of a PR comment and a check failure

b) In the security tab of the repository

c) In the workflow run logs

d) The CodeQL analysis workflow will fail and produce an artifact with the results

A:: **Answer:** A

Directly in the pull request in the form of a PR comment and a check failure

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/triaging-code-scanning-alerts-in-pull-requests#about-code-scanning-results-on-pull-requests

Q:: When viewing a code scanning alert what is the `Show paths` option used for?

a) It will display the path through the code that leads to the issue causing the alert.

b) It's used for showing the paths to the CodeQL queries that were used to find the vulnerability

c) It will show recommendations on how to fix the vulnerability

d) It's used for showing the file path to the CodeQL database that was used to find the vulnerability

A:: **Answer:** A

It will display the path through the code that leads to the issue causing the alert.

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/managing-code-scanning-alerts-for-your-repository#viewing-the-alerts-for-a-repository

Q:: What does it mean to dismiss a code scanning alert?

a) Closing an alert that you don't think needs to be fixed

b) Closing the alert after fixing the vulnerability in the code

A:: **Answer:** A

Closing an alert that you don't think needs to be fixed

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/managing-code-scanning-alerts-for-your-repository#dismissing--alerts1. [x] Single-Choice Correct Answer

Q:: Which of these is NOT a valid approach one can take to reduce the time it takes for CodeQL analysis workflow to complete?

a) Run the analysis on every push event

b) Use runners with more CPU/RAM resources

c) Parallelize the analysis for multi-language codebases

d) Ignore irrelevant files and directories from the analysis

e) Reduce the number of queries that are run

A:: **Answer:** A

Run the analysis on every push event

Source: https://docs.github.com/en/code-security/code-scanning/troubleshooting-code-scanning/analysis-takes-too-long

Q:: What is the purpose of defining a SARIF category?

a) Use the category to distinguish between multiple analyses for the same tool or commit, but performed on different languages or different parts of the code.

b) Use the category to distinguish files that have been analyzed from files that have not been analyzed.

c) Use the category to distinguish files that contain vulnerabilities from files that do not contain vulnerabilities.

d) Use a different category for each file that has been analyzed to easily track back the vulnerabilities to the files that contain them.

A:: **Answer:** A

Use the category to distinguish between multiple analyses for the same tool or commit, but performed on different languages or different parts of the code.

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/sarif-support-for-code-scanning#uploading-more-than-one-sarif-file-for-a-commit

Q:: How can you enable GitHub Advanced Security features on GitHub Enterprise Server? (Choose two.)

a) In the Security tab of the Site admin management console

b) By connecting directly to the GitHub Enterprise Server instance through SSH and using the administrative shell `ghe-config` commands.

c) By requesting an upgrade from GitHub Support

d) By setting the `github.advanced_security.enabled` configuration option to `true` in the `config.yml` file in the `/etc/github` directory on the GitHub Enterprise Server instance.

e) By setting the `github.advanced_security.enabled` configuration option to `true` in the `config.yml` file in the `.github` repository.

A:: **Answer(s):** A, B

In the Security tab of the Site admin management console; By connecting directly to the GitHub Enterprise Server instance through SSH and using the administrative shell `ghe-config` commands.

Source: https://docs.github.com/en/enterprise-server@3.3/admin/code-security/managing-github-advanced-security-for-your-enterprise/enabling-github-advanced-security-for-your-enterprise

Q:: How can you enable GitHub Advanced Security features for all repositories in an organization in GitHub Enterprise Cloud?

a) In `Code security and analysis` section of the organization settings

b) By connecting directly to the GitHub Enterprise Cloud instance through SSH and using the administrative shell `ghe-config` commands.

c) By requesting an upgrade from GitHub Support

d) In the Site admin page of your enterprise account

A:: **Answer:** A

In `Code security and analysis` section of the organization settings

Source: https://docs.github.com/en/enterprise-cloud@latest/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/managing-security-and-analysis-settings-for-your-organization#enabling-or-disabling-a-feature-for-all-existing-repositories

Q:: As a repository maintainer where should you put instructions on how to report a security vulnerability in your codebase?

a) In the `SECURITY.md` file

b) In the `CONTRIBUTING.md` file

c) In the `README.md` file

d) In the `CODE_OF_CONDUCT.md` file

A:: **Answer:** A

In the `SECURITY.md` file

Source: https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository#about-security-policies

Q:: What is a GitHub security policy?

a) It's a document that instructs users on how to responsibly report security vulnerabilities in a project. It's typically defined in a `SECURITY.md` file in a repository.

b) It's a tool for automatically fixing security vulnerabilities in your code.

c) It's a feature that allows you to encrypt your repository.

d) A GitHub security policy is a subscription service that provides antivirus protection for your projects.

A:: **Answer:** A

It's a document that instructs users on how to responsibly report security vulnerabilities in a project. It's typically defined in a `SECURITY.md` file in a repository.

Source: https://docs.github.com/en/code-security/getting-started/adding-a-security-policy-to-your-repository#about-security-policies

Q:: How can you set a default security policy for all repositories in `my-org` GitHub Organization?

a) By creating a `SECURITY.md` file in the `my-org/.github` repository

b) By editing the security policy in the organization's `Code Security and analysis` settings

c) Default security policies can only be set by GitHub support

d) You can set a default security policy for all repositories in `my-org` GitHub Organization by adding a `SECURITY.md` file to each individual repository.

A:: **Answer:** A

By creating a `SECURITY.md` file in the `my-org/.github` repository

Source: https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file#supported-file-types

Q:: Which API endpoint can be used to retrieve a list of all Dependabot alerts for an enterprise?

a) `GET /enterprises/{enterprise}/dependabot/alerts`

b) `GET /orgs/{org}/dependabot/alerts`

c) `GET /repos/{owner}/{repo}/dependabot/alerts`

d) `GET /github/{enterprise}/dependabot/alerts`

A:: **Answer:** A

`GET /enterprises/{enterprise}/dependabot/alerts`

Source: https://docs.github.com/en/rest/dependabot/alerts?apiVersion=2022-11-28#list-dependabot-alerts-for-an-enterprise

Q:: Which API endpoint can be used to retrieve a list of all secret scanning alerts for an organization?

a) `GET /orgs/{org}/secret-scanning/alerts`

b) `GET /enterprises/{enterprise}/secret-scanning/alerts`

c) `GET /repos/{owner}/{repo}/secret-scanning/alerts`

d) `GET /github/{org}/secret-scanning/alerts`

A:: **Answer:** A

`GET /orgs/{org}/secret-scanning/alerts`

Source: https://docs.github.com/en/rest/secret-scanning/secret-scanning?apiVersion=2022-11-28#list-secret-scanning-alerts-for-an-organization

Q:: Which API endpoint can be used to retrieve a list of all code scanning alerts for a repository?

a) `GET /repos/{owner}/{repo}/code-scanning/alerts`

b) `GET /orgs/{org}/{repo}/code-scanning/alerts`

c) `GET /{enterprise}/{org}/{repo}/code-scanning/alerts`

d) `GET /github/{repo}/code-scanning/alerts`

A:: **Answer:** A

`GET /repos/{owner}/{repo}/code-scanning/alerts`

Source: https://docs.github.com/en/rest/code-scanning/code-scanning?apiVersion=2022-11-28#list-code-scanning-alerts-for-a-repository

Q:: Which of these statements best defines a vulnerable dependency?

a) A vulnerable dependency is dependency that a project relies on, which contains security flaws that could potentially be exploited, compromising the project's security.

b) A vulnerable dependency is dependency that a project relies on, which has not been updated in a long time.

c) A vulnerable dependency is dependency that a project relies on, which is not widely used or popular.

d) A vulnerable dependency is dependency that a project relies on, which is not verified by GitHub.

A:: **Answer:** A

A vulnerable dependency is dependency that a project relies on, which contains security flaws that could potentially be exploited, compromising the project's security.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts

Q:: What are Dependabot security updates?

a) It's a Dependabot feature that automatically creates pull requests to update vulnerable dependencies in your repository.

b) It's a Dependabot feature that creates a list of vulnerable dependencies in your repository.

c) It's a Dependabot feature that creates alerts when a security vulnerability is detected in one of your dependencies.

d) It's a Dependabot feature that automatically creates pull requests to update dependencies in your repository when they release a new version.

A:: **Answer:** A

It's a Dependabot feature that automatically creates pull requests to update vulnerable dependencies in your repository.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-security-updates/about-dependabot-security-updates

Q:: Dependabot Alerts are enabled by default on:

a) Dependabot Alerts are not enabled by default on any repositories.

b) Only public repositories.

c) All repositories.

d) Only private repositories.

A:: **Answer:** A

Dependabot Alerts are not enabled by default on any repositories.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts#configuration-of-dependabot-alerts

Q:: Who can enable Dependabot alerts on a repository?

a) Repository owners and people with admin access

b) Only the repository owner

c) Dependabot alerts are enabled on all repositories by GitHub and can't be disabled or enabled by any individual.

d) Dependabot alerts are enabled by adding a GitHub Action to the repository, so anyone with write access to the repository can enable them.

A:: **Answer:** A

Repository owners and people with admin access

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/about-dependabot-alerts#configuration-of-dependabot-alerts

Q:: What's the lowest access level needed to see Dependabot alerts in a repository within an organization?

a) Write

b) Read

c) Maintain

d) Triage

e) Admin

A:: **Answer:** A

Write

Source: https://docs.github.com/en/organizations/managing-user-access-to-your-organizations-repositories/managing-repository-roles/repository-roles-for-an-organization#access-requirements-for-security-features

Q:: To enable Dependabot Alerts on all repositories in an organization you should:

a) Go to the organization's `Code security and analysis` settings and enable Dependabot Alerts for all repositories at once.

b) Make all repositories in the organization private.

c) On all repositories in the organization - run the `actions/enable-ghas` GitHub Action with `alerts` parameter set to `true`

d) Create a script that will enable Dependabot Alerts on all repositories in the organization.

A:: **Answer:** A

Go to the organization's `Code security and analysis` settings and enable Dependabot Alerts for all repositories at once.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/configuring-dependabot-alerts#enabling-or-disabling-dependabot-alerts-for-all-existing-repositories

Q:: Which of these is a valid `dependabot.yml` configuration file?

a) Code block (yaml):
version: 2
updates:
\- package-ecosystem: "npm"
directory: "/"
schedule:
interval: "daily"

b) Code block (yaml):
version: 2
config:
\- directory: "/"
schedule:
interval: "daily"

c) Code block (yaml):
version: 2
updates:
\- package-ecosystem: "npm"
directory: "/"
schedule:
interval: "everyday"

d) Code block (yaml):
version: 2
config:
\- package-ecosystem: "npm"
directory: "/"
schedule:
interval: "daily"

A:: **Answer:** A

Code block (yaml):
version: 2
updates:
\- package-ecosystem: "npm"
directory: "/"
schedule:
interval: "daily"

Source: https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file

Q:: Which of these is not a GitHub supported channel for receiving Dependabot alerts?

a) SMS/Call

b) github.com notification inbox

c) GitHub Mobile

d) GitHub CLI

e) Email

A:: **Answer:** A

SMS/Call

Source: https://docs.github.com/en/code-security/dependabot/dependabot-alerts/configuring-notifications-for-dependabot-alerts#configuring-notifications-for-dependabot-alerts

Q:: What are Dependabot auto-triage rules?

a) It's a feature that allows Dependabot to automatically dismiss Dependabot alerts that match certain criteria.

b) Auto-triage rules are defined in the `dependabot.yml` configuration file to specify which package managers should be used to scan your project for vulnerabilities.

c) Dependabot auto-triage rules are used for automatically deleting old dependencies in your project.

d) Auto triage rules define how often Dependabot should scan your project for vulnerabilities.

A:: **Answer:** A

It's a feature that allows Dependabot to automatically dismiss Dependabot alerts that match certain criteria.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-auto-triage-rules/about-dependabot-auto-triage-rules

Q:: How can you automate dismissing low severity Dependabot alerts?

a) By using Dependabot's auto-triage rules.

b) By setting the `severity` field in `dependabot.yml` file to high

c) By removing all dependencies that cause low severity alerts

d) By setting the `dismiss-severity` field in `dependabot.yml` file to low

A:: **Answer:** A

By using Dependabot's auto-triage rules.

Source: https://docs.github.com/en/code-security/dependabot/dependabot-auto-triage-rules/about-dependabot-auto-triage-rules

Q:: To enable Dependabot security updates on all repositories in an organization you should:

a) Go to the organization's `Code security and analysis` settings and enable Dependabot Security Updates for all repositories at once.

b) Make all repositories in the organization private.

c) Run the `actions/enable-ghas` GitHub Action with `security-updates` parameter set to `true` on all repositories in the organization.

d) Create a script that will enable Dependabot Security Updates on all repositories in the organization.

A:: **Answer:** A

Go to the organization's `Code security and analysis` settings and enable Dependabot Security Updates for all repositories at once.

Source: https://docs.github.com/en/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/managing-security-and-analysis-settings-for-your-organization#enabling-or-disabling-a-feature-for-all-existing-repositories

Q:: The tool that checks if a pull request introduces any dependencies with security vulnerabilities is called:

a) Dependency Review

b) Dependabot Alerts

c) Dependabot Security Updates

d) Dependabot Version Updates

A:: **Answer:** A

Dependency Review

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-dependency-review

Q:: You need GitHub Actions enabled for

a) Dependency Review

b) Dependabot Security Updates

c) Dependabot Version Updates

d) All of these

e) None of these

A:: **Answer:** A

Dependency Review

Source: https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/about-dependabot-version-updates#about-dependabot-version-updates

Q:: What does `CVSS` stand for?

a) `Common Vulnerability Scoring System`

b) `Code Verification Security System`

c) `Critical Vulnerability Scanning Service`

d) `Cybersecurity Validation Scoring Scheme`

A:: **Answer:** A

`Common Vulnerability Scoring System`

Source: https://docs.github.com/en/code-security/code-scanning/managing-code-scanning-alerts/about-code-scanning-alerts#about-alert-severity-and-security-severity-levels

Q:: What does `CVE` stand for?

a) `Common Vulnerabilities and Exposures`

b) `Common Virus Elimination`

c) `Cybersecurity Verification Entity`

d) `Code Validation and Enumeration`

A:: **Answer:** A

`Common Vulnerabilities and Exposures`

Source: https://docs.github.com/en/code-security/security-advisories/working-with-repository-security-advisories/about-repository-security-advisories#cve-identification-numbers

Q:: What does `CWE` stand for?

a) `Common Weakness Enumeration`

b) `Cybersecurity Weakness Enumeration`

c) `Code Wrapping Engine`

d) `Critical Web Elements`

A:: **Answer:** A

`Common Weakness Enumeration`

Source: https://cwe.mitre.org/

Q:: Which Dependabot comment command will get a pull request successfully completed?

a) `@dependabot close`

b) `@dependabot merge`

c) `@dependabot cancel merge`

d) `@dependabot rebase`

A:: **Answer:** B

`@dependabot merge`

Source: https://docs.github.com/en/code-security/dependabot/working-with-dependabot/managing-pull-requests-for-dependency-updates#managing-dependabot-pull-requests-with-comment-commands

Q:: Jobs that run on macOS runners that GitHub hosts consume minutes at \_\_ rate as Linux runners consume

a) the same

b) 2x

c) 5x

d) 10x

A:: **Answer:** D

10x

Source: https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions#minute-multipliers

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn

FILE TAGS: #GitHub::#Security::#Microsoft

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```
