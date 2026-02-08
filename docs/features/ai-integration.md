# AI Integration

Shelly uses AI across all its features through the `@juspay/neurolink` package, which provides a unified interface to Google Vertex AI and Google AI services.

## Providers

### Google AI API (Free)

Best for individual developers and getting started:

```bash
export GOOGLE_AI_API_KEY="your-api-key-here"
```

Get your API key from [Google AI Studio](https://aistudio.google.com/app/apikey).

### Google Cloud Vertex AI (Enterprise)

For teams and production use with full Neurolink integration:

```bash
export GOOGLE_CLOUD_PROJECT="your-project-id"
export GOOGLE_CLOUD_REGION="us-east5"
export GOOGLE_APPLICATION_CREDENTIALS="/path/to/service-account.json"
```

## How AI Is Used

### Error Analysis

When you run `shelly` after a failed command, the AI:

1. Receives the failed command, error output, and recent history
2. Identifies the root cause of the failure
3. Suggests the corrected command
4. Provides an explanation of what went wrong

### Memory Bank Generation

The AI analyzes your project structure to generate:

- Project briefs and product context
- System architecture patterns
- Technical documentation
- Active development context

### Content Generation

The `AIContentGenerator` class (`src/shelly/utils/aiContentGenerator.ts`) handles:

- README generation from repository analysis
- CONTRIBUTING guide generation
- Memory Bank content creation

## Neurolink Package

All AI operations go through `@juspay/neurolink`, which provides:

- Multi-provider support (Google AI, Vertex AI)
- Automatic fallback between providers
- Consistent API across different AI services
- Token management and rate limiting
