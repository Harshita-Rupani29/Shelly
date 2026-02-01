# Testing Tools

This directory contains testing utilities and automation scripts.

## Available Tools

### Adaptive Test Runner (`adaptiveTestRunner.js`)

Smart test selection based on changed files:

- Analyzes git diff to identify changed files
- Maps changes to relevant test files
- Runs only affected tests for faster feedback
- Falls back to full suite when needed

### Performance Monitor (`performanceMonitor.js`)

Benchmarking and performance tracking:

- Measures execution time of functions
- Tracks memory usage patterns
- Generates performance reports
- Compares against baselines

### Test Fixtures Generator (`fixturesGenerator.js`)

Generates test data and fixtures:

- Creates mock data based on schemas
- Maintains consistency across tests
- Supports various data formats (JSON, CSV, etc.)

## Usage

```bash
# Run adaptive tests
node tools/testing/adaptiveTestRunner.js

# Run performance benchmarks
node tools/testing/performanceMonitor.js

# Generate test fixtures
node tools/testing/fixturesGenerator.js
```

## Integration

```json
{
  "scripts": {
    "test:smart": "node tools/testing/adaptiveTestRunner.js",
    "test:perf": "node tools/testing/performanceMonitor.js"
  }
}
```
