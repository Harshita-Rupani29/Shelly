# Troubleshooting

## Installation Issues

### "shelly: command not found"

- Verify global installation: `npm list -g @juspay/shelly`
- Ensure npm global bin is in PATH: `export PATH="$(npm bin -g):$PATH"`
- For local development, use: `node dist/main.js`

### node-pty Build Failures

See the detailed [Troubleshooting Guide](../TROUBLESHOOTING.md#node-pty-build-failures) for platform-specific solutions.

## Error Analysis Issues

### "Could not retrieve the last command from history"

- Ensure shell integration is configured (see [Shell Compatibility](../features/shell-integration.md))
- Restart your terminal after adding the alias
- Verify your shell supports `fc` (bash/zsh) or `history` (tcsh)

### "Could not analyze the error with Neurolink"

- Check `GOOGLE_AI_API_KEY` environment variable is set
- Verify internet connectivity
- Try debug mode: `SHELLY_DEBUG=true shelly`

### "shelly cannot analyze itself"

This is expected. Shelly skips analyzing its own invocation. Run another command first, then use `shelly`.

## GitHub Setup Issues

### "GITHUB_TOKEN is not set"

```bash
export GITHUB_TOKEN=your_token_here
```

Required token scopes: `repo`, `admin:repo_hook`, `write:packages`.

### Permission Denied on GitHub API

Ensure your token has the required scopes. For fine-grained tokens, you need repository administration permissions.

## Memory Bank Issues

### "Memory Bank already exists"

Use `--force` to reinitialize:

```bash
shelly memory init --force
```

### AI Content Generation Fails

- Verify AI provider credentials are configured
- Check that `@juspay/neurolink` is properly installed
- Try: `SHELLY_DEBUG=true shelly memory init`

## Debug Mode

Enable detailed logging for any Shelly command:

```bash
SHELLY_DEBUG=true shelly
```

## Getting Help

- [GitHub Issues](https://github.com/juspay/shelly/issues)
- Email: opensource@juspay.in
