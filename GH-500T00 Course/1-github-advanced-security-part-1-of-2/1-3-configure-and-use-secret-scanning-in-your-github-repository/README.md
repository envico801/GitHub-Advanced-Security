## 1. [GitHub Advanced Security Part 1 of 2](https://learn.microsoft.com/en-us/training/paths/github-advanced-security/)

### 1.3. [Configure and use secret scanning in your GitHub repository](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/)

#### [The Big Picture: Don't Leave Your Keys Lying Around](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/2-what-is-secret-scanning)

*   **Simple Idea:** Software often needs to connect to other services (like a database, a cloud provider like Amazon, or a social media site). To do this, it uses "secrets"—things like passwords, API keys, or access tokens. Think of these as the digital master keys to your house or car. **Secret Scanning** is like a highly trained security guard whose only job is to make sure no one accidentally leaves these keys out in the open where anyone can find them.

*   **Where the "Guard" Looks:** This guard is incredibly thorough. It doesn't just check the main code; it searches the project's entire history, all the notes developers leave for each other (in "issues" and "pull requests"), and even the public discussion forums.

---

#### [1. What do you need to do if you want to change the settings for secret scanning on a public repository?](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/3-configure-secret-scanning)

*   **Simple Idea:** For public projects, GitHub's "security guard" (Secret Scanning) is always on duty, and it follows a standard, unchangeable set of rules. You can't ask it to ignore certain areas or change its patrol route.
*   **How it Works:** GitHub provides this as a free service to protect the entire open-source community. Because of this, the settings are locked. If you need control over the settings—like telling the guard to ignore a specific test file that looks like it has a key but doesn't—you need to move the project into a "private building" and have a special security contract.
*   **Simplified Answer:** You can't change the settings on a public project. To get access to the settings, you have to make the repository **private** and have a paid **GitHub Advanced Security** license.

---

#### [2. Where can you configure the recipients of secret scanning alerts?](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/4-use-secret-scanning)

*   **Simple Idea:** When the security guard finds a lost key, it needs to know who to notify. You can give it a list of people to call. This list is configured in a special, high-security area of the project's settings.
*   **Where to Find it:** All the powerful, advanced security tools (like Code Scanning and Secret Scanning) are grouped together in one place. You configure who gets the secret alerts in the **Advanced Security settings** of a repository. This is like going to the main security office to update the emergency contact list, not the general front desk.
*   **Simplified Answer:** You can set this up in the **Advanced Security settings** of a repository.

---

#### [3. How many custom patterns can you create for an organization?](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/3-configure-secret-scanning)

*   **Simple Idea:** The "security guard" comes pre-trained to recognize thousands of common keys (like keys for Google, Amazon, Twitter, etc.). But what if your company has its own unique, custom-made key format? You can **teach the guard what your special keys look like**. This is called creating a "custom pattern."
*   **The Limit:** You can teach the guard a lot of new tricks, but not an infinite amount. For a whole company (an "organization"), you can create up to **500** of these custom patterns.
*   **Simplified Answer:** **500**.

---

#### [A Quick Word on "Push Protection" and "Validity Checks"](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/4-use-secret-scanning)

*   **Push Protection (The Proactive Guard):** This is an even smarter guard. Instead of just finding keys that have *already been dropped*, it stops you at the door *before* you can even enter the building with a key dangling from your pocket. It blocks you from saving code that contains a known secret.

*   **Validity Checks (Checking if the Key Still Works):** When a lost key is found, it's helpful to know if it's still an active key or an old, expired one. Validity Checks do exactly that. It tells you, "We found a key, and it looks like it can still open the door!" This helps you prioritize which emergencies to handle first.

---

#### [In a Nutshell:](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/7-summary)

**Secret Scanning** is GitHub's automated system for finding exposed passwords and keys in your code. On public projects, it's always on and can't be changed. On private projects (with a special license), you can customize it, including teaching it to find your company's unique secrets (**custom patterns**). When it finds a secret, it sends an alert to the right people, which you configure in the **Advanced Security settings**.
