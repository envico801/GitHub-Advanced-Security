========== Question ==========  

### You have included some fake secrets in your test code and they have been picked up by GitHub's secret scanning. What can you do to tell GitHub that these are fake secrets used in tests and can be ignored by secret scanning? (Choose two.)

a) By creating a `secret_scanning.yml` file within which you declare paths where fake secrets are located, so scans will omit them

b) Close the Secret Scanning Alert with `Used in tests` close reason

c) In your test files, add a comment `#gh_ignore: fake secret` on the line where the fake secret is located.

d) By creating a `.github/codeql.yml` file within which you declare paths where fake secrets are located, so scans will omit them  

========== Answer ==========  

**Answer(s):** A, B

By creating a `secret_scanning.yml` file within which you declare paths where fake secrets are located, so scans will omit them; Close the Secret Scanning Alert with `Used in tests` close reason

Source: https://docs.github.com/en/code-security/secret-scanning/using-advanced-secret-scanning-and-push-protection-features/excluding-folders-and-files-from-secret-scanning

========== Id ==========  
56

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#56-You-have-included-some-fake-secrets-in-you

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
