# Contributing Guide

Thank you for your interest in contributing to minimax-usage. This document walks you through the complete workflow, from preparing your development environment to opening a Pull Request. Please read it in full before you begin, so that your contribution can move through review and merge smoothly.

## About the Project

minimax-usage is a Claude Code plugin that displays the remaining usage of your MiniMax subscription in the Claude Code HUD status bar. The project is written in TypeScript and ships as a JavaScript bundle that runs on Node.js 18+.

A Chinese version of this guide is available in [CONTRIBUTING.zh.md](./CONTRIBUTING.zh.md).

## Code of Conduct

All interactions in this project are expected to remain professional and welcoming. We expect every contributor to:

- Use welcoming and inclusive language
- Respect differing viewpoints and experiences
- Accept constructive criticism gracefully
- Focus on what is best for the project

If you experience or witness inappropriate behavior, please contact the project maintainers.

## Submitting Issues

Before opening an Issue, please search the existing list to confirm that the topic has not already been reported. Two templates are available:

- **Bug Report** — for unexpected behavior
- **Feature Request** — for new features or improvements

Please fill in the requested fields as completely as possible so that maintainers can investigate efficiently.

## Development Environment

### Requirements

- Node.js 18 or newer
- npm 9 or newer
- A working Claude Code installation (for local debugging)

### Clone and Install

```bash
git clone https://github.com/PureLo/minimax-usage.git
cd minimax-usage
npm install
```

### Local Build

```bash
npm run build
```

### Watch Mode

```bash
npm run dev
```

This starts the TypeScript compiler in watch mode so that you can see the effect of your changes immediately.

## Coding Standards

- Follow the existing code style and directory structure
- Add TSDoc comments to public functions and exported types
- Make sure `npm run build` passes locally before pushing, with no new TypeScript errors
- Avoid adding new runtime dependencies; if a new dependency is required, justify it in the PR description
- Keep Pull Requests focused; one PR should solve a single problem

## Commit Messages

This project follows the [Conventional Commits](https://www.conventionalcommits.org/) specification:

```
<type>(<optional scope>): <short description>

<optional body>

<optional footer>
```

Common types:

| Type | Purpose |
| --- | --- |
| feat | A new feature |
| fix | A bug fix |
| docs | Documentation only changes |
| style | Changes that do not affect the meaning of the code |
| refactor | A code change that neither fixes a bug nor adds a feature |
| test | Adding missing tests or correcting existing tests |
| chore | Changes to the build process or auxiliary tools and dependencies |

## Pull Request Workflow

1. Fork the repository and create a feature branch off `main`. Suggested naming: `feat/xxx`, `fix/xxx`, or `docs/xxx`
2. Follow the commit message convention above
3. Make sure `npm run build` still passes locally before opening the Pull Request
4. Push to your fork and open a Pull Request against `PureLo/minimax-usage` `main`
5. **Before/after screenshots are required in the Pull Request description.** Because the core deliverable of this plugin is the visual output of the status bar, screenshots are the most direct and reliable evidence for reviewers
6. Your Pull Request will be merged once CI is green, CodeRabbit's suggestions have been addressed, and at least one maintainer has approved

### Screenshot Requirements

The plugin runs in a terminal, so please use your OS screenshot tool to capture the terminal area that contains the Claude Code status bar. The Pull Request description must include:

- **Before** — a screenshot showing the original state or the bug being fixed
- **After** — a screenshot showing the result of your change
- A short description of the difference, with the corresponding text output when relevant

If your change is purely non-visual (for example, configuration parsing, cache strategy, or error handling), please state that explicitly in the PR description and attach relevant test output or logs. Pull Requests limited to documentation updates or `chore`-style changes are exempt from the screenshot requirement.

## Versioning and Releases

Version numbers follow [Semantic Versioning](https://semver.org/). Maintainers bump the version and publish a new release manually, so contributors do not need to edit `version` in `package.json`.

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## Contact

If you have questions, please leave a comment on the relevant Issue or Pull Request, or reach the maintainers through the contact information on the project page.
