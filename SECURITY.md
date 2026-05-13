# Security Policy

## Supported Versions

We release patches for security vulnerabilities for the following versions:

| Version | Supported          |
| ------- | ------------------ |
| 1.0.x   | :white_check_mark: |

## Reporting a Vulnerability

If you discover a security vulnerability, please follow these steps:

1. **Do NOT** open a public issue
2. Email the maintainer directly or use GitHub's private vulnerability reporting
3. Provide a detailed description of the vulnerability
4. Include steps to reproduce if applicable

We will respond within 72 hours and work with you to address the issue promptly.

## Security Best Practices

When using this meta-prompt generator:

- Never include sensitive data (API keys, passwords, personal information) in prompts
- Be cautious with proxy variables in compliance/legal domains (see C2 validation)
- Review generated prompts for potential injection vulnerabilities
- Sanitize user inputs before processing (see built-in input sanitization)
- Use the Council deliberation for security-critical prompts

## Prompt Injection Prevention

The Promptor v3.1 includes built-in sanitization that checks for instruction injection patterns.
However, always validate generated prompts before deploying them in production systems.
