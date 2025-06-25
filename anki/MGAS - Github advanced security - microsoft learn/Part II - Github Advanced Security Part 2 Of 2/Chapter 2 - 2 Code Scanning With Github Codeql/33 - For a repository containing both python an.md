========== Question ==========  

### For a repository containing both Python and JavaScript, what feature can you use to optimize the CodeQL scanning time, and what principle does it operate on?  

========== Answer ==========  

You can use a **language matrix** in the GitHub Actions workflow. It operates on the principle of **parallelization**, running two separate analysis jobs (one for Python, one for JavaScript) at the same time, which is significantly faster than running them sequentially.

[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/10-custom-build-steps-for-code-scanning)

========== Id ==========  
33

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part II - Github Advanced Security Part 2 Of 2::Chapter 2 - 2 Code Scanning With Github Codeql

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-II-Github-Advanced-Security-Part-2-Of-2::#Chapter-2-2-Code-Scanning-With-Github-Codeql::#33-For-a-repository-containing-both-python-an

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
