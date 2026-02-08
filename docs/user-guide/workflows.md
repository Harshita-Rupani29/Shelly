# Common Workflows

## New Project Setup

```bash
mkdir my-project && cd my-project
npm init -y
git init
git remote add origin https://github.com/username/my-project.git

# Complete setup (GitHub + organize + memory)
export GITHUB_TOKEN=your_token_here
shelly setup --force
shelly memory init

# Verify
shelly status
```

## Existing Project Enhancement

```bash
cd existing-project

# Add missing project files without overwriting
shelly organize --update

# Initialize AI context
shelly memory init

# Add GitHub best practices
export GITHUB_TOKEN=your_token_here
shelly gh --dry-run  # Preview changes
shelly gh --force    # Apply

# Move misplaced files (optional)
shelly organize --move
```

## Daily Development

```bash
# After any failed command
some-failed-command
shelly  # Get AI analysis

# Update project context regularly
shelly memory update

# Check repository health
shelly status
```

## Publishing-Ready Repository

```bash
cd your-repository
export GITHUB_TOKEN=your_token_here

# Full transformation
shelly setup --force   # GitHub setup + organize
shelly memory init     # AI context

# Result:
# - Branch protection rules
# - GitHub Pages setup
# - NPM publishing guidance
# - Complete project structure
# - AI-assisted development context
```

## GitHub-Only Setup

```bash
# Configure GitHub without touching project files
shelly setup --github-only

# Or use the shortcut
shelly gh --force
```

## Organization-Only Setup

```bash
# Scaffold project files without GitHub changes
shelly setup --organize-only

# Or directly
shelly organize --update
```
