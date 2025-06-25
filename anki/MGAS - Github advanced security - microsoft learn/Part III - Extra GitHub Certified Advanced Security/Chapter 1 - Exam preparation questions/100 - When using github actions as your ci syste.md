========== Question ==========  

### When using GitHub Actions as your CI system and a third party tool to run code scanning, how can you upload the SARIF results to GitHub?

a) By using the `github/codeql-action/upload-sarif` GitHub Action

b) When using GitHub Actions the SARIF results are automatically uploaded to GitHub.

c) You can only use CodeQL when running code scanning in GitHub Actions. Third party code scanning tools are not supported.

d) By using the `actions/upload-artifact` GitHub Action  

========== Answer ==========  

**Answer:** A

By using the `github/codeql-action/upload-sarif` GitHub Action

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/uploading-a-sarif-file-to-github#uploading-a-code-scanning-analysis-with-github-actions

========== Id ==========  
100

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#100-When-using-github-actions-as-your-ci-syste

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
