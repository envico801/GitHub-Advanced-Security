========== Question ==========  

### When Secret Scanning finds a potential secret, what additional, crucial information does the "Validity Check" feature provide to help you prioritize your response?  

========== Answer ==========  

The Validity Check confirms whether the discovered secret is still **active** and can actually be used to access a service. This helps you prioritize alerts, allowing you to immediately address the most critical, live credentials over old, expired ones.

[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/4-use-secret-scanning)

========== Id ==========  
15

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part I - Github Advanced Security Part 1 Of 2::Chapter 3 - 3 Configure And Use Secret Scanning In Your Github Reposit

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-I-Github-Advanced-Security-Part-1-Of-2::#Chapter-3-3-Configure-And-Use-Secret-Scanning-In-Your-Github-Reposit::#15-When-secret-scanning-finds-a-potential-sec

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
