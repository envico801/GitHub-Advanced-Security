Q:: What is the fundamental shift in security philosophy that GitHub Advanced Security (GHAS) promotes, moving away from traditional methods?
A:: GHAS shifts security from being a final, separate step (like an inspection after a building is finished) to an integrated, continuous process built into every stage of development. This "shift-left" approach makes finding and fixing vulnerabilities faster, cheaper, and less disruptive.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/4-respond-to-security-alerts)

Q:: In the analogy of building a house, what role does Code Scanning play, and why is this role most effective early in the construction process?
A:: Code Scanning acts as the "blueprint inspector." It's most effective early because it finds structural weaknesses (vulnerabilities) in the code (the "blueprints") *before* they are built into the final product. Fixing a flaw on paper is much easier and cheaper than fixing a crack in the foundation of a finished house.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/4-respond-to-security-alerts)

Q:: Which GitHub Advanced Security feature is specifically designed to act as a "password guard," preventing sensitive information like API keys or passwords from being accidentally left in the code?
A:: Secret Scanning. Its job is to detect and even block commits that contain secrets, ensuring they don't become part of the project's public history.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/2-what-is-github-advanced-security)

Q:: How do the Dependency Graph and Dependabot work together to secure a project's software supply chain?
A:: The Dependency Graph acts as a complete "parts list" for the software. Dependabot reads this list and cross-references it with the GitHub Advisory Database (a list of known vulnerabilities) to check for any unsafe parts. If a match is found, it raises an alert, much like a safety recall notice for a faulty car part.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/3-create-culture-around-security)

Q:: At what specific point in a developer's workflow does GitHub Advanced Security typically intervene to check for vulnerabilities?
A:: GHAS intervenes when a developer submits new code in a "pull request," *before* it is merged into the main project. This allows developers to see and fix security issues immediately within their normal workflow, while the context is still fresh in their minds.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/4-respond-to-security-alerts)

Q:: Why is it a security risk for a project to have outdated dependencies?
A:: Outdated dependencies are a risk because new vulnerabilities are constantly being discovered in software components. An old version of a component might contain a known security flaw that attackers can exploit. Dependabot helps mitigate this risk by flagging outdated dependencies that have known security advisories.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/3-create-culture-around-security)

Q:: Complete the sentence: To secure a project, GHAS uses Code Scanning to inspect the ______, Secret Scanning to protect ______, and Dependabot to manage the security of its ______.
A:: ...Code Scanning to inspect the **code's blueprints** (for vulnerabilities), Secret Scanning to protect **secrets** (like passwords and keys), and Dependabot to manage the security of its **dependencies** (third-party parts).
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/introduction-github-advanced-security/6-summary)
