Q:: Using the "code detective" analogy, what are the three fundamental steps a developer must perform when using the CodeQL CLI to investigate a codebase?
A:: The three steps are: 1) **Create a database** to organize the code into a searchable format, 2) **Run queries** to ask specific questions and look for patterns, and 3) **Analyze the results** to identify vulnerabilities.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/2-how-prepare-database-codeql)

Q:: Why is the initial step of "creating a database" so crucial for CodeQL's analysis, rather than simply searching the raw code files?
A:: Creating a database transforms the raw code into a structured, relational model. This allows CodeQL to understand the relationships between different parts of the code (like data flow and function calls), enabling it to find complex vulnerabilities that a simple text search would miss.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/2-how-prepare-database-codeql)

Q:: What is a CodeQL "query," and what is its role in the security analysis process?
A:: A CodeQL query is a question written in a special language that is used to "ask" the CodeQL database for specific code patterns. Its role is to act as the detective's instruction, guiding the search for known types of vulnerabilities, bugs, or other errors.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/3-run-codeql-database)

Q:: In an automated pull request check, what is the function of the default failure threshold, and which severity level triggers it?
A:: The function is to act as an automated quality gate that prevents code with significant issues from being merged into the main branch. By default, this check is triggered to fail if CodeQL finds any problem with a severity level of **Error**.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/4-understand-results)

Q:: What is the most direct way to optimize a slow CodeQL analysis without changing the amount of code being scanned?
A:: The most direct way is to increase the system resources available to the analysis, specifically by **increasing the memory (RAM)** and/or the number of CPU cores. More resources allow the CodeQL engine to process the database and queries more quickly.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/5-troubleshoot-your-results)

Q:: Complete the sentence: The hierarchical command structure for using the CodeQL command-line tool follows the format `codeql` ____ ____.
A:: ...`codeql` **[command]** **[subcommand]**.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/3-run-codeql-database)
