## 1. [GitHub Advanced Security Part 1 of 2](https://learn.microsoft.com/en-us/training/paths/github-advanced-security/)

### 1.4. [Configure code scanning on GitHub](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/)

#### [The Big Picture: Your Automated Code Inspector](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/2-what-code-scanning)

*   **Simple Idea:** Think of **Code Scanning** as an automated inspector for the "blueprints" (your code) of your software. Its job is to read through all the plans and find potential security flaws or common mistakes *before* the software is built and released. This saves a huge amount of time and prevents problems later.

*   **How it Works:** The main "inspector" GitHub provides is called **CodeQL**. It's a very smart analysis engine. You can also hire "inspectors" from other companies (third-party tools) and have them submit their reports to GitHub. All these reports show up in one central place in your project's "Security" tab.

---

#### [1. What is the difference between scheduled versus triggered events in code scanning?](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/4-configure-code-scanning)

*   **Simple Idea:** This is about *when* the inspector does its work. You have two main choices:
    1.  **Triggered Events (The "Every Time" Inspector):** The inspector checks the blueprints every time a developer makes a change. It's like having an inspector on-site who reviews every single new drawing the moment it's submitted. This is great for catching new mistakes immediately.
        *   *Example:* A scan runs every time code is **pushed** to the main branch or a **pull request** is created.

    2.  **Scheduled Events (The "Weekly" Inspector):** The inspector comes in at a regular, set time (e.g., every Monday at 9 AM) to review the entire set of blueprints. This is useful for finding problems that might have been missed or for checking against newly discovered types of flaws that your "Every Time" inspector didn't know about last week.

*   **Simplified Answer:** **Scheduled events** run on a fixed schedule (like a calendar appointment), while **triggered events** happen in response to a specific developer action (like saving new code).

---

#### [2. Which of the following are the tools used to upload a SARIF file?](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/3-enable-code-scanning-with-third-party-tools)

*   **Simple Idea:** A **SARIF file** is like a standardized inspection report. Whether your inspector is GitHub's own CodeQL or a third-party tool, they all write their findings down in this common format. You then need a way to "upload" this report to GitHub so it can be displayed.

*   **The "Delivery Methods" for the Report:**
    1.  **GitHub Actions:** This is the most common way. It's like having an automated courier service built into GitHub. You set up a "workflow" that runs your inspector and then tells the courier to deliver the SARIF report.
    2.  **The Code Scanning API:** This is for more custom or advanced setups. Think of it like a special "mailbox" where you can programmatically send your reports from another system. "API" is just a fancy term for a way computer programs talk to each other.
    3.  **The CodeQL CLI (Command-Line Interface):** This is a tool you can run on your own computer or server. It runs the CodeQL inspector and then has a built-in command to send the report directly to GitHub. It's like the inspector having its own direct delivery drone.

*   **What are *not* tools for uploading?**
    *   `ESLint`: This is an *example* of a third-party inspection tool. It *creates* a SARIF report, but it doesn't upload it.
    *   `partialFingerprints`: This is a piece of information *inside* the SARIF report that helps GitHub avoid showing you the same error twice. It's part of the report's content, not a tool for delivering it.

*   **Simplified Answer:** The tools used are **GitHub Actions**, the **code scanning API**, and the **CodeQL CLI**. These are the three official ways to get your inspection report (SARIF file) into GitHub.

---

#### [In a Nutshell:](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/7-summary)

**Code Scanning** is GitHub's system for automatically checking your code for problems. You can set it to run whenever developers make changes (**triggered events**) or on a regular basis (**scheduled events**). The inspection results are put into a standard **SARIF file**, which you can upload to GitHub using **GitHub Actions**, a dedicated **API**, or the **CodeQL CLI**. This helps you find and fix security issues early and easily.
