# Contributing to Cursor Project Rules

Thank you for considering contributing to Cursor Project Rules! This document provides guidelines and instructions for contributing to this project.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Adding or Updating Rules](#adding-or-updating-rules)
  - [First-time Contributors](#first-time-contributors)
- [Style Guides](#style-guides)
  - [Markdown Style Guide](#markdown-style-guide)
  - [Rule Format Guidelines](#rule-format-guidelines)
- [Development Process](#development-process)
  - [Local Development](#local-development)
  - [Pull Request Process](#pull-request-process)

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

If you find issues with any of the documentation rules or their implementation:

1. Check if the issue already exists in the [Issues](https://github.com/yourusername/cursor-project-rules/issues) section
2. If not, create a new issue using the bug report template
3. Provide a clear description, steps to reproduce, and expected behavior

### Suggesting Enhancements

Have ideas for making the rules better?

1. Check if your suggestion already exists in the [Issues](https://github.com/yourusername/cursor-project-rules/issues) section
2. If not, create a new issue using the feature request template
3. Clearly describe your suggestion and how it would improve the project

### Adding or Updating Rules

To add new documentation rules or update existing ones:

1. Fork the repository
2. Create a new branch (`git checkout -b new-rule/your-rule-name`)
3. Add your rule file in the `.cursor/rules` directory using the `.mdc` extension
4. Follow the [Rule Format Guidelines](#rule-format-guidelines)
5. Submit a pull request

#### Rule Naming Conventions

- For general framework documentation: `framework-name.mdc` (e.g., `nextjs.mdc`)
- For numbered sequence of related docs: `##-name.mdc` (e.g., `01-openai.mdc`, `02-anthropic.mdc`)
- For usage-specific documentation: `name-usage.mdc` (e.g., `shadcn-usage.mdc`)

### First-time Contributors

New to contributing? Look for issues tagged with `good first issue` - these are simpler tasks perfect for those making their first contribution.

## Style Guides

### Markdown Style Guide

- Use Markdown formatting consistently
- Include code blocks with appropriate language tags (`js, `tsx, etc.)
- Use headers for organization (# for title, ## for sections)
- Use lists and tables for easy scanning
- Include examples where helpful

### Rule Format Guidelines

Each rule file should:

1. Begin with a clear title: `# Title of Documentation`
2. Include a brief description of what the rule covers
3. Organize content with clear section headers
4. Use code examples where appropriate
5. Focus on practical usage rather than theory
6. Keep file size reasonable (1-25KB is ideal)

Example structure:

```markdown
# Framework Name Documentation

A brief description of the framework and its purpose.

## Installation

How to install the framework.

## Basic Usage

Code examples and explanation of basic usage.

## Advanced Techniques

More complex patterns and examples.
```

## Development Process

### Local Development

1. Clone your fork: `git clone https://github.com/your-username/cursor-project-rules.git`
2. Create a branch for your work: `git checkout -b your-feature-branch`
3. Make your changes
4. Test your rules in a Cursor project by copying them to the `.cursor/rules` directory
5. Commit with meaningful messages: `git commit -m "Add documentation for XYZ framework"`

### Pull Request Process

1. Push your changes to your fork: `git push origin your-feature-branch`
2. Create a Pull Request against the main repository
3. Fill out the PR template completely
4. Request review from maintainers
5. Address any feedback from code reviews
6. Once approved, a maintainer will merge your PR

Thank you for helping improve Cursor Project Rules!
