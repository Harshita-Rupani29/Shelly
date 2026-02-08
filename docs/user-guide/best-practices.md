# Best Practices

## Repository Organization

- **Use `--update` mode** for existing projects to preserve your customizations
- **Run `shelly status`** after organizing to verify completeness
- **Commit generated files** to version control so your team benefits from the scaffolding

## Memory Bank

- **Initialize early** - Set up Memory Bank when starting a new project
- **Update regularly** - Run `shelly memory update` when significant changes occur
- **Review generated content** - AI-generated docs may need project-specific adjustments
- **Keep `activeContext.md` current** - This is what AI assistants read first

## GitHub Setup

- **Preview first** - Use `shelly gh --dry-run` before applying changes
- **Use `--force` for automation** - Skip prompts in CI/CD with `shelly setup --force`
- **Protect your release branch** - The GitHub setup configures branch protection automatically

## Error Analysis

- **Source the alias once** - Add it to your shell config file, not to each session
- **Don't pass commands as arguments** - Just run `shelly` with no arguments after a failure
- **Use debug mode** when troubleshooting: `SHELLY_DEBUG=true shelly`

## Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/) format:

```
type(scope): description
```

Valid types: `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `chore`

## Single Commit Per Branch

Shelly enforces a single commit per feature branch policy:

- Each branch should contain exactly one commit
- Use `git rebase -i` to squash multiple commits
- Merge commits are not allowed in feature branches
- Use `git push --force-with-lease` after squashing
