# Commit Message Guidelines

A good commit message should be descriptive and provide context about the changes made. This helps improve code review, debugging, and long-term maintainability.

Table of Contents:

- [Commit Message Guidelines](#commit-message-guidelines)
  - [Commit Message Format](#commit-message-format)
    - [`<type>`](#type)
    - [`<scope>`](#scope)
    - [`<short message>`](#short-message)
    - [`<optional issue references>`](#optional-issue-references)
    - [`<optional PR reference>`](#optional-pr-reference)
    - [`<optional longer description>`](#optional-longer-description)
    - [`<optional trailers>`](#optional-trailers)
  - [Issue and PR References](#issue-and-pr-references)
    - [Best Practices](#best-practices)
    - [Examples for Issue and PR References](#examples-for-issue-and-pr-references)
    - [Summary Table for Issue and PR Linking (with Scope)](#summary-table-for-issue-and-pr-linking-with-scope)
  - [AI Attribution Trailers](#ai-attribution-trailers)
    - [Examples with AI Attribution](#examples-with-ai-attribution)
  - [Commits by AI Agents](#commits-by-ai-agents)
  - [✅ Summary Examples with All Fields](#-summary-examples-with-all-fields)

## Commit Message Format

Use the following format for commit messages:

```md
<type>(<scope>): <short message> (<optional issue references>) (<optional PR reference>)

<optional longer description>

<optional trailers>
```

### `<type>`

The `<type>` field indicates the nature of the changes made in the commit. Use one of the following values:

| Type     | Description                                                   |
|----------|---------------------------------------------------------------|
| feat     | A new feature or enhancement to existing functionality.       |
| fix      | A bug fix or correction of an issue.                          |
| docs     | Documentation updates (e.g., README, code comments).          |
| style    | Code style changes (e.g., formatting, indentation, no logic). |
| refactor | Code refactoring without changing external behavior.          |
| perf     | Performance improvements.                                     |
| test     | Adding or modifying tests.                                    |
| chore    | Routine tasks, maintenance, or tooling changes.               |

### `<scope>`

The `<scope>` is optional, but recommended. It helps clarify which part of the project the commit affects. For example:

| Scope         | Description                                           |
|---------------|-------------------------------------------------------|
| repo          | Project-wide configuration or setup                   |
| config        | Build scripts, environment, or settings               |
| auth          | Authentication logic or features                      |
| api           | API endpoints or integrations                         |
| ui            | User interface components or styling                  |
| db            | Database models or queries                            |

### `<short message>`

A concise summary of what the commit does.

Writing Tips:

- Use the imperative mood (e.g., “Add” not “Added”)
- Capitalize the first letter
- Don’t end with a period
- Keep under 50 characters if possible
- Be specific (e.g., “Add agent tools” > “Update code”)
- Avoid "I", "this commit", or "fix" as vague verbs

### `<optional issue references>`

Optionally link the commit to relevant issues using GitHub keywords such as `fixes`, `closes`, `resolves`, or `refs`. Multiple issues can be referenced by separating them with commas.

### `<optional PR reference>`

Optionally link the commit to a pull request using the format `(#<number>)`. This should be placed at the end of the commit message.

### `<optional longer description>`

An optional detailed description of the changes made in the commit. This can include the reasoning behind the changes, implementation details, or any other relevant information. Separate this section from the header with a blank line.

### `<optional trailers>`

Optional `Key: value` lines at the very end of the message, separated from the description by a blank line, such as `Assisted-by:`, `Co-authored-by:`, or `Signed-off-by:`. Use them to credit co-authors and to disclose AI involvement. See [AI Attribution Trailers](#ai-attribution-trailers).

## Issue and PR References

Use GitHub keywords to link commits to issues, and standard notation for PRs.

### Best Practices

- **Pull Requests**: Use `(#<number>)` at the very end of the header. This is automatically recognized by GitHub.
  - ✅ `(#5)`
  - 🚫 `(pr #5)` or `refs #5` for the PR itself.
- **Issues**: Use standard GitHub keywords (`fixes`, `refs`, `closes`, `resolves`) in parentheses before the PR number.

### Examples for Issue and PR References

**Straightforward PR reference:**

```md
chore(repo): Migrate v1.1.0 codebase to new repository (#5)
```

**Issue + PR:**

```md
fix(auth): Prevent session expiration bug (fixes #42) (#102)
```

**Multiple Issues + PR:**

```md
chore(repo): Migrate v1.1.0 codebase to new repository (refs #1, #2) (#5)
```

### Summary Table for Issue and PR Linking (with Scope)

| Purpose                | Example Commit Message                                              | Result                             |
| ---------------------- | ------------------------------------------------------------------- | ---------------------------------- |
| Close single issue     | `fix(ui): Resolve button alignment issue (fixes #12) (#100)`        | Closes #12, links PR #100          |
| Reference single issue | `docs(config): Clarify setup instructions (refs #34) (#105)`        | Links issue #34, PR #105           |
| Reference PR Only      | `chore(deps): Bump version (#45)`                                   | Links PR #45                       |
| Close multiple issues  | `feat(api): Add registration (fixes #56, #57) (#200)`               | Closes #56, #57, links PR #200     |
| Mixed References       | `fix(api): Handle edge case (fixes #12, refs #23) (#150)`           | Closes #12, refs #23, links PR #150|
| Multiple PRs (rare)    | `chore(repo): Sync repos (#5, #6)`                                  | Links PR #5 and #6                 |

## AI Attribution Trailers

When AI tools or AI agents generate part of a change (AI involvement **Level 2 or higher**, as defined in the [AI Policy](AI_POLICY.md)), say so in the commit message with a trailer. For Levels 0-1, trailers are optional.

| Trailer           | When to use                                                                                                                        | Example                                       |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| `Assisted-by:`    | An AI tool or agent generated part of the change. Name the tool, and the model if you know it.                                     | `Assisted-by: GitHub Copilot`                 |
| `Co-authored-by:` | A person co-wrote the change. An AI agent may also be credited this way, for example when its tool adds the trailer automatically. | `Co-authored-by: Jane Doe <jane@example.com>` |
| `Signed-off-by:`  | A person certifies that they have the right to submit the change (Developer Certificate of Origin). **Only people may add it.**    | `Signed-off-by: Jane Doe <jane@example.com>`  |

Follow these rules:

- Put trailers at the very end of the message, one per line, after a blank line.
- Add one trailer for each AI tool or agent that generated part of the change.
- Use the format `Assisted-by: <tool> (<model>)` when you know the model, for example `Assisted-by: Cursor (<model-name>)`.
- Never add a `Co-authored-by:` or `Signed-off-by:` trailer for a person who did not take part, and never let an AI agent add `Signed-off-by:`.

### Examples with AI Attribution

**AI-assisted commit (Level 2):**

```md
feat(api): Add pagination to search results (refs #87)

Assisted-by: GitHub Copilot
```

**Commit made by an AI agent (Level 4):**

```md
docs(README): Fix broken links in setup guide (fixes #91)

Replace three links that pointed to removed pages.

Co-authored-by: <agent-name> <agent-email>
```

## Commits by AI Agents

AI agents follow the same format as everyone else, plus these rules:

- Make small commits that each contain one logical change, with a clear `<type>` and `<scope>`.
- Explain *why* in the description when the reason for a change is not obvious.
- Reference the issue the agent is working on, for example `(refs #12)`. Never invent issue or pull request numbers.
- Identify the agent in every commit: as the commit author, or with an `Assisted-by:` or `Co-authored-by:` trailer.
- Never add `Signed-off-by:` for a person, and never commit using another person's identity.
- Never rewrite or force-push history on shared branches.

## ✅ Summary Examples with All Fields

```md
feat(api): Add login endpoint (fixes #12) (#101)

This adds a new login endpoint to the API that allows users to authenticate using their email and password.
```

```md
fix(auth): Prevent session expiration bug (fixes #42) (#102)
```

```md
chore(repo): Migrate v1.1.0 codebase to new repository (refs #1, #2) (#5)
```

```md
chore(deps): Bump version (#45)
```

```md
test(auth): Add tests for token refresh (refs #58) (#110)

Cover expired, revoked, and malformed refresh tokens.

Assisted-by: Claude Code
```
