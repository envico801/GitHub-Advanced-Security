========== Question ==========  

### In an automated pull request check, what is the function of the default failure threshold, and which severity level triggers it?  

========== Answer ==========  

The function is to act as an automated quality gate that prevents code with significant issues from being merged into the main branch. By default, this check is triggered to fail if CodeQL finds any problem with a severity level of **Error**.

[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/4-understand-results)

========== Id ==========  
27

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part II - Github Advanced Security Part 2 Of 2::Chapter 1 - 1 Identify Security Vulnerabilities In Your Codebase By Us

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-II-Github-Advanced-Security-Part-2-Of-2::#Chapter-1-1-Identify-Security-Vulnerabilities-In-Your-Codebase-By-Us::#27-In-an-automated-pull-request-check-what-i

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
