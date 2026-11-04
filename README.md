# Community Standards

This repository includes community standards that I personally use for my projects on GitHub.

![Community Standards](https://dileepadev.github.io/images/community-standards/preview.png)

## 🤖 Built for the AI Era

Projects today are built with every kind of AI involvement, from asking a chatbot a quick question to AI agents that open pull requests on their own. Starting with v2.0.0, these standards cover all of it, so every project has clear rules for how AI may be used, how its use is disclosed, and who is accountable.

| Level | Name              | Summary                                                                     |
| ----- | ----------------- | --------------------------------------------------------------------------- |
| 0     | Human-authored    | No generative AI is used.                                                   |
| 1     | AI-supported      | AI answers questions, explains, or reviews; people write the content.       |
| 2     | AI-assisted       | AI generates parts; people edit them and understand every line.             |
| 3     | Human-in-the-loop | AI generates most of the work; a person directs and approves each step.     |
| 4     | Agent-driven      | An AI agent works on its own; a human sponsor reviews the result.           |
| 5     | Fully automated   | Registered automations run pre-approved tasks inside strict guardrails.     |

The key ideas:

- **A person is always accountable** for every contribution, whatever tools produced it.
- **Disclosure is built in.** Pull requests declare their AI involvement level, and commits use `Assisted-by:` trailers.
- **AI agents have clear rules.** [AGENTS.md](AGENTS.md) tells agents how to work in the repository, and the [🤖 Agent Task](.github/ISSUE_TEMPLATE/agent_task.md) template gives them well-scoped tasks.
- **Oversight grows with autonomy.** The more independently AI works, the stronger the review and guardrails around it.

Read the full [AI Policy](AI_POLICY.md) for details.

## 🚀 Using These Standards

1. Copy the files into your repository, keeping the `.github/` folder structure.
2. Replace the project-specific details: the project name and links, the `dileepadev` username (in the issue templates and `.github/CODEOWNERS`), and the contact email `contact@dileepa.dev`.
3. Review [AI_POLICY.md](AI_POLICY.md), and update its **Project AI Declaration** and **Automation Register** for your project.
4. Update the project-specific sections of [AGENTS.md](AGENTS.md), such as the project overview, structure, and commands.
5. Create the labels that the templates and policies use: `bug`, `documentation`, `enhancement`, `feature request`, `feedback`, `other`, `ai-assisted`, `ai-agent`, and `breaking change`.
6. Configure your repository settings:
   - Protect the default branch: require pull requests, reviews from Code Owners, and passing status checks.
   - Require approval before workflows run on pull requests from outside contributors and AI agents.
   - Enable private vulnerability reporting, secret scanning, and push protection.
   - If low-quality automated contributions become a problem, use GitHub's interaction limits and contribution controls, for example to limit who can open pull requests.

## 📂 File Structure

```markdown
community-standards/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── agent_task.md
│   │   ├── bug_report.md
│   │   ├── documentation_update.md
│   │   ├── feature_request.md
│   │   ├── feedback.md
│   │   └── other.md
│   ├── CODEOWNERS
│   └── PULL_REQUEST_TEMPLATE.md
├── .markdownlint.jsonc
├── AGENTS.md
├── AI_POLICY.md
├── BRANCH_NAMING_GUIDELINES.md
├── CHANGELOG.md
├── CITATION.cff
├── CODE_OF_CONDUCT.md
├── COMMIT_MESSAGE_GUIDELINES.md
├── CONTRIBUTING.md
├── LICENSE
├── PULL_REQUEST_GUIDELINES.md
├── README.md
├── SECURITY.md
├── TODO.md
└── VERSIONING.md
```

- [.github/](.github/) - GitHub-specific configuration: issue and pull request templates, and code owners.

  - [ISSUE_TEMPLATE/](.github/ISSUE_TEMPLATE/) - Pre-made forms that guide contributors to report consistent issues.

    - [agent_task.md](.github/ISSUE_TEMPLATE/agent_task.md) - Form for defining well-scoped tasks for AI agents, with a human sponsor.

    - [bug_report.md](.github/ISSUE_TEMPLATE/bug_report.md) - Form for reporting bugs with all necessary details, including any AI assistance.

    - [documentation_update.md](.github/ISSUE_TEMPLATE/documentation_update.md) - Form for suggesting documentation improvements.

    - [feature_request.md](.github/ISSUE_TEMPLATE/feature_request.md) - Form for proposing new features and enhancements.

    - [feedback.md](.github/ISSUE_TEMPLATE/feedback.md) - Form for sharing general feedback and ideas.

    - [other.md](.github/ISSUE_TEMPLATE/other.md) - Form for issues that don't fit other categories.

  - [CODEOWNERS](.github/CODEOWNERS) - Required human reviewers for every file, including policy and AI agent instruction files.

  - [PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md) - Checklist to ensure pull requests are complete, reviewed properly, and disclose their AI involvement.

- [.markdownlint.jsonc](.markdownlint.jsonc) - Markdown lint rules shared by contributors and AI agents.

- [AGENTS.md](AGENTS.md) - Instructions for AI coding agents: project structure, commands, conventions, workflow, and boundaries.

- [AI_POLICY.md](AI_POLICY.md) - Rules for using AI tools and AI agents: involvement levels, disclosure, accountability, and automation.

- [BRANCH_NAMING_GUIDELINES.md](BRANCH_NAMING_GUIDELINES.md) - Standards for naming branches clearly and consistently, including release and AI agent branches.

- [CHANGELOG.md](CHANGELOG.md) - Record of all project updates, features, and fixes organized by version.

- [CITATION.cff](CITATION.cff) - Proper format for citing this project in academic or formal references.

- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) - Community standards for respectful and inclusive behavior (Contributor Covenant 3.0), including AI tools and automated participants.

- [COMMIT_MESSAGE_GUIDELINES.md](COMMIT_MESSAGE_GUIDELINES.md) - Standards for writing clear and descriptive commit messages, including AI attribution trailers.

- [CONTRIBUTING.md](CONTRIBUTING.md) - Step-by-step guide for contributing to the project, including with AI tools and AI agents.

- [LICENSE](LICENSE) - Legal license defining how the project can be used, modified, and distributed.

- [PULL_REQUEST_GUIDELINES.md](PULL_REQUEST_GUIDELINES.md) - Best practices for naming, describing, reviewing, and submitting pull requests, including those opened by AI agents.

- [README.md](README.md) - This file: overview and structure of the project.

- [SECURITY.md](SECURITY.md) - Guidelines for responsibly reporting security vulnerabilities, including AI-assisted reports and AI agent risks.

- [TODO.md](TODO.md) - Planned tasks and features scheduled for upcoming releases.

- [VERSIONING.md](VERSIONING.md) - Versioning strategy for tracking releases and backward compatibility.

## 💬 Contact

If you have any questions or suggestions regarding these community standards, feel free to open an issue or submit a pull request in this repository.

You can also reach me via email at: **<contact@dileepa.dev>**
