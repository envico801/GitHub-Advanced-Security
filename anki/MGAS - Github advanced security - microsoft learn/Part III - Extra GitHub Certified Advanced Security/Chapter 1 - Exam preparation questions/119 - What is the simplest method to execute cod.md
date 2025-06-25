========== Question ==========  

### What is the simplest method to execute CodeQL analysis concurrently for each language in a multi-language repository using GitHub Actions?

a) By creating a `languages` matrix for the job and then reference it in the `github/codeql-action/init` action's `languages` input parameter

b) By calling the `github/codeql-action/analyze` action in separate steps for each language

c) By creating a separate workflow for each language

d) Define the parallelism in the `github/codeql-action/analyze` action  

========== Answer ==========  

**Answer:** A

By creating a `languages` matrix for the job and then reference it in the `github/codeql-action/init` action's `languages` input parameter

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#changing-the-languages-that-are-analyzed

========== Id ==========  
119

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#119-What-is-the-simplest-method-to-execute-cod

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
