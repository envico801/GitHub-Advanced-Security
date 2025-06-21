Q:: What is the primary difference in how standard Secret Scanning and "Push Protection" operate when a developer tries to commit code containing a secret?
A:: Standard Secret Scanning is **reactive**; it finds and alerts you about a secret *after* it has been committed. Push Protection is **proactive**; it acts as a gatekeeper that *blocks* the developer from committing the code in the first place, preventing the secret from ever entering the repository's history.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/4-use-secret-scanning)

Q:: Why are the settings for Secret Scanning locked and unchangeable on a public repository?
A:: The settings are locked because GitHub provides Secret Scanning as a free, standardized service to protect the entire public open-source community. This ensures a consistent baseline of security for all public projects. To gain control over the settings, the repository must be private and have a GitHub Advanced Security license.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/3-configure-secret-scanning)

Q:: When Secret Scanning finds a potential secret, what additional, crucial information does the "Validity Check" feature provide to help you prioritize your response?
A:: The Validity Check confirms whether the discovered secret is still **active** and can actually be used to access a service. This helps you prioritize alerts, allowing you to immediately address the most critical, live credentials over old, expired ones.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/4-use-secret-scanning)

Q:: What specific problem do "custom patterns" solve for an organization?
A:: They solve the problem of an organization using unique, internal secret formats that the default scanner wouldn't recognize. Custom patterns allow you to "teach" the scanner what your company-specific secrets look like, extending its detection capabilities beyond common, public service tokens.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/3-configure-secret-scanning)

Q:: The "security guard" analogy for Secret Scanning highlights that it searches more than just the current code. What other parts of a repository does it inspect?
A:: It inspects the project's entire history, developer notes (in "issues" and "pull requests"), and public comments. This comprehensive search ensures that secrets aren't hiding anywhere within the repository's data.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/2-what-is-secret-scanning)

Q:: To ensure the correct security team is notified when a secret is found, where in the repository settings must you go to configure the list of alert recipients?
A:: You must go to the **Advanced Security settings** of the repository. This is the central location for managing the configuration of all advanced security features, including who receives alerts.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/4-use-secret-scanning)

Q:: Complete the sentence: For a single organization, you can define up to 500 ____ to extend Secret Scanning's capabilities to find unique, internally-defined credentials.
A:: ...500 **custom patterns**...
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-use-secret-scanning-github-repository/3-configure-secret-scanning)
