## 2. [GitHub Advanced Security Part 2 of 2](https://learn.microsoft.com/en-us/training/paths/github-advanced-security-2/)

### 2.4. [Manage sensitive data and security policies within GitHub](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/)

#### [The Big Picture: Being the Security Guard for Your Project](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/2-set-security-policies)

*   **Simple Idea:** Think of your project on GitHub as a secure building. As the "Security Guard" (or administrator), your job is to set the rules, check who comes and goes, and know what to do if someone accidentally leaves a key card lying around. This module is about learning all the tools GitHub gives you to be a good security guard.

*   **Key Responsibilities You'll Learn:**
    *   **Writing the Rulebook:** Creating documents that tell everyone the security rules.
    *   **Setting Up the Locks:** Configuring permissions and branch rules so people can't accidentally break things.
    *   **Automating Patrols:** Using tools like Dependabot to automatically check for problems.
    *   **Responding to an Incident:** Knowing what to do if sensitive data (like a password) gets leaked.
    *   **Reviewing Security Tapes:** Using audit logs to see who did what and when.

---

#### [1. What file should you use to create documentation for collaborators that lists supported versions of the project?](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/2-set-security-policies)

*   **Simple Idea:** When someone finds a potential security flaw, they need to know if it affects a version of your project that you still support. You need a specific file to communicate this information clearly.
*   **The Special File:** GitHub has a special file called **`SECURITY.md`**. This is the official "Security Rulebook" for your project. In it, you tell people which versions of your product are still getting security updates and exactly how to report a vulnerability to you privately.
*   **Why Not the Others?**
    *   `CONTRIBUTING.md`: This is for telling people how to *contribute code* to your project.
    *   `SUPPORT.md`: This is for telling people where to get *general help* or support.
*   **Simplified Answer:** `SECURITY.md`. It's the go-to document for all security-related information.

---

#### [2. What tool should you use to automate part of your security process?](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/3-scrub-sensitive-data-from-repository)

*   **Simple Idea:** Being a security guard is a lot of work. You want to automate as much of your patrol route as possible so you can focus on real threats.
*   **The Best Tool for Automation:** **Dependabot** is a perfect example of an automated security tool. It automatically checks all the third-party "parts" (dependencies) your project uses. If it finds a part with a known security flaw, it not only alerts you but often automatically creates a fix for you to approve.
*   **Why Not the Others?** The other options are manual tasks. Creating documentation, setting restrictions, and writing advisories are things *you* do. Dependabot is a robot that works for you.
*   **Simplified Answer:** **Add Dependabot to your code base.**

---

#### [3. Which two pieces of information should be included in a security advisory?](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/4-report-logs)

*   **Simple Idea:** A **security advisory** is a formal public announcement you make when you've found and fixed a security vulnerability. Think of it like a car company issuing a public safety recall notice. It needs to contain clear, essential information.
*   **The Essentials for an Advisory:**
    1.  **What's affected?** You need to clearly state the **product** (and which versions of it) are vulnerable.
    2.  **How bad is it?** You need to give it a **severity** rating (like Low, Medium, High, or Critical) so people know how urgently they need to update.
*   **Why Not the Others?** While other details are useful, the product and severity are the absolute minimum needed for someone to understand if they are at risk and how serious it is. The administrator's name or an internal "exposures list" are not standard parts of a public advisory.
*   **Simplified Answer:** The **product affected** and the **severity**.

---

#### [4. Which two pieces of information are included in your organization's log?](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/4-report-logs)

*   **Simple Idea:** The **audit log** is like the building's security camera footage. It records every important action that happens. When you review the footage, you want to know two basic things about every event.
*   **The "Who" and "When":** Every entry in the audit log will tell you:
    1.  **The user that performed the action** (Who did it?)
    2.  **The date and time of the action** (When did they do it?)
*   **Why Not the Others?** "Changes in permissions" and "users being promoted" are *types* of actions that are recorded, but the fundamental pieces of information in *every* log entry are the person responsible and the timestamp.
*   **Simplified Answer:** **The user that performed the action** and **the date and time of the action.**

---

#### [In a Nutshell:](https://learn.microsoft.com/en-us/training/modules/manage-sensitive-data-security-policies/7-summary)

As a GitHub security administrator, your key tools are:
- The **`SECURITY.md`** file for documenting policies
- **Dependabot** for automated dependency monitoring
- Clear **security advisories** with product and severity info
- Comprehensive **audit logs** tracking all user actions
