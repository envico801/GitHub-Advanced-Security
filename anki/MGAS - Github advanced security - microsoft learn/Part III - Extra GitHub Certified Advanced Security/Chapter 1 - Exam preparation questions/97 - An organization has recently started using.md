========== Question ==========  

### An organization has recently started using CodeQL analysis for all pull requests on their repositories as well as running the analysis on an hourly schedule. Since then they are experiencing larger than usual GitHub Actions bills. What is the most likely cause of this?

a) Code scanning uses GitHub Actions and the organization is being billed for the additional usage.

b) The code scanning analysis is finding more issues than expected and is taking longer to complete.

c) Code scanning can only be run on a daily schedule and the organization is being billed for the additional usage.

d) There is no correlation between code scanning and GitHub Actions billing. The organization is being billed for other GitHub Actions workflows.  

========== Answer ==========  

**Answer:** A

Code scanning uses GitHub Actions and the organization is being billed for the additional usage.

Source: https://docs.github.com/en/code-security/code-scanning/introduction-to-code-scanning/about-code-scanning#about-billing-for-code-scanning

========== Id ==========  
97

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#97-An-organization-has-recently-started-using

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
