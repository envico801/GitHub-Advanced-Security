========== Question ==========  

### How does GitHub Dependency graph know what dependencies your project is using? (Choose two.)

a) GitHub derives dependencies automatically from manifests and lock files committed to the repository

b) Dependencies can be manually added using the Dependency submission API

c) GitHub scans the repository code for import statements of external packages

d) It's required to add a GitHub Actions workflow that uses the official `actions/dependency-graph` GitHub Action to add dependencies to the graph whenever a new commit is pushed to the repository  

========== Answer ==========  

**Answer(s):** A, B

GitHub derives dependencies automatically from manifests and lock files committed to the repository; Dependencies can be manually added using the Dependency submission API

Source: https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph#supported-package-ecosystems

========== Id ==========  
68

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#68-How-does-github-dependency-graph-know-what

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
