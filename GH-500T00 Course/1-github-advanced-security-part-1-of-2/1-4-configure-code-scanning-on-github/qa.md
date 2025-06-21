Q:: What is the strategic difference between using a **triggered** code scan versus a **scheduled** code scan?
A:: A **triggered** scan provides immediate feedback on new changes (like in a pull request), catching vulnerabilities the moment they are introduced. A **scheduled** scan provides a periodic, comprehensive review of the entire codebase, which is useful for finding existing issues and checking against the very latest security rules.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/4-configure-code-scanning)

Q:: What is the purpose of the SARIF file format in the context of GitHub Code Scanning?
A:: SARIF acts as a standardized "inspection report." Its purpose is to provide a common format for any analysis tool (whether it's GitHub's native CodeQL or a third-party tool) to report its findings. This allows GitHub to ingest and display results from many different sources in one unified security interface.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/3-enable-code-scanning-with-third-party-tools)

Q:: In the code scanning process, what is the fundamental difference between a tool like `ESLint` and a tool like `GitHub Actions`?
A:: A tool like `ESLint` is an **analyzer** that *creates* the inspection report (the SARIF file) by checking the code for issues. `GitHub Actions` is a **delivery mechanism** or orchestrator that *runs the analyzer and uploads* that report to GitHub so the results can be displayed. One generates the findings, the other delivers them.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/3-enable-code-scanning-with-third-party-tools)

Q:: In the context of GitHub's native code scanning, what is the role of CodeQL?
A:: CodeQL is the powerful analysis engine that acts as GitHub's own native "code inspector." It treats code as data and queries it to find security vulnerabilities and coding errors, generating the results that are then displayed as code scanning alerts.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/2-what-code-scanning)

Q:: How does integrating Code Scanning into a pull request workflow prevent security issues from reaching the main codebase?
A:: By automatically scanning the code within a pull request *before* it is merged, it acts as an automated quality gate. It presents any discovered vulnerabilities directly to the developer in their workflow, allowing them to fix the issue immediately, thus preventing the flawed code from ever being integrated into the main branch.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/4-configure-code-scanning)

Q:: Besides using GitHub Actions and the CodeQL CLI, what is the third primary method for uploading a SARIF file to GitHub?
A:: The code scanning API. This method is used for programmatic or custom integrations where an external system needs to push analysis results directly to GitHub without using a standard workflow or command-line tool.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/3-enable-code-scanning-with-third-party-tools)
