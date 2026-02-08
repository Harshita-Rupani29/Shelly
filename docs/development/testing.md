# Testing

## Test Runner

Shelly uses the Node.js built-in test runner (`node --test`).

## Running Tests

```bash
# Build and run all tests
npm test

# Watch mode (rebuild + rerun on changes)
npm run test:watch
```

## Test Location

- Source: `src/tests/*.test.ts`
- Compiled: `dist/tests/*.test.js`
- Tests are excluded from the main TypeScript compilation and must be built before running

## Writing Tests

Tests use Node.js built-in `node:test` and `node:assert`:

```typescript
import { describe, it } from 'node:test';
import assert from 'node:assert';

describe('myFunction', () => {
  it('should do something', () => {
    assert.strictEqual(myFunction(), expected);
  });
});
```

## Build Validation

Before pushing, the pre-push hook runs:

```bash
# Type checking
npx tsc --noEmit

# Full test suite
npm test

# Build validations (if script exists)
node scripts/build-validations.cjs
```

## CI/CD

Tests run automatically in GitHub Actions on push and pull request events. The workflow:

1. Installs dependencies
2. Runs linting (`npm run lint`)
3. Checks formatting (`npm run format:check`)
4. Builds the project (`npm run build`)
5. Runs tests (`npm test`)
