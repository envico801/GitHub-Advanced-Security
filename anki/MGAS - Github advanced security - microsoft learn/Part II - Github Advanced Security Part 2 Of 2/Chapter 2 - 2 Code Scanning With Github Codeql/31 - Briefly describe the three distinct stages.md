========== Question ==========  

### Briefly describe the three distinct stages CodeQL uses to transform raw source code into an actionable security alert.  

========== Answer ==========  

1. **Database Creation:** It first extracts the code into a structured, relational database.

2. **Query Execution:** It runs queries (the inspection rules) against this database to find patterns.

3. **Result Interpretation:** It translates the raw query results into user-friendly alerts that pinpoint the exact location and nature of the potential issue.

[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/3-how-does-codeql-analyze-code)

========== Id ==========  
31

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part II - Github Advanced Security Part 2 Of 2::Chapter 2 - 2 Code Scanning With Github Codeql

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-II-Github-Advanced-Security-Part-2-Of-2::#Chapter-2-2-Code-Scanning-With-Github-Codeql::#31-Briefly-describe-the-three-distinct-stages

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
