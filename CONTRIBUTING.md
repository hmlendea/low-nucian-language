# Contributing to Nucian Language

This document covers the guidelines and processes for contributing to this project, including how to report issues, suggest enhancements, submit code changes, and follow project standards.

## 📑 Table of Contents

- [Contributing](#-contributing)
  - [Reporting Issues](#reporting-issues)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Code Contributions](#code-contributions)
    - [Prerequisites](#prerequisites)
    - [Development Setup](#development-setup)
    - [Making Changes](#making-changes)
    - [Pull Request Guidelines](#pull-request-guidelines)
  - [Code Style](#code-style)
  - [Testing](#testing)
  - [Documentation](#documentation)
- [License](#-license)
- [Recognition](#-recognition)
- [Getting Assistance](#-getting-assistance)

## 🤝 Contributing

### Reporting Issues

- Search existing issues first.
- Use the issue templates if available.
- Provide clear reproduction steps.
- Include environment details.

### Suggesting Enhancements

- Check the existing discussions.
- Explain the use case and expected conduct.
- Consider the implementation complexity.

### Code Contributions

#### Prerequisites

- Bash shell
- xmlstarlet
- xmllint

#### Development Setup

```bash
# Clone the repository
git clone https://github.com/hmlendea/low-nucian-language.git
cd low-nucian-language

# Install dependencies
sudo apt-get update && sudo apt-get install -y xmlstarlet libxml2-utils
```

#### Making Changes

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Make your changes.
4. Run tests: `bash ./update-dictionary.sh && bash ./format-dic.sh`
5. Run linters: `shellcheck update-dictionary.sh format-dic.sh`
6. Commit with clear and descriptive messages.
7. Push to your fork.
8. Open a Pull Request.

#### Pull Request Guidelines

- Target the `master` branch.
- Keep PRs focused and atomic.
- Revise documentation if applicable.
- Include tests for any new functionality.
- Ensure the CI checks pass.

### Code Style

Follow the project's coding standards:
- Use `set -euo pipefail` at the top of every non-interactive script
- Use `[[ ]]` over `[ ]` for all conditional tests
- Use `$(command)` for command substitution; never use backticks
- Constant strings must use single quotes; strings with variables must use double quotes
- Variables inside functions must be declared with `local` whenever possible
- Declare constants with `readonly`
- Function naming: all lowercase, words separated by underscores
- Variable naming: all uppercase, always referenced with surrounding curly braces
- Run `shellcheck update-dictionary.sh format-dic.sh` before committing

### Testing

```bash
# Run all tests
bash ./update-dictionary.sh && bash ./format-dic.sh

# Run specific validation
bash ./update-dictionary.sh
```

### Documentation

- Revise relevant docs for changes.
- Follow the documentation style guide.
- Preview changes locally if possible.

## 📜 Code of Conduct

This project follows the [Code of Conduct](./CODE_OF_CONDUCT.md).

## 🔒 Security

Report security vulnerabilities per the [Security Policy](./SECURITY.md).

## 📄 License

By contributing, you agree that your contributions will be licensed under the GNU General Public License v3.0 or later.

## 🙏 Recognition

Contributors are recognized in the GitHub contributors list.

## ❓ Getting Assistance

- Open an issue on GitHub
- Check existing discussions and documentation first.