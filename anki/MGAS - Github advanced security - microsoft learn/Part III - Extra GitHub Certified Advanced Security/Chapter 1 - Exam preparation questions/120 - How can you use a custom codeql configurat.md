========== Question ==========  

### How can you use a custom CodeQL configuration file in a GitHub Actions workflow?

a) By explicitly providing the configuration file path in the `config-file` input parameter of the `github/codeql-action/init` action

b) By storing the configuration in `.github/codeql/config-config.yml` file. The `github/codeql-action/init` action will automatically detect the file and use it

c) By uploading that file in the Code Scanning section of the Security tab in the repository

d) By storing the configuration in `.github/workflows/codeql-analysis.yml` file. The `github/codeql-action/init` action will automatically detect the file and use it  

========== Answer ==========  

**Answer:** A

By explicitly providing the configuration file path in the `config-file` input parameter of the `github/codeql-action/init` action

Source: https://docs.github.com/en/code-security/code-scanning/creating-an-advanced-setup-for-code-scanning/customizing-your-advanced-setup-for-code-scanning#using-a-custom-configuration-file

========== Id ==========  
120

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#120-How-can-you-use-a-custom-codeql-configurat

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
