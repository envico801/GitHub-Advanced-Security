========== Question ==========  

### In the code scanning process, what is the fundamental difference between a tool like `ESLint` and a tool like `GitHub Actions`?  

========== Answer ==========  

A tool like `ESLint` is an **analyzer** that _creates_ the inspection report (the SARIF file) by checking the code for issues. `GitHub Actions` is a **delivery mechanism** or orchestrator that _runs the analyzer and uploads_ that report to GitHub so the results can be displayed. One generates the findings, the other delivers them.

[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/3-enable-code-scanning-with-third-party-tools)

========== Id ==========  
22

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part I - Github Advanced Security Part 1 Of 2::Chapter 4 - 4 Configure Code Scanning On Github

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-I-Github-Advanced-Security-Part-1-Of-2::#Chapter-4-4-Configure-Code-Scanning-On-Github::#22-In-the-code-scanning-process-what-is-the

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
