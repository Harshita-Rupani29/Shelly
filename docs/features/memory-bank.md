# Memory Bank

The Memory Bank provides persistent AI development context, enabling AI assistants to understand your project across sessions.

## Overview

Memory Bank creates structured documentation in a `memory-bank/` directory that AI tools (like Cline) can read for project context. This eliminates the need to re-explain your project to AI assistants every session.

## Usage

```bash
# Initialize Memory Bank
shelly memory init

# Force reinitialize (overwrites existing)
shelly memory init --force

# Update all Memory Bank files
shelly memory update

# Update a specific file
shelly memory update --file progress.md

# Check Memory Bank status
shelly memory status

# List all Memory Bank files
shelly memory list

# Display a specific file
shelly memory show projectbrief.md
shelly memory show current/activeContext.md
```

## File Structure

```
memory-bank/
├── README.md                    # Memory Bank overview
├── project/                     # Project Definition & Strategy
│   ├── projectbrief.md         # Mission, goals, scope
│   └── productContext.md       # Problem statement, solution overview
├── technical/                   # Technical Architecture & Implementation
│   ├── systemPatterns.md       # Architecture patterns, design decisions
│   └── techContext.md          # Technology stack, setup, dependencies
└── current/                     # Active Development State
    ├── activeContext.md        # Current work focus, recent changes
    └── progress.md             # Status, completed features, roadmap
```

## AI Content Generation

Memory Bank content is generated using Neurolink (Google Vertex AI). The AI analyzes your project's `package.json`, source structure, and existing documentation to produce accurate, contextual documentation.

## Integration with AI Assistants

Memory Bank generates a `.clinerules` file that Cline and other AI assistants read automatically. This provides persistent context about:

- Project architecture and patterns
- Current development focus
- Technical decisions and constraints
- Active tasks and progress
