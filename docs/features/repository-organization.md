# Repository Organization

The `shelly organize` command transforms any project into a publication-ready repository with proper structure, configuration files, and best practices.

## Usage

```bash
# Basic organization
shelly organize

# Force overwrite existing files
shelly organize --force

# Update mode - add missing files, preserve existing
shelly organize --update

# Move misplaced files to correct directories
shelly organize --move

# Target a specific directory
shelly organize --directory /path/to/project
```

## What Gets Generated

The organize command scaffolds:

- **CI/CD** - GitHub Actions workflows for testing, linting, and releases
- **Code Quality** - ESLint, Prettier, commitlint configurations
- **Documentation** - README template, CONTRIBUTING guide, CODE_OF_CONDUCT
- **Git Hooks** - Husky pre-commit and pre-push hooks with lint-staged
- **Project Config** - `.editorconfig`, `.gitignore`, TypeScript config
- **Security** - Security check scripts, dependency audit setup

## Template System

Templates are stored in `src/shelly/templates/` and copied to `dist/` during build. The template engine supports variable substitution for project-specific values like name, description, and license.

## GitHub Integration

Combine with `shelly gh` for complete repository setup:

```bash
export GITHUB_TOKEN=your_token_here

# Complete setup: GitHub config + project scaffolding
shelly setup --force

# Or run separately
shelly gh --force        # GitHub settings only
shelly organize --update # Project files only
```

## Status Check

Verify your repository's organization status:

```bash
shelly status
```

This reports which expected files are present, missing, or need updating.
