========== Question ==========  

### As part of your Jenkins CI pipeline you've successfully created and then analyzed a CodeQL database, therefore producing a SARIF file. How can you upload the SARIF file to GitHub? (Choose two.)

a) Using the `codeql github upload-results` command from CodeQL CLI

b) Using the GitHub REST API `POST /repos/{owner}/{repo}/code-scanning/sarifs` endpoint

c) Using the `gh codeql upload-results` command from GitHub CLI

d) By committing the SARIF file to the GitHub repository

e) Using the `github/codeql-action/upload-sarif` GitHub Action  

========== Answer ==========  

**Answer(s):** A, B

Using the `codeql github upload-results` command from CodeQL CLI; Using the GitHub REST API `POST /repos/{owner}/{repo}/code-scanning/sarifs` endpoint

Source: https://docs.github.com/en/code-security/code-scanning/integrating-with-code-scanning/uploading-a-sarif-file-to-github#about-sarif-file-uploads-for-code-scanning

========== Id ==========  
125

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#125-As-part-of-your-jenkins-ci-pipeline-you-ve

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
