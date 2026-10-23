# Security Policy

Vivédex aims to make biodiversity knowledge more accessible while protecting contributors, research data, and the systems that support the project.

## Reporting a Vulnerability

**Please do not report security vulnerabilities in public GitHub issues, discussions, pull requests, or social media.** Public reports can expose users or project infrastructure before a fix is available.

Use GitHub's **private vulnerability reporting** feature from the repository's **Security** tab and select **Report a vulnerability**, if it is enabled.

If private vulnerability reporting is not available, contact the repository maintainers privately using a contact method listed on the repository owner's GitHub profile. Include **Vivédex security report** in the subject. Do not include real personal data, credentials, or sensitive wildlife coordinates in a public message.

When reporting, please include, where possible:

- A clear description of the potential vulnerability and its impact.
- The affected version, commit, component, or endpoint.
- Steps to reproduce the issue, with a minimal proof of concept where safe.
- Any suggested mitigation.

Please make a good-faith effort to avoid accessing, changing, deleting, or disclosing data that does not belong to you. Do not perform destructive tests, denial-of-service tests, or social engineering against project contributors or infrastructure.

## What to Report

Examples include:

- Authentication or authorization bypasses, or unintended access to private observations or accounts.
- Exposure of API keys, credentials, tokens, private configuration, or internal data.
- Unsafe image, audio, document, or other file uploads and processing.
- Injection, remote-code-execution, or dependency-supply-chain issues.
- Server-side request forgery, insecure API endpoints, or other exploitable application flaws.
- Vulnerabilities in AI-assisted workflows that cause private data to be disclosed or unsafe actions to occur.
- Exposure of sensitive species records, precise locations, contributor details, or other data that should be restricted.

For ordinary bugs, incorrect species identifications, data-quality concerns, and feature requests, use the normal GitHub issue process instead. Do not include sensitive location data in a public issue.

## Response and Disclosure

The maintainers will make a reasonable effort to acknowledge a private report, assess its impact, and communicate next steps. Response times may vary while Vivédex is an early-stage project maintained with limited resources.

Please allow maintainers reasonable time to investigate and prepare a fix before disclosing a vulnerability publicly. We will aim to coordinate disclosure with the reporter and affected upstream projects where appropriate. There is no guarantee of a particular response or resolution time.

## Supported Versions

Vivédex is currently in early development. Unless a release explicitly states otherwise, only the latest version on the default branch is considered for security fixes. Older commits, experimental branches, forks, and third-party deployments may not receive fixes or support.

## Scope and Third-Party Services

This policy covers security issues in code and infrastructure maintained by the Vivédex project. Services, datasets, libraries, model APIs, and other components maintained by third parties may have their own reporting processes; report issues to the relevant provider when appropriate, and notify Vivédex privately if the issue also affects this project.

Do not upload confidential, personal, or otherwise sensitive data to a development instance unless that instance explicitly states that it is suitable for such data. Species-identification results are suggestions, not authoritative scientific determinations.

## Safe Harbor

Vivédex welcomes good-faith security research that follows this policy. We will not seek to penalize or bring legal action against researchers for accidental, good-faith violations of this policy. This safe-harbor statement does not authorize access to data, systems, or accounts without permission, and it does not bind third-party service providers.

## Before Public Launch

Repository maintainers should enable GitHub private vulnerability reporting or publish a monitored private security contact method. Do not consider this reporting channel operational until one of those options has been verified.
