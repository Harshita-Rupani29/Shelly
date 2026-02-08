# Memory Bank Overview

The Memory Bank is Shelly's persistent AI context management system. It creates structured documentation that AI assistants can read to understand your project across development sessions.

## Purpose

AI assistants lose context between sessions. Memory Bank solves this by maintaining a structured set of files that describe your project's architecture, current state, and development focus.

## Structure

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

## Quick Start

```bash
# Initialize
shelly memory init

# Check status
shelly memory status

# Update after changes
shelly memory update
```

## Integration

Memory Bank generates a `.clinerules` file for automatic integration with Cline and other AI development assistants. The context is loaded automatically when the AI assistant starts a session.

## Sections

- [Project Context](project.md) - Project definition files
- [Technical Docs](technical.md) - Architecture and technology documentation
- [Current Status](current.md) - Active development state
