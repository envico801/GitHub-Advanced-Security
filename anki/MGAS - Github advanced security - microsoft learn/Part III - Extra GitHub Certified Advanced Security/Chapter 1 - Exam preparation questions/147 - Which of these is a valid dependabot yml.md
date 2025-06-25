========== Question ==========  

### Which of these is a valid `dependabot.yml` configuration file?

a) Code block (yaml):

version: 2

updates:

\- package-ecosystem: "npm"

directory: "/"

schedule:

interval: "daily"

b) Code block (yaml):

version: 2

config:

\- directory: "/"

schedule:

interval: "daily"

c) Code block (yaml):

version: 2

updates:

\- package-ecosystem: "npm"

directory: "/"

schedule:

interval: "everyday"

d) Code block (yaml):

version: 2

config:

\- package-ecosystem: "npm"

directory: "/"

schedule:

interval: "daily"  

========== Answer ==========  

**Answer:** A

Code block (yaml):

version: 2

updates:

\- package-ecosystem: "npm"

directory: "/"

schedule:

interval: "daily"

Source: https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file

========== Id ==========  
147

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#147-Which-of-these-is-a-valid-dependabot-yml

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
