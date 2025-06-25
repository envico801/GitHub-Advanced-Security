========== Question ==========  

### When configuring a security workflow in GitHub Actions, what is the critical security principle you should apply to the `GITHUB_TOKEN`?  

========== Answer ==========  

You must apply the **principle of least privilege** by correctly setting up the permissions for the `GITHUB_TOKEN`. The token should only be granted the minimum permissions necessary for the workflow to complete its job, which reduces the potential risk if the workflow were ever compromised.

[Documentation Link](https://learn.microsoft.com/en-us/training/modules/github-administration-github-advanced-security/5-manage-github-advanced-security-features-alerts)

========== Id ==========  
39

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part II - Github Advanced Security Part 2 Of 2::Chapter 3 - 3 Github Administration For Github Advanced Security

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-II-Github-Advanced-Security-Part-2-Of-2::#Chapter-3-3-Github-Administration-For-Github-Advanced-Security::#39-When-configuring-a-security-workflow-in-gi

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
