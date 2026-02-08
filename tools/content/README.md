# Content Tools

This directory contains utilities for managing content and media assets.

## Available Tools

### Media Cleanup (`mediaCleanup.js`)

Manages media files and removes unused assets:

- Scans for unused images and videos
- Reports orphaned media files
- Provides safe cleanup options
- Maintains asset inventory

### Content Validator (`contentValidator.js`)

Validates content files and formats:

- Checks markdown syntax
- Validates frontmatter
- Ensures consistent formatting
- Reports content issues

### Asset Optimizer (`assetOptimizer.js`)

Optimizes media assets for production:

- Compresses images
- Generates responsive sizes
- Creates web-optimized formats
- Caches optimization results

## Usage

```bash
# Find unused media
node tools/content/mediaCleanup.js --scan

# Clean up orphaned files
node tools/content/mediaCleanup.js --cleanup

# Validate content
node tools/content/contentValidator.js

# Optimize assets
node tools/content/assetOptimizer.js --optimize
```

## Integration

```json
{
  "scripts": {
    "content:scan": "node tools/content/mediaCleanup.js --scan",
    "content:validate": "node tools/content/contentValidator.js",
    "content:optimize": "node tools/content/assetOptimizer.js"
  }
}
```
