## 2. [GitHub Advanced Security Part 2 of 2](https://learn.microsoft.com/en-us/training/paths/github-advanced-security-2/)

### 2.1. [Identify security vulnerabilities in your codebase by using CodeQL](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/)

#### [The Big Picture: Becoming a Code Detective](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/2-how-prepare-database-codeql)

*   **Simple Idea:** CodeQL is a powerful tool that lets you investigate your code for security flaws. Think of it like a detective's toolkit. Instead of running it automatically inside GitHub, this module is about using the **CodeQL command-line tool (CLI)** yourself. This gives you more control and lets you run inspections on your own computer or server.

*   **The Detective's Process (Three Main Steps):**
    1.  **Create a Database:** First, the detective takes all the evidence (your source code) and organizes it into a structured **database**. It's like taking messy piles of documents and filing them neatly so you can search them easily.
    2.  **Run Queries:** Next, the detective asks specific questions to find clues. These questions are called **queries**. A query might be, "Show me every place where user input is used to build a database command," which could find a major security flaw.
    3.  **Analyze Results:** Finally, the detective reviews the answers to the questions (the query results) to decide if a crime (a vulnerability) has been committed.

---

#### [1. What does CodeQL first do when you're creating a database?](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/2-how-prepare-database-codeql)

*   **Simple Idea:** This question asks about the very first step in the detective's process. Before you can ask any questions, you need to organize the evidence.
*   **The Process:** CodeQL reads through every single file of your source code. For each file, it creates a structured, "relational" representation of it. This means it understands how all the pieces of your code relate to each other—what function calls another, where data comes from, etc. It then puts all this structured information into the database.
*   **Simplified Answer:** It **extracts a single relational representation of each source file.** It's turning your code into a highly organized, searchable map.

---

#### [2. What is the format of the command for creating and analyzing a CodeQL database from the CLI?](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/3-run-codeql-database)

*   **Simple Idea:** When you use a command-line tool, you type commands in a specific order. This question asks for the correct order for using CodeQL.
*   **The Structure:** The structure is always `tool [action] [details]`.
    *   First, you name the tool you're using: `codeql`.
    *   Next, you say what *major action* you want to perform, like `database` or `query`. This is the `[command]`.
    *   Finally, you give the specific detail of that action, like `create` or `analyze`. This is the `[subcommand]`.
*   **Example:** `codeql database create` (Tool: codeql, Command: database, Subcommand: create).
*   **Simplified Answer:** The format is `codeql [command] [subcommand]`.

---

#### [3. By default, which severity level causes a pull-request check failure during code scanning?](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/4-understand-results)

*   **Simple Idea:** When CodeQL finds problems, it gives them a severity rating, like a doctor diagnosing an illness as minor, serious, or critical. When a developer tries to add new code (in a "pull request"), you can set up a rule that says, "If the code has any problems that are 'serious' or worse, don't let it in!" This question asks what the default "serious" level is.
*   **The Default Rule:** By default, GitHub considers any problem that CodeQL flags as an **`Error`** to be serious enough to block the new code. This is the highest level of non-security-related problem.
*   **Simplified Answer:** `Error`.

---

#### [4. Which is one way to optimize CodeQL analysis runtimes?](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/5-troubleshoot-your-results)

*   **Simple Idea:** The detective's work (running a CodeQL analysis) can sometimes be slow, especially on a very large case (a big codebase). This question asks for a way to speed things up.
*   **How to Make it Faster:** A computer's "thinking power" depends on two main things: its brain (CPU cores) and its short-term memory (RAM). If the detective's work is slow, giving them more "thinking power" will help.
*   **Simplified Answer:** **Increase the memory** (and/or the number of cores). More resources mean the analysis can run faster. Analyzing *less* code would also work, but increasing memory is a direct way to improve performance on the same amount of code.

---

#### [In a Nutshell:](https://learn.microsoft.com/en-us/training/modules/codebase-representation-codeql/7-summary)

Using the **CodeQL CLI** is like being a hands-on code detective. You first **create a database** to organize the evidence, then you **run queries** to ask questions and find vulnerabilities. The command format is always `codeql [command] [subcommand]`. The results are rated by severity, and by default, any **Error** will block new code. To make your investigation faster, you can give your computer more resources, like **increasing its memory**.
