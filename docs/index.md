# Shelly - AI-Powered Development Assistant

Shelly is a multi-purpose AI-powered CLI tool built by [Juspay](https://juspay.io) that combines error analysis, repository organization, and Memory Bank management into a single development workflow.

## Core Features

- **Error Analysis** - AI-powered debugging for failed shell commands across bash, zsh, tcsh, and fish
- **Repository Organization** - Complete project scaffolding with GitHub integration and best practices
- **Memory Bank** - Persistent AI development context for enhanced AI-assisted workflows

## Quick Install

```bash
npm install -g @juspay/shelly
```

## How It Works

Shelly uses a **dual CLI architecture**:

1. **`shelly`** (no arguments) - Analyzes your last failed command using AI
2. **`shelly <command>`** - Repository management tools (`organize`, `memory`, `github`, etc.)

```bash
# After a failed command
$ grp "pattern" file.txt
grp: command not found

$ shelly
Analyzing: "grp pattern file.txt"
Maybe you meant: grep "pattern" file.txt

# Repository organization
$ shelly organize
$ shelly memory init
$ shelly gh --force
```

## Getting Started

- [Quick Start Guide](QUICK_START.md) - Get up and running in minutes
- [Installation](GETTING_STARTED.md) - Detailed installation instructions
- [Setup & Configuration](SETUP.md) - Shell integration and AI provider setup

## Links

- [GitHub Repository](https://github.com/juspay/shelly)
- [NPM Package](https://www.npmjs.com/package/@juspay/shelly)
- [Report Issues](https://github.com/juspay/shelly/issues)
