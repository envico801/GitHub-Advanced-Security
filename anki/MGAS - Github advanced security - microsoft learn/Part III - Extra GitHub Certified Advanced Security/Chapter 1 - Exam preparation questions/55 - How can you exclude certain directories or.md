========== Question ==========  

### How can you exclude certain directories or files from secret scanning?

a) By creating a `secret_scanning.yml` file and including paths that should not be scanned

b) It's not possible to exclude specific files and/or directories from being scanned. Once you enable secret scanning for a repository, all files and directories will be scanned.

c) Include these files in the `.gitignore` file

d) By creating a `dependabot.yml` file and including paths which should not be scanned  

========== Answer ==========  

**Answer:** A

By creating a `secret_scanning.yml` file and including paths that should not be scanned

Source: https://docs.github.com/en/code-security/secret-scanning/configuring-secret-scanning-for-your-repositories#excluding-directories-from-secret-scanning-alerts-for-users

========== Id ==========  
55

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#55-How-can-you-exclude-certain-directories-or

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
