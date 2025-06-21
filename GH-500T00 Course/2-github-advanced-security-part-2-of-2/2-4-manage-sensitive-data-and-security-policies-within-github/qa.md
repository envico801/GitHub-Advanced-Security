Q:: What is the primary purpose of a `SECURITY.md` file, and how does it differ from a `CONTRIBUTING.md` file?
A:: The `SECURITY.md` file's purpose is to provide a clear, responsible disclosure policy, detailing which project versions are supported and how to privately report vulnerabilities. This is distinct from a `CONTRIBUTING.md` file, which provides instructions for developers on how to contribute code to the project.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/2-set-security-policies)

---

Q:: How does a tool like Dependabot embody the principle of security automation within a project's lifecycle?
A:: Dependabot embodies automation by continuously and automatically monitoring a project's third-party dependencies for known vulnerabilities. Instead of requiring manual, periodic checks, it proactively alerts developers and often creates pull requests with fixes, integrating security maintenance directly into the development workflow.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/3-scrub-sensitive-data-from-repository)

---

Q:: To enable users to effectively assess their risk, what two critical pieces of information must a well-formed security advisory contain?
A:: It must contain the **product and versions affected** (so users know if they are impacted) and the **severity level** of the vulnerability (so they know how urgently they need to act).
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/4-report-logs)

---

Q:: During a security incident investigation, what two fundamental questions about any event does the GitHub audit log help you answer?
A:: The audit log answers "who" (**the user that performed the action**) and "when" (**the date and time of the action**). This is crucial for establishing a timeline of events and attributing actions to specific users.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/4-report-logs)

---

Q:: If you discover that sensitive data has been accidentally committed to a repository, which GitHub administrative tool is essential for tracing how and when it was introduced?
A:: The **audit log**. It provides a detailed, time-stamped record of all repository actions, allowing you to identify the specific user and commit that introduced the sensitive data, which is the critical first step in the incident response process.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/4-report-logs)

---

Q:: To communicate security policies, such as supported versions and how to report a flaw, you should create a ____ file in your repository.
A:: ...a **`SECURITY.md`** file...
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/2-set-security-policies)
