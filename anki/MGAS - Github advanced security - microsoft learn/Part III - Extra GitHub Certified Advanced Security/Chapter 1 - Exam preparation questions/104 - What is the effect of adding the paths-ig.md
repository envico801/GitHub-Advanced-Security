========== Question ==========  

### What is the effect of adding the `paths-ignore` keyword to your code scanning GitHub Actions workflow?

a) Avoiding unnecessary scans when files that are not relevant to the analysis are changed.

b) It tells CodeQL to omit all `*.txt` and `*.md` files from the analysis.

c) Preventing the CodeQL analysis from running on pull requests that change files with the specified extensions.

d) Pull request checks will ignore any CodeQL vulnerabilities that are found in `*.txt` and `*.md` files.  

========== Answer ==========  

**Answer:** A

Avoiding unnecessary scans when files that are not relevant to the analysis are changed.

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#avoiding-unnecessary-scans-of-pull-requests

========== Id ==========  
104

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#104-What-is-the-effect-of-adding-the-paths-ig

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
