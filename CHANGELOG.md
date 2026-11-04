# Changelog

All notable changes to this project are documented in this file.

Changes are organized into the following categories:

- **Added:** New features or functionality introduced to the project.
- **Changed:** Modifications to existing functionality that do not add new features.
- **Fixed:** Bug fixes that resolve issues or correct unintended behavior.
- **Removed:** Features or components that have been removed from the project.

## [Unreleased]

- Changes for the next release are available in development branches.

## [v2.0.0] - 2026-11-04

### Added - v2.0.0

- Standards for AI-assisted, AI agent-driven, and fully automated development. Six AI involvement levels (0-5), from human-authored to fully automated, each with disclosure, accountability, and review requirements.
- New files:
  - `AI_POLICY.md`
    - AI involvement levels, disclosure, contributor responsibilities, rules for AI agents, fully automated workflows with an Automation Register, licensing, privacy, security, enforcement, and a Project AI Declaration
  - `AGENTS.md`
    - Instructions for AI coding agents: project structure, commands, writing conventions, Git workflow, boundaries, and security
  - `.github/ISSUE_TEMPLATE/agent_task.md`
    - Issue template for well-scoped tasks delegated to AI agents, with a human sponsor
  - `.github/CODEOWNERS`
    - Human ownership of every file, with policy and AI agent instruction files listed explicitly
  - `.markdownlint.jsonc`
    - Markdown lint rules shared by contributors and AI agents
- New labels used by the templates and the AI policy: `ai-assisted`, `ai-agent`, and `breaking change`

### Changed - v2.0.0

- **Breaking:** `.github/PULL_REQUEST_TEMPLATE.md`
  - Add a required AI Involvement section, a Breaking Change option, and checklist items for AI disclosure, human review, and secrets
- **Breaking:** `CODE_OF_CONDUCT.md`
  - Upgrade from Contributor Covenant 2.0 to 3.0 (licensed under CC BY-SA 4.0)
  - Add a section on AI tools and automated participants
- Update selected files:
  - `.github/ISSUE_TEMPLATE/*.md`
    - Add an AI Assistance section (required in bug reports, and in other issues when AI was used)
  - `CONTRIBUTING.md`
    - Add Before You Start, Using AI Tools, and Contributing with AI Agents sections
  - `COMMIT_MESSAGE_GUIDELINES.md`
    - Add AI attribution trailers (`Assisted-by:`, `Co-authored-by:`, `Signed-off-by:`) and rules for commits by AI agents
  - `BRANCH_NAMING_GUIDELINES.md`
    - Add release branches and AI agent branches
  - `PULL_REQUEST_GUIDELINES.md`
    - Add PR description, reviewability, AI-assisted pull request, AI agent pull request, and review and merge requirements
  - `SECURITY.md`
    - Add supported versions, AI-assisted reports, AI and agent security, and new maintainer responsibilities
  - `VERSIONING.md`
    - Add breaking-change rules for standards and rules for AI and automation in releases
  - `README.md`
    - Add an AI-era overview, adoption steps, and the updated file structure
  - `CITATION.cff`
    - Update the version, release date, abstract, and keywords

### Fixed - v2.0.0

- `PULL_REQUEST_GUIDELINES.md`
  - Use the `feat/` branch prefix from the branch naming guidelines instead of `feature/`
- `BRANCH_NAMING_GUIDELINES.md`
  - Describe `main` as the stable version of the project instead of the website
- `VERSIONING.md`
  - Complete the table of contents, fix a closing code fence, and generalize the version bump step
- `CITATION.cff`
  - Fix the author entry so the file passes Citation File Format 1.2.0 validation
  - Update the version, which was not changed in v1.1.0

## [v1.1.0] - 2026-03-25

### Changed - v1.1.0

- Update selected files:
  - `.github/ISSUE_TEMPLATE/feature_request.md`
    - Add enhancement label
  - `COMMIT_MESSAGE_GUIDELINES.md`
    - Add option for PR and Issue
    - Restructure
  - `CHANGELOG.md`
    - Add category items with versions
  - `VERSIONING.md`
    - Update examples

## [v1.0.0] - 2026-01-12

### Added - v1.0.0

- Initial public release of the community-standards repository. Establishes the foundational repository structure, community governance, contribution workflows, and documentation standards required to support a scalable, maintainable, and collaborative open-source project.
- Defines baseline standards for contributions, versioning, and release processes (v1.0.0).
- No breaking changes introduced. This release provides initial governance and documentation for future contributions.
- Repository contents and templates added:
  - [community-standards/](./) - Root directory of the repository
    - [.github/](./.github) - GitHub-specific files (workflows, templates, etc.)
      - [ISSUE_TEMPLATE/](./.github/ISSUE_TEMPLATE) - Contains all issue templates
        - [bug_report.md](./.github/ISSUE_TEMPLATE/bug_report.md) - Template for reporting bugs
        - [documentation_update.md](./.github/ISSUE_TEMPLATE/documentation_update.md) - Template for documentation updates
        - [feature_request.md](./.github/ISSUE_TEMPLATE/feature_request.md) - Template for suggesting new features
        - [feedback.md](./.github/ISSUE_TEMPLATE/feedback.md) - Template for general feedback
        - [other.md](./.github/ISSUE_TEMPLATE/other.md) - Template for other types of issues
      - [PULL_REQUEST_TEMPLATE.md](./.github/PULL_REQUEST_TEMPLATE.md) - Template for pull request submissions
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

<!-- e.g., -->
<!-- Unreleased -->
<!-- v2.0.0 -->
<!-- v1.1.0 -->
<!-- v1.0.0 -->
<!-- v0.0.1 -->

[Unreleased]: https://github.com/dileepadev/community-standards/branches
[v1.0.0]: https://github.com/dileepadev/community-standards/releases/tag/v1.0.0
[v1.1.0]: https://github.com/dileepadev/community-standards/releases/tag/v1.1.0
[v2.0.0]: https://github.com/dileepadev/community-standards/releases/tag/v2.0.0
