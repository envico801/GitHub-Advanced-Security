## 1. [GitHub Advanced Security Part 1 of 2](https://learn.microsoft.com/en-us/training/paths/github-advanced-security/)

### 1.1. [Introduction to GitHub Advanced Security](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/)

#### [1. What is GitHub Advanced Security (GHAS)?](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/2-what-is-github-advanced-security)

*   **Simple Idea:** Think of GitHub as a giant workshop where programmers build software. GitHub Advanced Security (GHAS) is like having a team of specialized security experts built right into that workshop. Their job is to check the software for safety problems *as it's being built*, not just at the end.

*   **What This "Security Team" Does (The 3 Main Tools):**
    *   **Code Scanning (The Blueprint Inspector):** This tool reads the actual code (the "blueprints" of the software) to look for common security flaws and weaknesses. It's like an expert inspector who reads the blueprints for a new building to find structural weaknesses *before* it's built.
        *   *Example:* It can find a "door" in the code that an attacker could use to sneak in and steal data (like a vulnerability called "SQL Injection").

    *   **Secret Scanning (The Password Guard):** Programmers often use "secrets" like passwords, API keys, and access tokens to connect their software to other services. This tool's job is to make sure no one accidentally leaves a master key lying around in the public code.
        *   *Example:* If a developer accidentally copies and pastes a password for their company's database into the code, this tool acts like a security guard that spots it and says, "Hey, you can't leave this here!" It can even block the code from being saved.

    *   **Dependabot (The Supply Chain Manager):** Software is rarely built from scratch. Developers use many pre-made parts and tools from other people (called "dependencies"). Dependabot is like a diligent supply chain manager who keeps track of all these parts.
        *   *Example:* Imagine your software uses a pre-built part for processing payments. If a security flaw is discovered in that payment part, Dependabot will automatically get an alert (like a safety recall notice) and will even try to order and install the new, safer version for you.

---

#### [2. How does code scanning contribute to the security of a software development project?](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/4-respond-to-security-alerts)

*   **Simple Idea:** Code scanning's main job is to find security problems **early**, while the software is still being written.

*   **How it Helps (The "Why"):**
    *   Think of it like finding a flaw in a building's blueprint versus discovering a crack in the foundation after the building is already open. It's much cheaper, faster, and safer to fix problems on paper (in the code) than to fix them in the real world (in the live software).
    *   When a developer writes new code and wants to add it to the main project (this is called a "pull request"), Code Scanning automatically checks it *before* it gets approved. It's like a mandatory inspection for every new part added to the building, ensuring new problems aren't introduced.

---

#### [3. How does Dependabot use the dependency graph in GitHub Advanced Security (GHAS)?](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/3-create-culture-around-security)

This has two parts: the "dependency graph" and "Dependabot."

*   **1. What is the Dependency Graph? (The Parts List)**
    *   **Simple Idea:** The Dependency Graph is a detailed list of every single part used to build your software.
    *   **Analogy:** Imagine your software is a car. You use an engine from Company A, tires from Company B, and a radio from Company C. The Dependency Graph is a list of all these parts. But it goes deeper—it also lists all the parts *inside* the engine (like its spark plugs and pistons). It's a complete "bill of materials" for your entire car.

*   **2. How Dependabot Uses This Graph (The Recall Check)**
    *   **Simple Idea:** Dependabot reads the parts list and checks it against a global database of known safety problems.
    *   **How it Works:**
        1.  Dependabot takes your software's complete parts list (the Dependency Graph).
        2.  It compares that list against a huge, constantly updated database of known security flaws (the "GitHub Advisory Database").
        3.  If it finds a match—for example, it sees you're using tires from a batch that is known to be faulty—it immediately raises an alert. This is how it **cross-references dependency data with the GitHub Advisory Database**.

---

#### [4. How does GitHub Advanced Security (GHAS) help integrate security into each step of the software development life cycle?](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/4-respond-to-security-alerts)

*   **Simple Idea:** Instead of having security be a final, stressful inspection at the very end, GHAS builds security checks into the *entire* building process, from start to finish.

*   **The Old Way vs. The New Way (An Analogy):**
    *   **The Old Way (Security at the end):** Imagine building an entire skyscraper. Only *after* it's completely finished do you hire a single inspector to check everything. If they find a major problem in the foundation, it's a disaster to fix. This is slow, expensive, and risky.
    *   **The New Way (Integrated Security with GHAS):** GHAS is like having specialized inspectors on-site *every single day*:
        *   When the foundation is poured, a foundation expert inspects the blueprints (**Code Scanning**).
        *   As materials (parts from suppliers) arrive, the supply manager checks them for safety recalls (**Dependabot**).
        *   Security guards are always watching to make sure no master keys are left lying around (**Secret Scanning**).
    *   These checks happen **automatically every time a developer submits new work** (in a "pull request"). This means problems are found and fixed in minutes, right in the developer's workflow, not months later when they've become a huge, expensive mess.

---

#### [In a Nutshell:](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/6-summary)

GitHub Advanced Security (GHAS) isn't a single tool; it's a **built-in security team** for your software project. It has a **blueprint inspector (Code Scanning)** to find flaws in your design, a **password guard (Secret Scanning)** to protect your keys, and a **supply chain manager (Dependabot)** to make sure all your parts are safe. By having them work continuously, it makes security a normal part of the development day, not a scary final exam.
