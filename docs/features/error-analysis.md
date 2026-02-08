# Error Analysis

Shelly's error analysis mode provides AI-powered debugging for failed shell commands. Run `shelly` with no arguments after any failed command to get intelligent suggestions.

## How It Works

1. Shelly captures your last command from shell history using the `fc` command (bash/zsh) or `history` (tcsh)
2. The command and error output are sent to Neurolink (Google Vertex AI) for analysis
3. AI provides a diagnosis, correction suggestions, and explanations

## Usage

```bash
# Run a command that fails
$ git psuh origin main
git: 'psuh' is not a git command.

# Analyze with Shelly
$ shelly
Analyzing previous command: "git psuh origin main"
Maybe you meant: git push origin main
```

## Shell Integration

Shelly requires a shell alias to access real-time command history:

=== "Bash"

    ```bash
    echo 'eval "$(shelly --alias)"' >> ~/.bashrc
    source ~/.bashrc
    ```

=== "Zsh"

    ```bash
    echo 'eval "$(shelly --alias)"' >> ~/.zshrc
    source ~/.zshrc
    ```

=== "Tcsh"

    ```bash
    echo 'alias shelly "node /path/to/shelly/src/main.js"' >> ~/.tcshrc
    source ~/.tcshrc
    ```

## Pattern-Based Corrections

Before calling AI, Shelly checks built-in correction rules in `src/rules/` for common mistakes:

- Typo corrections (`gti` -> `git`, `grp` -> `grep`)
- Common flag mistakes
- Missing arguments

## Debug Mode

Enable verbose output for troubleshooting:

```bash
SHELLY_DEBUG=true shelly
```

## Architecture

The error analysis pipeline flows through these services:

- `services/historyService.ts` - Shell history retrieval
- `services/commandService.ts` - Command execution
- `services/analysisService.ts` - AI error analysis via Neurolink
- `services/shellService.ts` - Multi-shell support (bash, zsh, tcsh)
- `rules/` - Pattern-based command correction rules
