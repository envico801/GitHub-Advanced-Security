========== Question ==========  

### When does CodeQL's `autobuild` feature typically fail, and what must a developer provide in the workflow to overcome this failure for compiled languages?  

========== Answer ==========  

The `autobuild` feature typically fails when a project has a complex, non-standard, or unique build process. To overcome this, the developer must provide their own **custom build steps** in the workflow file, explicitly telling CodeQL how to compile the code before it can be analyzed.

[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/10-custom-build-steps-for-code-scanning)

========== Id ==========  
34

---

DECK INFO

TARGET DECK: GitHub::Advanced Security (GHAS)::MGAS - Github advanced security - microsoft learn::Part II - Github Advanced Security Part 2 Of 2::Chapter 2 - 2 Code Scanning With Github Codeql

FILE TAGS: #GitHub::#Security::#Microsoft::#MGAS-Github-advanced-security-microsoft-learn::#Part-II-Github-Advanced-Security-Part-2-Of-2::#Chapter-2-2-Code-Scanning-With-Github-Codeql::#34-When-does-codeql-s-autobuild-feature-typ

Tags:

Reference:

Related:

```dataview
LIST
where file.name = this.file.name
```

QUESTION STATUS: Safe to store
