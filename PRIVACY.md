# Privacy and Personal Data

This document describes how the Nucian Language repository manages personal data. The repository is a static constructed-language data project with no running application, user accounts, authentication, telemetry, or external data processing. Personal data is limited to Git metadata (commit authorship) and GitHub interaction records (issues, pull requests, discussions).

## 📑 Table of Contents

- [What This Document Covers](#-what-this-document-covers)
- [Self-Hosted Deployments](#-self-hosted-deployments)
- [Data We Handle](#-data-we-handle)
- [Processing and Use](#-processing-and-use)
- [Storage, Retention, and Deletion](#-storage-retention-and-deletion)
- [External Processing and Integrations](#-external-processing-and-integrations)
- [Document Changes](#-document-changes)
- [Contact](#-contact)

## 🔎 What This Document Covers

This document describes how the Nucian Language repository at https://github.com/hmlendea/low-nucian-language manages personal data. It covers the repository conduct and verified integrations described below. The repository is a static data project; there is no deployed application or service operated by the maintainers.

## 🏠 Self-Hosted Deployments

This repository contains only static data files (XML dictionary, JSON validation assets, shell scripts, generated Markdown) and documentation. There is no application to deploy or operate. Users who fork or clone the repository receive only the linguistic data and tooling; no personal data is transmitted to the project maintainers or any external service by the repository contents themselves.

## 📥 Data We Handle

### Data Provided to the Application

No personal data is requested, collected, or stored by the repository contents. Contributors may voluntarily include attribution or etymology notes in dictionary entries (e.g., "From: Romanian (genunchi)"), but these are linguistic metadata, not personal data.

### Data Generated or Collected by the Application

The repository itself generates no personal data. Git records commit authorship (name, email, timestamp) and GitHub records issue/PR/discussion authorship. These are governed by GitHub's privacy policy, not by this repository.

### Data Received from Integrations

No personal data is received from integrations or third parties. The CI workflow uses `hmlendea/polyglot-language-validate@v1.0.0` which validates only the repository's dictionary and validation files; it does not transmit personal data.

## 🧭 Processing and Use

The repository processes only linguistic data for these verified functions:
- Dictionary maintenance — lexical entries, parts of speech, definitions, etymology notes
- Validation — word inflection vectors and sentence corpus alignment
- Documentation generation — Markdown dictionary rendering from XML

No personal data is processed.

## 🗄️ Storage, Retention, and Deletion

Linguistic data is stored in the Git repository as plain-text files (`PGDictionary.xml`, `words.json`, `sentences.json`, `docs/DICTIONARY.md`). Git history retains all committed versions indefinitely. Contributors control their local clones; the project maintainers control the canonical repository on GitHub. GitHub's data retention policies apply to the hosted repository.

## 🔗 External Processing and Integrations

| Service or integration | Purpose | Data involved | Configuration or documentation |
|-----------------------|---------|---------------|--------------------------------|
| GitHub Actions | Continuous validation of dictionary structure and consistency | `PGDictionary.xml`, `words.json`, `sentences.json` (linguistic data only) | `.github/workflows/validate.yml` |
| `hmlendea/polyglot-language-validate@v1.0.0` | Validates PolyGlot XML schema adherence, referential integrity, inflection and sentence alignment | Linguistic data files only | GitHub Marketplace listing |

No other external services process data from this repository.

## 🛡️ Data Protection and Security

The repository contains no secrets, credentials, or personal data. Linguistic data is public. Contributors should not commit personal data in dictionary entries or validation assets. The original maintainers are not responsible for changes, modifications, or privacy issues introduced by downstream forks.

## 🔄 Document Changes

Update this document when repository data processes, storage, integrations, or deployment responsibilities change. The current version is published at `PRIVACY.md` in the repository root.

## 📬 Contact

For questions about repository data handling, contact the project maintainers via GitHub issues or the repository's listed contact channels. Do not send passwords, access tokens, or other secrets.