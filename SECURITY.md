# Security Policy

This document describes the security policy for the Nucian Language repository, a static constructed-language data project with no running application, user accounts, authentication, or external data processing. The policy covers vulnerability reporting, supported versions, and coordinated disclosure expectations.

## 📑 Table of Contents

- [Supported Versions](#-supported-versions)
- [Reporting a Vulnerability](#-reporting-a-vulnerability)
- [Scope](#-scope)
- [Disclosure Policy](#-disclosure-policy)

## 🛡️ Supported Versions

Use this table to indicate which project versions currently receive security maintenance.

| Version | Distribution Channel | Supported |
|---------|--------------------|-----------|
| Latest version | GitHub repository (master branch) | ✅ |
| Preceding versions | Any distribution channel | ❌ |

## 🚨 Reporting a Vulnerability

Please do not disclose suspected vulnerabilities publicly before maintainers have had an opportunity to validate and remediate them.

To report a vulnerability:
- [GitHub Security Advisories](https://github.com/hmlendea/low-nucian-language/security/advisories)
- Contact the maintainers directly

## 📌 Scope

The original maintainers are not responsible for changes, modifications, or security issues introduced by downstream forks.

The subsequent report categories are in scope for this repository:
- Dictionary data integrity (PGDictionary.xml, words.json, sentences.json)
- Validation script behaviour (update-dictionary.sh, format-dic.sh)
- Generated documentation accuracy (docs/DICTIONARY.md)
- CI workflow integrity (.github/workflows/validate.yml)

The subsequent categories are out of scope unless explicitly stated to the contrary:
- Downstream fork modifications
- User-local script executions
- Third-party tooling that consumes the linguistic data
- GitHub platform vulnerabilities

## 📢 Disclosure Policy

This project follows coordinated disclosure:
1. Vulnerabilities are investigated privately.
2. A remediation plan is prepared and validated.
3. Public disclosure is published after a fix, mitigation, or agreed risk decision is available.
4. Credit is attributed in accordance with reporter preference and project policy.