## 1. [GitHub Advanced Security Part 1 of 2](https://learn.microsoft.com/en-us/training/paths/github-advanced-security/)

### 1.2. [Configure Dependabot security updates on your GitHub repo](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/)

#### [The Big Picture: Managing Your Software's "Parts"](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/2-manage-your-dependencies-github)

*   **Simple Idea:** When developers build software, they almost never build everything from scratch. They use pre-made code packages (like libraries or tools) from other people to save time. These are called **"dependencies."** Think of it like building a car: you don't make your own tires, engine, or radio; you buy them from other companies and assemble them.

*   **The Problem:** Just like car parts can have safety recalls, these software "parts" can have security flaws discovered later. Your job is to keep track of all the parts you've used and replace any that are found to be unsafe. GitHub gives you tools to automate this.

---

#### [1. What are direct dependencies?](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/2-manage-your-dependencies-github)

*   **Simple Idea:** These are the main parts you *personally choose* to include in your project.
*   **Car Analogy:** If you're building a car, the engine you select from Ford, the tires from Michelin, and the sound system from Bose are your **direct dependencies**. You picked them out and put them on your "parts list" (which in code is called a `manifest` or `lock file`).
*   **What about Indirect Dependencies?** The engine you chose has its own parts inside it, like spark plugs and pistons. You didn't choose those spark plugs yourself; they came *with* the engine. These are **indirect dependencies**. GitHub tracks both.
*   **Simplified Answer:** They are the main parts you decide to add to your project and list on your "parts list" file.

---

#### [2. When is a Dependabot alert generated?](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/3-dependabot-alerts)

*   **Simple Idea:** Dependabot is your automated "safety recall manager." It sends you an alert when it finds out a part you're using is dangerous. This happens in two main situations:
    1.  **A new safety recall is announced:** A global database of software vulnerabilities (the "GitHub Advisory Database") gets a new entry. Dependabot sees this and immediately checks if you're using that faulty part.
    2.  **You add a new part to your project:** As soon as you add a new dependency to your "parts list," Dependabot runs a background check on it to see if it has any known safety issues.
*   **Simplified Answer:** When a new security flaw is reported for a part you're using, OR when you add a new part to your project's "parts list."

---

#### [3. What is a prerequisite for Dependabot to automatically enable security updates for a repository?](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/4-dependabot-security-updates)

*   **Simple Idea:** "Dependabot security updates" is the feature where Dependabot not only *tells* you about a bad part but also *tries to fix it for you* by automatically creating a request to install the safe version. For this to be turned on by default for free, a certain condition must be met.
*   **The Condition:** The project (repository) must be **public**.
*   **Why?** GitHub provides many of its powerful security tools for free to public, open-source projects. It's a way of helping the entire software community stay safe. For private projects, these advanced, automated features are typically part of a paid plan like GitHub Advanced Security.
*   **Simplified Answer:** The project is public.

---

#### [4. What query can you use to view all the notifications marked as done?](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/5-manage-dependabot-notifications-reporting)

*   **Simple Idea:** Your security alerts show up in a notification inbox, just like email. It can get crowded. To keep things organized, you can mark alerts that you've already handled as **"Done."**
*   **How to Filter:** The notification inbox has a search bar where you can type special commands to filter your view.
*   **The Command:** To see only the notifications you've already finished and marked as done, you use the search filter `is:done`. This hides all the current, unread alerts and just shows your completed work.
*   **Simplified Answer:** `is:done`. It's like searching your email inbox for everything you've already archived.

---

#### [A Quick Word on "Dependency Review"](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/6-dependency-review)

*   **Simple Idea:** This is another tool that works with Dependabot. Think of it as a **gatekeeper**.
*   **How it's Different from Dependabot:**
    *   **Dependabot** is like a manager who constantly checks the parts *already in your warehouse* for new safety recalls.
    *   **Dependency Review** is like a security guard at the loading dock who inspects *new parts as they arrive*, *before* they even get put in your warehouse. It checks every new "shipment" of code (a "pull request") to see if it's bringing in any known dangerous parts.
*   **In short:** Dependency Review helps you *prevent* bad parts from getting in, while Dependabot helps you *fix* bad parts that are already there.
