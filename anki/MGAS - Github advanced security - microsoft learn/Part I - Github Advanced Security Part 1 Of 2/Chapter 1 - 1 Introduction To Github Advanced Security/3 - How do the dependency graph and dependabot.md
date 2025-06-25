========== Question ==========  

### How do the Dependency Graph and Dependabot work together to secure a project's software supply chain?  

========== Answer ==========  

The Dependency Graph acts as a complete "parts list" for the software. Dependabot reads this list and cross-references it with the GitHub Advisory Database (a list of known vulnerabilities) to check for any unsafe parts. If a match is found, it raises an alert, much like a safety recall notice for a faulty car part.

[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/3-create-culture-around-security)

========== Id ==========  
3

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part I - Github Advanced Security Part 1 Of 2::Chapter 1 - 1 Introduction To Github Advanced Security

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-I-Github-Advanced-Security-Part-1-Of-2::#Chapter-1-1-Introduction-To-Github-Advanced-Security::#3-How-do-the-dependency-graph-and-dependabot

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
