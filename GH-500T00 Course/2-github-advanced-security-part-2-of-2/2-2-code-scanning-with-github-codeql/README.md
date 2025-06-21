## 2. [GitHub Advanced Security Part 2 of 2](https://learn.microsoft.com/en-us/training/paths/github-advanced-security-2/)

### 2.2. [Code scanning with GitHub CodeQL](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/)

#### [The Big Picture: Mastering Your Code Inspector](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/2-what-is-codeql)

*   **Simple Idea:** This set of materials moves beyond just turning on the "automated code inspector" (CodeQL). It's about learning to be the *manager* of the inspector. You'll learn how to give it very specific instructions, change what it looks for, and even how to use it outside of GitHub's automated system.

*   **Key Concepts You'll Master:**
    *   **QL:** The special "language" the inspector speaks.
    *   **Custom Queries & Suites:** Writing your own inspection checklists.
    *   **The Language Matrix:** How to inspect projects with multiple programming languages efficiently.
    *   **Custom Build Steps:** Teaching the inspector how to handle projects that are built in a weird or unique way.

---

#### [1. What is QL? (The Inspector's Language)](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/4-what-is-ql)

*   **Simple Idea:** QL (Query Language) is the specialized programming language used to write CodeQL "queries." Think of it as the language you use to write instructions for the code inspector.
*   **How it's Different from Regular Programming:**
    *   **It's "Declarative":** You describe **what** you're looking for, not **how** to find it. It's like telling a detective, "Find me all the people who were at the bank on Tuesday and left with a red bag," instead of giving them step-by-step instructions on how to check security footage and interview people.
    *   **It's for Finding Patterns:** It's designed specifically to find relationships and patterns in code, like tracking where a piece of data comes from and where it ends up.
    *   **It's Object-Oriented:** This is a programming concept that makes it easier to organize your queries into reusable, modular pieces. It's like having a library of pre-written instructions you can mix and match.
*   **In a Nutshell:** QL is a powerful, logic-based language for asking very complex questions about your code to find security flaws.

---

#### [2. How does CodeQL Analyze Code? (The Inspector's 3-Step Process)](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/3-how-does-codeql-analyze-code)

*   **Simple Idea:** CodeQL follows a consistent three-step process to inspect your code.
    1.  **Create a Database (Organize the Evidence):** First, it reads all your code and turns it into a highly structured database. This makes the code searchable in a very powerful way.
    2.  **Run Queries (Ask the Questions):** Next, it runs your inspection checklist (the queries) against this database to find any matches (potential problems).
    3.  **Interpret Results (Write the Report):** Finally, it takes the raw results and presents them in a human-readable way, pointing directly to the problem line in your code and explaining why it's a potential issue.

---

#### [3. How can you customize what CodeQL looks for?](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/6-customize-your-scanning-workflow-with-codeql)

*   **Simple Idea:** You're not stuck with just the standard inspection checklist. You can add your own custom checks or use checklists created by others.
*   **Two Ways to Add More Checks:**
    1.  **In the Workflow File:** You can directly list extra queries or "query packs" (bundles of queries) you want to run right inside the main GitHub Actions workflow file. This is quick and easy for simple additions.
    2.  **Using a Custom Configuration File:** For more complex setups, you can create a separate `codeql-config.yml` file. This file lets you do more advanced things like:
        *   List lots of custom queries.
        *   *Disable* the default queries so you *only* run your custom ones.
        *   Tell the inspector to *ignore* certain files or folders.
        *   Exclude specific rules from the default set that you don't care about.

---

#### [4. How do you handle multiple languages or special build steps?](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/10-custom-build-steps-for-code-scanning)

*   **Simple Idea:** The inspector needs to know what programming languages it's looking at and how your project is built, especially for "compiled" languages like C++ or Java.
*   **Handling Multiple Languages (The Language Matrix):**
    *   If your project uses, say, both JavaScript and Python, you can set up a "matrix." This tells GitHub to run two separate inspections *at the same time* (in parallel)—one for JavaScript and one for Python. This is much faster than doing them one after the other.
*   **Handling Special Builds (Custom Build Steps):**
    *   CodeQL has an `autobuild` feature that tries to guess how to build your code. But if you have a complex or non-standard build process, `autobuild` might fail.
    *   In this case, you can remove the `autobuild` step and provide your own **custom build steps**. You're essentially giving the inspector a specific set of instructions on how to compile your code so it can be inspected correctly.

---

#### [In a Nutshell:](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/12-summary)

This section is all about taking your code scanning skills to the next level. You learn about **QL**, the language used to write inspection rules. You can **customize** which rules get run, either in the main **workflow file** or a separate **config file**. For projects with **multiple languages**, you can use a **matrix** to speed up scans. And if your project has a unique build process, you can provide **custom build steps** to make sure the inspection runs correctly.
