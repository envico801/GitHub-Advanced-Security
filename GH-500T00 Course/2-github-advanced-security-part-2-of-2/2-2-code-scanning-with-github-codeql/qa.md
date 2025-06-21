Q:: What is the key philosophical difference between the QL language and a standard imperative language like Python?
A:: QL is **declarative**, meaning you describe *what* pattern you want to find, not the step-by-step process of *how* to find it. This makes it highly optimized for finding complex relationships and data-flow patterns in code, which is ideal for security analysis.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/4-what-is-ql)

Q:: Briefly describe the three distinct stages CodeQL uses to transform raw source code into an actionable security alert.
A:: 1) **Database Creation:** It first extracts the code into a structured, relational database. 2) **Query Execution:** It runs queries (the inspection rules) against this database to find patterns. 3) **Result Interpretation:** It translates the raw query results into user-friendly alerts that pinpoint the exact location and nature of the potential issue.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/3-how-does-codeql-analyze-code)

Q:: What key capabilities does a custom `codeql-config.yml` file offer that make it more powerful than simply adding queries directly to a workflow file?
A:: A custom configuration file allows for more advanced control, such as **disabling the default queries**, specifying files or directories to **ignore** during a scan, and excluding specific unwanted rules from the default set.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/6-customize-your-scanning-workflow-with-codeql)

Q:: For a repository containing both Python and JavaScript, what feature can you use to optimize the CodeQL scanning time, and what principle does it operate on?
A:: You can use a **language matrix** in the GitHub Actions workflow. It operates on the principle of **parallelization**, running two separate analysis jobs (one for Python, one for JavaScript) at the same time, which is significantly faster than running them sequentially.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/10-custom-build-steps-for-code-scanning)

Q:: When does CodeQL's `autobuild` feature typically fail, and what must a developer provide in the workflow to overcome this failure for compiled languages?
A:: The `autobuild` feature typically fails when a project has a complex, non-standard, or unique build process. To overcome this, the developer must provide their own **custom build steps** in the workflow file, explicitly telling CodeQL how to compile the code before it can be analyzed.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/10-custom-build-steps-for-code-scanning)

Q:: To achieve advanced customization, such as disabling default queries or ignoring specific directories, you would use a dedicated ____ file instead of modifying the main workflow.
A:: ...dedicated **custom configuration file** (or `codeql-config.yml` file)...
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/code-scanning-with-github-codeql/6-customize-your-scanning-workflow-with-codeql)
