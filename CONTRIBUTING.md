# Contributing to community-standards

Thank you for your interest in contributing to [community-standards](https://github.com/dileepadev/community-standards)! We welcome contributions, including bug fixes, feature enhancements, documentation improvements, and other general improvements, whether you write them yourself, with the help of AI tools, or with an AI agent.

## Before You Start

- For anything larger than a small fix, [open an issue](https://github.com/dileepadev/community-standards/issues) first, so we can agree on the approach before you invest time.
- Check existing issues and pull requests to avoid duplicate work.
- If you plan to use AI tools or AI agents, read the [AI Policy](AI_POLICY.md).

## Getting Started

1. **Fork the repository**  
   Fork this repository to your GitHub account. This creates a copy of the repository in your account, allowing you to make changes without affecting the original repository.  
   To fork the repository, click the **Fork** button in the top right corner of this page or click [here to fork the repository](https://github.com/dileepadev/community-standards/fork).

2. **Clone your fork**  
   Clone your forked repository to your local machine using the following command:

   ```bash
   git clone https://github.com/<your-username>/community-standards.git
   ```

3. **Create a new branch**  
   Create a new branch for your changes. Follow the [branch naming guidelines](BRANCH_NAMING_GUIDELINES.md).

   ```bash
   git checkout -b your-branch-name
   ```

4. **Make changes and commit**  
   Make your changes and commit them with a descriptive commit message. Follow the [commit message guidelines](COMMIT_MESSAGE_GUIDELINES.md), including the [AI attribution trailers](COMMIT_MESSAGE_GUIDELINES.md#ai-attribution-trailers) when AI generated part of the change.

   ```bash
   git commit -m "feat: Add a new feature"
   ```

5. **Push your changes**  
   Push your changes to your forked repository.

   ```bash
   git push origin your-branch-name
   ```

6. **Submit a pull request**  
   To submit a pull request:
   - Go to your forked repository.
   - Click the **Compare & pull request** button next to your `your-branch-name`.
   - Add a title and description for your pull request. Follow the [pull request guidelines](PULL_REQUEST_GUIDELINES.md).
   - Complete the [pull request template](.github/PULL_REQUEST_TEMPLATE.md), including the **🤖 AI Involvement** section.
   - Click **Create pull request** and remember to add the relevant labels.

## Using AI Tools

AI tools are welcome. Whatever tools you use, **you are responsible for your contribution**:

- **Disclose** your AI involvement level (0-5) in the pull request template. When AI generated part of the change (Level 2 or higher), add an `Assisted-by:` trailer to your commits and the `ai-assisted` label to your pull request.
- **Review and understand** every line before you ask for a review. You must be able to explain your changes without AI help.
- **Verify** AI output: test it, and check that every file, command, link, and package it mentions actually exists.
- **Keep it focused.** Small, well-explained pull requests are reviewed faster than large generated ones.
- **Respond to reviews yourself** instead of passing reviewers' comments to an AI tool.

The [AI Policy](AI_POLICY.md) defines the AI involvement levels and what each one requires.

## Contributing with AI Agents

If an AI agent works on your behalf (Level 4), you are its **human sponsor** and are accountable for its work:

1. Give the agent a well-scoped task, ideally an issue created with the [🤖 Agent Task template](.github/ISSUE_TEMPLATE/agent_task.md) and approved by a maintainer.
2. Make sure the agent follows [AGENTS.md](AGENTS.md), which most agents read automatically.
3. Have the agent open a **draft** pull request with the `ai-agent` label and a completed **🤖 AI Involvement** section.
4. Review the agent's work yourself before you mark the pull request as ready for review.

Fully automated workflows (Level 5) are only allowed for automations listed in the [Automation Register](AI_POLICY.md#automation-register).

## Guidelines

- Follow the project's code style.
- Update documentation if necessary.
- Add tests if applicable.
- Ensure all tests pass before submitting your changes.
- Keep your pull request focused and avoid unrelated changes.
- Refer to the following templates and guidelines before submitting your changes:
  - [community-standards/](./) - Root directory of the repository
    - [.github/](./.github) - GitHub-specific files (workflows, templates, etc.)
      - [ISSUE_TEMPLATE/](./.github/ISSUE_TEMPLATE) - Contains all issue templates
        - [agent_task.md](./.github/ISSUE_TEMPLATE/agent_task.md) - Template for tasks delegated to AI agents
        - [bug_report.md](./.github/ISSUE_TEMPLATE/bug_report.md) - Template for reporting bugs
        - [documentation_update.md](./.github/ISSUE_TEMPLATE/documentation_update.md) - Template for documentation updates
        - [feature_request.md](./.github/ISSUE_TEMPLATE/feature_request.md) - Template for suggesting new features
        - [feedback.md](./.github/ISSUE_TEMPLATE/feedback.md) - Template for general feedback
        - [other.md](./.github/ISSUE_TEMPLATE/other.md) - Template for other types of issues
      - [CODEOWNERS](./.github/CODEOWNERS) - Required human reviewers for each file
      - [PULL_REQUEST_TEMPLATE.md](./.github/PULL_REQUEST_TEMPLATE.md) - Template for pull request submissions
    - [.markdownlint.jsonc](./.markdownlint.jsonc) - Markdown lint rules
    - [AGENTS.md](./AGENTS.md) - Instructions for AI agents
    - [AI_POLICY.md](./AI_POLICY.md) - Rules for using AI tools and AI agents
    - [BRANCH_NAMING_GUIDELINES.md](./BRANCH_NAMING_GUIDELINES.md) - Branch naming rules
    - [CHANGELOG.md](./CHANGELOG.md) - Record of project changes
    - [CITATION.cff](./CITATION.cff) - Standardized citation information for the repository
    - [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) - Contributor behavior guidelines
    - [COMMIT_MESSAGE_GUIDELINES.md](./COMMIT_MESSAGE_GUIDELINES.md) - Rules for writing commit messages
    - [CONTRIBUTING.md](./CONTRIBUTING.md) - How to contribute to the project
    - [LICENSE](./LICENSE) - Project license
    - [PULL_REQUEST_GUIDELINES.md](./PULL_REQUEST_GUIDELINES.md) - Pull request submission guidelines
    - [README.md](./README.md) - Project overview
    - [SECURITY.md](./SECURITY.md) - Security policy and reporting
    - [TODO.md](./TODO.md) - Tasks planned for future releases
    - [VERSIONING.md](./VERSIONING.md) - Versioning strategy for the project

## Code of Conduct

This project adheres to the **Contributor Covenant 3.0 Code of Conduct**. By participating, you agree to abide by its terms.  
Read the full Contributor Covenant Code of Conduct in the [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) file.

## Contact

If you have any questions or suggestions regarding these community standards, feel free to open an issue or submit a pull request in this repository.

You can also reach me via email at: **<contact@dileepa.dev>**
