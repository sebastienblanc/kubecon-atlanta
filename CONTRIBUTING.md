# Contributing to kubecon-atlanta

We welcome contributions to this project! This document provides guidelines for contributing.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [How to Contribute](#how-to-contribute)
- [Submitting Issues](#submitting-issues)
- [Submitting Pull Requests](#submitting-pull-requests)
- [Development Guidelines](#development-guidelines)
- [Testing](#testing)
- [Questions](#questions)

## Code of Conduct

By participating in this project, you agree to abide by our Code of Conduct. Please be respectful and inclusive in all interactions.

## Getting Started

1. Fork the repository on GitHub
2. Clone your fork locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/kubecon-atlanta.git
   cd kubecon-atlanta
   ```
3. Create a new branch for your changes:
   ```bash
   git checkout -b feature/your-feature-name
   ```

## How to Contribute

There are many ways to contribute to this project:

- Report bugs
- Suggest new features
- Improve documentation
- Submit code changes
- Review pull requests

## Submitting Issues

When submitting an issue, please:

1. Check if the issue already exists
2. Use a clear and descriptive title
3. Provide detailed information about:
   - What you expected to happen
   - What actually happened
   - Steps to reproduce the issue
   - Your environment (OS, Kubernetes version, etc.)

## Submitting Pull Requests

1. Ensure your code follows the project's coding standards
2. Include tests for new functionality
3. Update documentation as needed
4. Write clear commit messages
5. Reference any related issues in your PR description

### Pull Request Process

1. Fork the repository and create your branch from `main`
2. Make your changes
3. Test your changes thoroughly
4. Commit your changes with descriptive messages
5. Push to your fork and submit a pull request
6. Respond to any feedback during the review process

## Development Guidelines

### Kubernetes Manifests

- Follow Kubernetes best practices for YAML formatting
- Use proper indentation (2 spaces)
- Include appropriate labels and annotations
- Validate manifests using `kubectl --dry-run=client`

### Documentation

- Keep documentation up to date
- Use clear and concise language
- Include examples where helpful
- Follow Markdown formatting guidelines

### Commit Messages

- Use clear and descriptive commit messages
- Follow the format: `type: brief description`
- Types include: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

Example:
```
feat: add new custom resource definition for validation
docs: update README with installation instructions
fix: correct validation webhook configuration
```

## Testing

Before submitting a pull request:

1. Test your Kubernetes manifests:
   ```bash
   kubectl --dry-run=client -f manifests/
   ```

2. Validate YAML syntax:
   ```bash
   yamllint manifests/
   ```

3. Test in a local Kubernetes cluster if possible

## Questions

If you have questions about contributing, please:

1. Check existing issues and discussions
2. Open a new issue with the `question` label
3. Reach out to the maintainers

Thank you for contributing to kubecon-atlanta!