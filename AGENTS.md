# AGENTS.md

## Project Overview

- Repository Name: *community-standards*  
- Purpose: Define standard guidelines and best practices for GitHub projects (branch naming, commit message style, pull request workflow, etc.).  
- Target Audience: Human contributors and AI / automation agents.

## Setup & Environment

- Clone repository:  

  ```bash
  git clone <repo-url>
  cd community-standards
  ```

- Dependencies: None required for basic markdown / git workflows.
- Optional tools (for maintainers / agents):
  - Markdown linter (e.g., `markdownlint`)
  - Spell checker for docs.
  - Link checker (e.g., `markdown-link-check`)
- Environment variables: Not needed, but use placeholders for examples (e.g. `<contact_email>`).

## Build / Validation Commands

- To validate documentation syntax or links:

  ```bash
  markdownlint .  
  markdown-link-check "**/*.md"
  ```

- To run any CI checks: check `.github/workflows/` directory.
- Before merging or submitting PRs, agents should ensure no broken links in docs, consistent formatting, and that all guidelines are followed.

## Code Style & Commit / Branch Conventions

- **Branch Naming**  
  - Follow [BRANCH_NAMING_GUIDELINES.md](https://github.com/dileepadev/community-standards/blob/main/BRANCH_NAMING_GUIDELINES.md) - This file contains the branch naming guidelines of the project. The branch naming guidelines provide guidance on how to name branches in a consistent and meaningful way.

- **Commit Messages**
  - Follow [COMMIT_MESSAGE_GUIDELINES.md](https://github.com/dileepadev/community-standards/blob/main/COMMIT_MESSAGE_GUIDELINES.md) - This file contains the commit message guidelines of the project. The commit message guidelines provide guidance on how to write clear and informative commit messages when making changes to the project's codebase.

- **Pull Request Titles / Descriptions**
  - Follow [PULL_REQUEST_TEMPLATE.md](https://github.com/dileepadev/community-standards/blob/main/.github/PULL_REQUEST_TEMPLATE.md) - This file contains the pull request template. This template provides a structured way for contributors to submit code changes to the project.

## Testing & Review Process

- Tests: None for docs-only parts, unless new tooling is added.
- Review: All proposed changes should be peer-reviewed — at least one maintainer or contributor.
- Lint / formatting: Agent should ensure that documentation files pass markdown lint, link check, and style consistency before PR draft or merge.

## Security & Other Considerations

- DO NOT include passwords, private keys, or credentials in any file or example.
- Example data (emails, etc.) should use placeholder or fake domains (e.g., `user@example.com`).
- When updating security‑related guidelines (e.g., contact address, policies), double-check correctness.

## File Structure Notes

- This repository contains several guideline files (`BRANCH_NAMING_GUIDELINES.md`, `COMMIT_MESSAGE_GUIDELINES.md`, etc.). If an example or rule is changed in one, ensure consistency across the others.
- `.github/ISSUE_TEMPLATE/` and `PULL_REQUEST_TEMPLATE.md` are used by GitHub for issue/PR scaffolding — agents should respect those formats.

## Common Gotchas

- Examples should be sufficiently general — avoid internal or very project‑specific references unless documented.
- Ensure the email/contact address is correct everywhere.
- Always check for dead links in markdown.
- When examples are modified, also update any example usages in doc files.

## How Agents Should Use This File

- Agents should prefer instructions in `AGENTS.md` over guessing or human docs when performing tasks like setup, linting, commit message formatting.
- For nested contexts (if this repo had submodules or sub‑directories with different rules), agents should look for `AGENTS.md` in the relevant subdirectory first.
- Human overrides (prompts, direct instructions) take precedence over this file, but this file provides the default behavior.

## Contact & Maintenance

- If you spot mistakes, outdated instructions, or missing sections here, open an issue or submit a PR.
- When a new tool or checking workflow is added (e.g. a new linter, or spelling check), update this file accordingly.
- Maintain this file alongside other docs to ensure consistency.
