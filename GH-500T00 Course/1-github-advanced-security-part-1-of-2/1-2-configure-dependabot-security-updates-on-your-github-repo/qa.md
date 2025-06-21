Q:: Why is it crucial for a developer to manage not just the direct dependencies they choose, but also the indirect dependencies they don't?
A:: A project's security is only as strong as its weakest link. An indirect dependency (a "part-of-a-part") can contain a vulnerability, and even if you didn't choose it directly, it's still running in your software. Failing to track and update these hidden dependencies can leave a significant security hole.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/2-manage-your-dependencies-github)

Q:: What is the key difference in function between Dependabot and Dependency Review when securing a project's dependencies?
A:: Dependency Review is **proactive**; it acts as a "gatekeeper" on pull requests to *prevent* new vulnerable dependencies from being introduced. Dependabot is **reactive**; it acts as a "recall manager" for dependencies *already in* the project, alerting you when an existing part is found to be unsafe.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/6-dependency-review)

Q:: What are the two primary events that will trigger Dependabot to generate a new security alert for your repository?
A:: An alert is generated when: 1) A new vulnerability affecting one of your existing dependencies is published to the GitHub Advisory Database, or 2) You add a new dependency to your project, which is then scanned and found to have a pre-existing vulnerability.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/3-dependabot-alerts)

Q:: Using the analogy of building a car, what is the difference between a direct and an indirect dependency?
A:: A **direct dependency** is a major component you explicitly choose, like selecting an engine from Ford. An **indirect dependency** is a component that comes included with your choice, like the specific spark plugs inside that Ford engine, which you did not select yourself.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/2-manage-your-dependencies-github)

Q:: For Dependabot security updates to be enabled automatically on a repository for free, what condition must that repository meet?
A:: The repository must be public. This feature is provided by GitHub to help secure the open-source software ecosystem.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/4-dependabot-security-updates)

Q:: To manage your workflow in the security notifications inbox, what search query would you use to filter the view to show only the alerts that you have already processed and marked as resolved?
A:: You would use the search filter `is:done`. This helps organize the inbox by separating active alerts from those that have already been handled.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/5-manage-dependabot-notifications-reporting)

Q:: What is the primary source of information that Dependabot cross-references with your project's "parts list" (manifest) to identify security vulnerabilities?
A:: The GitHub Advisory Database. This is a comprehensive, constantly updated global database of known security vulnerabilities in software packages.
[Documentation Link](https://learn.microsoft.com/en-us/training/modules/configure-dependabot-security-updates-on-github-repo/3-dependabot-alerts)
