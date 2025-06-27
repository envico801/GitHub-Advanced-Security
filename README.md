<!-- Header & Badge -->

<div align="center">
  <img src="./images/github-advanced-security.svg " alt="GitHub Advanced Security Badge" height="150" />
  <h1>GH-500: GitHub Advanced Security – Study Guide</h1>
  <p><em>Based on the certification objectives as of June 2025</em></p>
</div>

## 📋 Overview

This study guide is designed for security engineers, DevOps professionals, and developers preparing for the **GH-500: GitHub Advanced Security** certification. It covers planning, configuring, and managing GitHub Advanced Security features to secure code, automate vulnerability scanning, and enforce best practices across your repositories.

## 🎯 Exam Objectives & Detailed Resources

The GHAS (GH-500) exam measures proficiency across five domains with the following weightings. Click on each objective link below to find a detailed skills breakdown mapped to specific Microsoft Learn modules and relevant documentation links.

- [Domain 1: Describe the GHAS security features and functionality (15%)](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-500#domain-1-describe-the-ghas-security-features-and-functionality-15)
- [Domain 2: Configure and use secret scanning (15%)](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-500#domain-2-configure-and-use-secret-scanning-15)
- [Domain 3: Configure and use Dependabot and Dependency Review (35%)](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-500#domain-3-configure-and-use-dependabot-and-dependency-review-35)
- [Domain 4: Configure and use Code Scanning with CodeQL (25%)](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-500#domain-4-configure-and-use-code-scanning-with-codeql-25)
- [Domain 5: Describe GitHub Advanced Security best practices, results, and how to take corrective measures (10%)](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-500#domain-5-describe-github-advanced-security-best-practices-results-and-how-to-take-corrective-measures-10)

## 💡 Preparation Tips

- **Hands-on Practice:** Enable GHAS on a sample repository and walk through code scanning setup, secret scanning, and dependency review alerts.
- **Review Official Docs:** Familiarize yourself with [GitHub Advanced Security documentation](https://docs.github.com/en/code-security/getting-started/github-security-features) and the exam skills outline.
- **Understand Workflows:** Know how to configure and customize GitHub Actions for scanning, triaging alerts, and integrating with issue trackers.

## 📚 Core Study Resources

- **Certification Page:** [GitHub Advanced Security Certification](https://learn.microsoft.com/en-us/credentials/certifications/github-advanced-security/)
- **Browse GitHub Credentials:** [GitHub Certifications](https://learn.microsoft.com/en-us/credentials/browse/?products=github)
- **Official Training Course:** [GH-500T00: GitHub Advanced Security Workshop](https://learn.microsoft.com/en-us/training/courses/gh-500t00)
- **Official Microsoft Study Guide**: [Study Guide](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/gh-500)

## 🧠 Flashcards & Memory Aids

Import the provided Anki deck ([./anki/GitHub\_\_Advanced Security (GHAS)\_\_MGAS - Github advanced security - microsoft learn.apkg](https://github.com/envico801/GitHub-Advanced-Security/tree/main/anki)) for spaced-repetition of key terms, definitions, and code snippets. Includes all the questions contained in this repository in a single file.

> [!IMPORTANT]\
> Check well because the anki deck will always include the most current questions and answers, even if there are questions elsewhere in the repository.

## 📝 Practice Questions

Test your knowledge with official practice assessments:

- **Microsoft Learn Practice Assessment:** [Official GH-500 GitHub Advanced Security Practice Questions](https://learn.microsoft.com/en-us/credentials/certifications/azure-ai-engineer/practice/assessment?assessment-type=practice&assessmentId=61&practice-assessment-type=certification)

## 🔬 Hands-on Labs & Projects

Explore these interactive labs from the **Securing Your Code with GitHub** workshop:

| 🧪 Lab | Title | Description |
| -------- | ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Lab 1 | **[GitHub Advanced Security Feature Introduction](https://github.com/github-samples/securing-your-code/blob/main/_labs/lab1.md)** | Get introduced to GHAS—enable features like CodeQL, Dependabot, Secret Scanning, and more on the [Juice Shop sample repository](https://github.com/juice-shop/juice-shop) |
| Lab 2 | **[Reviewing and Managing Security Alerts](https://github.com/github-samples/securing-your-code/blob/main/_labs/lab2.md)** | Learn to triage and fix alerts generated during Lab 1 using GitHub’s security interface |
| Lab 3 | **[Hands-on with Code Scanning](https://github.com/github-samples/securing-your-code/blob/main/_labs/lab3.md)** | Inject bad code, set up a ruleset to block it, and use Copilot Autofix to remediate issues |
| Lab 4 | **[Hands-on with Dependency Review](https://github.com/github-samples/securing-your-code/blob/main/_labs/lab4.md)** | Use the Dependency Review workflow and ruleset enforcement to prevent vulnerable package additions |
| Lab 5 | **[Hands-on with Secret Scanning](https://github.com/github-samples/securing-your-code/blob/main/_labs/lab5.md)** | Test secret scanning and push protection—try committing a secret and observe how GitHub blocks it |
| Lab 6 | **[Hands-on with Security Overview](https://github.com/github-samples/securing-your-code/blob/main/_labs/lab6.md)** | Explore the Security Overview dashboard to understand alerts and coverage at an organization level |
| EC Lab 1 | **[Extra Credit: Advanced CodeQL Setup](https://github.com/github-samples/securing-your-code/blob/main/_labs/lab7-ec.md)** | Dive deeper by switching to advanced CodeQL configurations for more flexible scanning |
| EC Lab 2 | **[Extra Credit: Custom Patterns for Secret Scanning](https://github.com/github-samples/securing-your-code/blob/main/_labs/lab8-ec.md)** | Create and test custom secret-scanning rules to catch non-standard secrets |

______________________________________________________________________

**OWASP Practice repository**: [https://github.com/juice-shop/juice-shop](https://github.com/juice-shop/juice-shop)
