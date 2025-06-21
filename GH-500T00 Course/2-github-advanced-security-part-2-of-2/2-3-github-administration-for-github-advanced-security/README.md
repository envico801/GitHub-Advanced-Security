## 2. [GitHub Advanced Security Part 2 of 2](https://learn.microsoft.com/en-us/training/paths/github-advanced-security-2/)

### 2.3. [GitHub administration for GitHub Advanced Security](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/)

#### [The Big Picture: Managing Security for Your Entire Company](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/2-what-is-github-advanced-security)

*   **Simple Idea:** Think of your company's software projects as a city full of different buildings (repositories). GitHub Advanced Security (GHAS) is like a city-wide, high-tech security system you can install. This module is about being the "Security Director" for the whole city—deciding which buildings get the new system, who gets the security badges to see the alerts, and how to get a bird's-eye view of everything.

*   **The "Shift Left" Philosophy:** Instead of having one big, stressful security inspection at the very end (right before a product launch), GHAS helps you build security checks into every step of the process. It "shifts" security to the "left" of the timeline, making it a continuous, less painful process.

---

#### [1. Which GitHub Advanced Security feature isn't available on public repositories?](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/5-manage-github-advanced-security-features-alerts)

*   **Simple Idea:** Most of the advanced security tools are available for free on public, open-source projects. However, one feature is designed specifically for managers and security teams inside a company to get a high-level view of all their projects. This feature doesn't make sense for a single public project.
*   **The Features:**
    *   **Code Scanning, Secret Scanning, Dependency Review:** These are all available on public projects because they help make individual projects safer, which benefits everyone.
    *   **Security Overview:** This is a special dashboard that shows you the security status of *all* the repositories in your organization in one place. It helps you see which projects are at the highest risk. Since a public repository isn't usually part of a larger organizational structure in the same way, this feature is reserved for organizations with a GHAS license.
*   **Simplified Answer:** The **Security Overview**. It's the manager's dashboard for all of a company's projects.

---

#### [2. Where can you enable GitHub Advanced Security for all the private and internal repositories in an organization?](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/3-enable-github-advanced-security)

*   **Simple Idea:** To turn on the "high-tech security system" for all the buildings in one district (an "organization"), you need to go to that district's main control panel.
*   **The Path:** The settings for an organization are grouped by category. All the security-related settings, including turning on GHAS, are found in the organization's **Code security and analysis** settings.
*   **Why Not the Others?**
    *   *Site admin page:* This is for the entire GitHub Enterprise instance (the whole city), not just one organization (district).
    *   *Security tab:* This is where you *view* the security alerts once they're running, not where you turn on the features themselves.
*   **Simplified Answer:** The setting is in the organization's **Code security and analysis** settings.

---

#### [3. What can you do to ensure that everyone in your organization is using GitHub Advanced Security?](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/4-manage-access-github-advanced-security)

*   **Simple Idea:** As the "Security Director," you want to make sure every building manager is actually using the security system you've provided. You can't force them individually, but you can set a company-wide rule.
*   **The Best Way:** You can create a **security policy at the organization level**. This policy can say, for example, "All repository admins in this organization are allowed (or required) to enable Advanced Security features." This is the most effective way to encourage or enforce adoption across the board.
*   **Why Not the Others?**
    *   *Giving access to alerts:* This is important, but it doesn't ensure the tools are being used in the first place.
    *   *Adding a SECURITY.md file:* This is a good practice for telling people how to report vulnerabilities, but it doesn't have anything to do with enabling the automated scanning tools.
*   **Simplified Answer:** **Set a security policy at the organization level.**

---

#### [4. What should you keep in mind when using GitHub Actions for your security workflows?](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/5-manage-github-advanced-security-features-alerts)

*   **Simple Idea:** GitHub Actions is the automation engine that runs your security scans. When it runs, it uses a special, temporary "access key" called a `GITHUB_TOKEN` to do its work (like posting results). This key has certain permissions, and you need to make sure it has the *right* permissions for your security workflow.
*   **The Golden Rule:** For security, you should always give a tool the *least amount of permission it needs to do its job*. If a workflow only needs to read issues, don't give it permission to write them. You must be careful to **correctly set the permissions for the `GITHUB_TOKEN`**. If the token doesn't have enough permission, your security workflow might fail. If it has too much, it could be a security risk itself.
*   **Simplified Answer:** You should **correctly set up the permissions for the `GITHUB_TOKEN`** used to make authenticated API calls.

---

#### [In a Nutshell:](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/7-summary)

As a GitHub administrator, you manage GHAS at the organization level through **Code security and analysis** settings. While most features work on public repos, the **Security Overview** dashboard requires a GHAS license. Enforce adoption through **organization-wide security policies**, and always carefully configure **`GITHUB_TOKEN` permissions** for security workflows.
