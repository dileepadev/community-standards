# Security Policy

The [community-standards](https://github.com/dileepadev/community-standards) project team takes security issues very seriously. We appreciate your efforts to responsibly disclose any security vulnerabilities you find.

## Table of Contents

- [Security Policy](#security-policy)
  - [Table of Contents](#table-of-contents)
  - [Supported Versions](#supported-versions)
  - [Reporting a Vulnerability](#reporting-a-vulnerability)
  - [AI-Assisted Reports](#ai-assisted-reports)
  - [AI and Agent Security](#ai-and-agent-security)
  - [Bug Bounty Program](#bug-bounty-program)
  - [Maintainer Responsibilities](#maintainer-responsibilities)
  - [Disclosures](#disclosures)

## Supported Versions

| Version | Supported |
| ------- | --------- |
| 2.x     | ✅ Yes    |
| 1.x     | ❌ No     |

## Reporting a Vulnerability

If you discover a security vulnerability, please send an email to **<contact@dileepa.dev>**. If private vulnerability reporting is enabled for the repository, you can also report it on GitHub under **Security > Report a vulnerability**. Please do not create a public issue for the vulnerability.

Your report should include the following information:

- A description of the vulnerability
- Steps to reproduce the vulnerability, ideally with a minimal proof of concept
- Possible impact of the vulnerability
- Any suggested mitigation or remediation steps
- Whether you used AI tools to find, verify, or describe the vulnerability, and which ones

We will respond to your email as soon as possible and work with you to address any security issues.

## AI-Assisted Reports

We accept reports that were found or written with the help of AI tools, as long as a person stands behind them:

- **Disclose** any AI use in your report.
- **Verify** the vulnerability yourself before you report it, ideally with a working proof of concept. Do not send theoretical or speculative findings that you have not confirmed.
- **Be concise.** Remove generic or invented content, and make sure every claim in the report is true.
- **Be ready to answer questions** about the report without relying on an AI tool.
- **Never let an AI agent submit reports on its own.** A person must review every report and send it.

Unverified AI-generated reports take time away from real security issues. We may close them without a detailed review, and repeated low-quality reports may lead to a block.

## AI and Agent Security

AI tools and AI agents create new kinds of security risks. Please report these privately, like any other vulnerability:

- **Prompt injection:** content in issues, pull requests, comments, files, or web pages that can make an AI agent or an AI-powered workflow act against the project or its users.
- **Poisoned instruction files:** malicious or hidden instructions in `AGENTS.md`, other agent instruction files, or templates, including invisible Unicode characters.
- **Excessive agent permissions:** tokens, secrets, or workflow permissions that give AI agents or automations more access than their task needs.
- **Secret exposure:** credentials or private data that could reach AI tools, agent logs, or AI-generated output.
- **Hallucinated dependencies:** references to packages, actions, or URLs that do not exist and could be registered by an attacker.

## Bug Bounty Program

At this time, we do not offer a bug bounty program. If we decide to introduce one in the future, details will be shared here.

## Maintainer Responsibilities

Maintainers are responsible for the security of the project. This includes:

- Responding to security reports in a timely manner
- Investigating reported vulnerabilities
- Developing and releasing patches for confirmed vulnerabilities
- Communicating with the reporting party as the issue is addressed
- Regularly reviewing and auditing the security of the project
- Reviewing changes to agent instruction files and templates as carefully as code, including checking for hidden characters
- Giving AI agents and automations only the permissions they need, and reviewing those permissions regularly
- Keeping details of unpublished vulnerabilities out of AI tools that are not approved for confidential data
- Making the final decision on every security report and fix personally, even when AI tools help with the analysis

## Disclosures

- We will acknowledge receipt of your report within one business day as soon as possible.
- We will confirm the vulnerability and determine its impact.
- We will release a fix as soon as possible, depending on the complexity of the issue.
- We will communicate the vulnerability and any patches or workarounds to our users.

Thank you for your help in making the [community-standards](https://github.com/dileepadev/community-standards) project a more secure place.
