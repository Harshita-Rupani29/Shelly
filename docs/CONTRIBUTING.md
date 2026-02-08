# Contributing

For the full contributing guide, see the [CONTRIBUTING.md](https://github.com/juspay/shelly/blob/release/CONTRIBUTING.md) in the repository root.

## Quick Start

1. Fork the repository
2. Clone your fork: `git clone https://github.com/your-username/shelly.git`
3. Install dependencies: `npm install`
4. Create a branch: `git checkout -b feature/your-feature`
5. Make changes and test: `npm test`
6. Push and create a PR

## Development Commands

```bash
npm run build        # Compile TypeScript
npm test             # Build and run tests
npm run lint         # Run ESLint
npm run format       # Format with Prettier
npm start            # Build and run CLI
```

## Commit Messages

Use [Conventional Commits](https://www.conventionalcommits.org/):

```
feat(auth): add OAuth2 authentication flow
fix(api): resolve null pointer in user service
docs(readme): update installation instructions
```

## Architecture

See the [Architecture Guide](development/architecture.md) for an overview of Shelly's dual CLI architecture and service layer.
