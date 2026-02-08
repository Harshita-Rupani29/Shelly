# Current Status

The `memory-bank/current/` directory tracks the active development state.

## Files

### activeContext.md

Tracks current development focus:

- What is being worked on now
- Recent changes and their impact
- Active decisions and open questions
- Blockers or pending items

This is the most frequently updated file and the first thing AI assistants should read.

### progress.md

Tracks overall project progress:

- Completed features and milestones
- In-progress work items
- Upcoming roadmap items
- Known issues

## Updating

These files should be updated most frequently as they reflect the current state:

```bash
# Update current status files
shelly memory update

# Update just progress
shelly memory update --file progress.md

# View current state
shelly memory show current/activeContext.md
shelly memory show current/progress.md
```
