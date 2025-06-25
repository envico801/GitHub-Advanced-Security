========== Question ==========  

### Why is it crucial for a developer to manage not just the direct dependencies they choose, but also the indirect dependencies they don't?  

========== Answer ==========  

A project's security is only as strong as its weakest link. An indirect dependency (a "part-of-a-part") can contain a vulnerability, and even if you didn't choose it directly, it's still running in your software. Failing to track and update these hidden dependencies can leave a significant security hole.

[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/2-manage-your-dependencies-github)

========== Id ==========  
7

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part I - Github Advanced Security Part 1 Of 2::Chapter 2 - 2 Configure Dependabot Security Updates On Your Github Rep

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-I-Github-Advanced-Security-Part-1-Of-2::#Chapter-2-2-Configure-Dependabot-Security-Updates-On-Your-Github-Rep::#7-Why-is-it-crucial-for-a-developer-to-manag

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
