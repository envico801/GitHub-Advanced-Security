========== Question ==========  

### Your company has internal secrets that should not be pushed to GitHub repositories. The pattern of these secrets is not known by GitHub and therefore is not detected by secret scanning. What can companies do to protect their developers from accidentally pushing these secrets to repositories in their GitHub Organization?

a) Define regex patterns for these secrets and enable custom patterns for secret scanning for the organization.

b) The company should join the GitHub partner program so the pattern of the companies secrets is recognized.

c) Define custom GitHub Actions workflows for repositories in the organization that will scan for these secrets.

d) In all repositories include `secret_scanning.yml` file which will define these custom secrets that should be scanned for.  

========== Answer ==========  

**Answer:** A

Define regex patterns for these secrets and enable custom patterns for secret scanning for the organization.

Source: https://docs.github.com/en/enterprise-cloud@latest/code-security/secret-scanning/defining-custom-patterns-for-secret-scanning#defining-a-custom-pattern-for-an-organization

========== Id ==========  
64

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part III - Extra GitHub Certified Advanced Security::Chapter 1 - Exam preparation questions

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-III-Extra-GitHub-Certified-Advanced-Security::#Chapter-1-Exam-preparation-questions::#64-Your-company-has-internal-secrets-that-sho

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
