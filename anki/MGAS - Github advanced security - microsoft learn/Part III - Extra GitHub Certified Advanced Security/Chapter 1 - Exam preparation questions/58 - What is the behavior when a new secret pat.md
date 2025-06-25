========== Question ==========  

### What is the behavior when a new secret pattern is added or updated in the GitHub secret scanning partner program?

a) GitHub will run a scan of all historical code content in public repositories with secret scanning enabled

b) GitHub will only scan for the new pattern in newly pushed commits in repositories with secret scanning enabled. If a secret of that pattern was already present in the repository, it will not be detected.

c) The GitHub partner has to deal with the historically leaked secrets and GitHub will only scan any new commits for the new pattern

d) GitHub will create an issue in all repositories with secret scanning enabled so the maintainers can check the repository for any secrets matching the new pattern  

========== Answer ==========  

**Answer:** A

GitHub will run a scan of all historical code content in public repositories with secret scanning enabled

Source: https://docs.github.com/en/code-security/secret-scanning/about-secret-scanning#accessing-secret-scanning-alerts

========== Id ==========  
58

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#58-What-is-the-behavior-when-a-new-secret-pat

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
