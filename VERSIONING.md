# Versioning

This project follows a versioning pattern similar to [Semantic Versioning](https://semver.org/) (SemVer) for managing releases.

## Table of Contents

- [Versioning](#versioning)
  - [Table of Contents](#table-of-contents)
  - [Format](#format)
    - [Examples](#examples)
    - [What Counts as a Breaking Change](#what-counts-as-a-breaking-change)
  - [Release Process](#release-process)
    - [Typical Steps](#typical-steps)
    - [AI and Automation in Releases](#ai-and-automation-in-releases)
  - [Pre-release Versions](#pre-release-versions)
  - [Viewing Tags & Differences](#viewing-tags--differences)
  - [Questions or Issues?](#questions-or-issues)

## Format

Version numbers follow the structure:

`MAJOR.MINOR.PATCH`

- **MAJOR** – Incompatible API changes or major breaking updates  
- **MINOR** – Backward-compatible functionality and feature additions  
- **PATCH** – Backward-compatible bug fixes and small improvements

### Examples

| Version | Meaning                          |
| ------- | -------------------------------- |
| `0.1.0` | First public release / early dev |
| `0.1.1` | Bug fix                          |
| `0.2.0` | New non‑breaking feature         |
| `1.0.0` | Official stable release          |
| `1.0.1` | Bug fix after release            |
| `1.1.0` | New feature added                |
| `2.0.0` | Major breaking change            |

### What Counts as a Breaking Change

For documents, policies, and templates like the ones in this repository:

| Change                                                                       | Version   |
| ---------------------------------------------------------------------------- | --------- |
| Removing or renaming a file, or a required section of a template             | **MAJOR** |
| Adding a new requirement for contributors, such as a mandatory disclosure    | **MAJOR** |
| Adding a new file, an optional section, or new guidance                      | **MINOR** |
| Fixing typos, broken links, or unclear wording without changing the meaning  | **PATCH** |

## Release Process

All notable changes are documented in the [CHANGELOG.md](CHANGELOG.md) file.

### Typical Steps

1. Complete all features and fixes planned for the release
2. Update the `CHANGELOG.md` with categorized entries:  
   - **Added**, **Changed**, **Fixed**, **Removed**
3. Bump the version number in the project's files (e.g. `CITATION.cff`, or `package.json` and `package-lock.json`)
4. Commit changes with a version-related message (e.g. `chore: Release v1.2.0`)
5. Tag the release:

   ```bash
   git tag v1.2.0
   git push origin v1.2.0
   ```

6. (Optional) Create a GitHub release and paste the relevant changelog section

### AI and Automation in Releases

- AI agents may help prepare a release, for example by drafting changelog entries, updating version numbers, and opening a release pull request.
- A human maintainer reviews the release pull request, creates the tag, and publishes the release. AI agents and automations never publish releases on their own.
- Check release notes drafted with AI against the actual changes before you publish them.

## Pre-release Versions

For beta or release candidates, we use suffixes:

- `1.2.0-beta.1` – Beta release
- `2.0.0-rc.1` – Release candidate

These versions are intended for testing and may not be fully stable.

## Viewing Tags & Differences

List all version tags:

```bash
git tag
```

View differences between versions:

```bash
git log v1.1.0..v1.2.0
```

## Questions or Issues?

If you have questions about the versioning strategy or encounter version-related problems, feel free to open an issue on the [GitHub repository](https://github.com/dileepadev/community-standards/issues).
