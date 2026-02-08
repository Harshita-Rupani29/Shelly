# Automation Tools

This directory contains automation scripts for build, deployment, and development workflows.

## Available Tools

### Build System (`buildSystem.js`)

A comprehensive build automation tool that orchestrates the entire build process:

- **Pre-build validation**: Ensures all prerequisites are met
- **Dependency checks**: Verifies required dependencies are installed
- **TypeScript compilation**: Compiles TypeScript to JavaScript
- **Asset processing**: Handles static assets and templates
- **Post-build verification**: Validates the build output

### Package Enhancer (`packageEnhancer.js`)

Enhances package.json with consistent configurations:

- Validates required fields
- Adds missing scripts
- Ensures consistent formatting
- Updates version information

### Environment Manager (`environmentManager.js`)

Safe environment variable management:

- Validates .env files against .env.example
- Detects missing required variables
- Supports multiple environments (development, staging, production)
- Provides secure defaults

## Usage

```bash
# Run build system
node tools/automation/buildSystem.js

# Enhance package.json
node tools/automation/packageEnhancer.js

# Validate environment
node tools/automation/environmentManager.js
```

## Integration

These tools are designed to be integrated into CI/CD pipelines and npm scripts:

```json
{
  "scripts": {
    "build:full": "node tools/automation/buildSystem.js",
    "env:validate": "node tools/automation/environmentManager.js"
  }
}
```
