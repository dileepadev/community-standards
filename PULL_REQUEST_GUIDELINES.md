# Pull Request Guidelines

When creating a pull request, please follow the commit message convention for the pull request title. This convention helps in providing a clear and standardized way to communicate the nature of the changes.

## Table of Contents

- [Pull Request Guidelines](#pull-request-guidelines)
  - [Table of Contents](#table-of-contents)
  - [PR Title Format](#pr-title-format)
  - [Examples](#examples)
  - [PR Description](#pr-description)
  - [Keep Pull Requests Reviewable](#keep-pull-requests-reviewable)
  - [AI-Assisted Pull Requests](#ai-assisted-pull-requests)
  - [Pull Requests Opened by AI Agents](#pull-requests-opened-by-ai-agents)
  - [Review and Merge Requirements](#review-and-merge-requirements)

## PR Title Format

The pull request title should follow the format:

```md
<type>(<branch>): <message> [#issue_number]
```

- `<type>`: Type of the change. Use one of the following:

  - `feat`: A new feature or enhancement to existing functionality.
  - `fix`: A bug fix or correction of an issue.
  - `docs`: Documentation updates (e.g., README, comments).
  - `style`: Code style changes (e.g., formatting, indentation).
  - `refactor`: Code refactoring or restructuring without changing functionality.
  - `perf`: Performance improvements.
  - `test`: Adding or modifying tests.
  - `chore`: Routine tasks, maintenance, or tooling changes.

- `<branch>`: Branch where the changes are made, e.g., `feat/<name>` (use feature branches for new work, as described in the [Branch Naming Guidelines](BRANCH_NAMING_GUIDELINES.md)).

- `<message>`: A short, clear, and concise description of the changes.

- `[#issue_number]` (optional): If the pull request is related to a GitHub issue, include the issue number.

## Examples

- `feat(feat/new-footer): Add new footer [#09]`
- `fix(fix/login): Resolve issue with login [#123]`
- `docs(docs/readme): Update installation instructions`
- `style(style/formatting): Format code according to style guide`
- `docs(copilot/fix-broken-links): Fix broken links in README [#45]`

## PR Description

Use the [pull request template](.github/PULL_REQUEST_TEMPLATE.md) and complete every required section:

- **Description:** what changed and why.
- **Type of Change** and **Related Issues**, for example `Closes #123`.
- **🤖 AI Involvement:** the highest AI involvement level that applies (0-5). For Level 2 and above, also list the tools used, how AI was used, and how you verified the result. The levels are defined in the [AI Policy](AI_POLICY.md).
- **Checklist:** check only the items that are true.

## Keep Pull Requests Reviewable

- Keep each pull request focused on one issue or change. Split large changes into smaller pull requests.
- Do not mix unrelated changes, such as reformatting a whole file while fixing a typo.
- Explain anything a reviewer might not expect, including what you could not test.

## AI-Assisted Pull Requests

- Add the `ai-assisted` label to pull requests at Levels 2-3, and the `ai-agent` label to pull requests at Levels 4-5.
- The author must review and understand every change before requesting a review, and must answer review questions personally.
- Reviewers may ask for more context, more tests, or a smaller change before they review AI-generated work.

## Pull Requests Opened by AI Agents

When an AI agent opens a pull request (Levels 4-5):

1. It is linked to an issue or task that a maintainer approved, and it names its **human sponsor** in the **🤖 AI Involvement** section.
2. It is opened as a **draft**. The sponsor reviews it and then marks it as ready for review.
3. Its description summarizes the agent's plan, the changes made, the checks it ran, and anything it could not verify.
4. The agent never approves, merges, or force-pushes its own pull request, and never bypasses required checks.
5. Maintainers should require approval before workflows run on pull requests from AI agents and first-time contributors.

## Review and Merge Requirements

- At least one human maintainer must review every pull request before it is merged. No pull request is merged without a person reviewing it.
- Code owners review changes to the files they own (see [.github/CODEOWNERS](.github/CODEOWNERS)).
- All required status checks must pass.
- When an AI agent produced a pull request, the approver should be someone other than the person who started the agent, whenever the project has more than one maintainer.
- Review changes to policy, security, and AI agent instruction files (`AI_POLICY.md`, `AGENTS.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, and `.github/`) with extra care, and check them for hidden characters and for instructions aimed at AI agents.

Please adhere to these guidelines to maintain consistency and clarity.
