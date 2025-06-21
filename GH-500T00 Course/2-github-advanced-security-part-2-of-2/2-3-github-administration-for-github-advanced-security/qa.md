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

Q:: To enforce the use of GHAS features across your company, you can create organization-wide _____.
A:: ...organization-wide **security policies**.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/4-manage-access-github-advanced-security)
