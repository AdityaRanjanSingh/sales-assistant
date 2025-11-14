# Agent App

## Environment Configuration

### Required Environment Variables

The application **requires** `NEXT_PUBLIC_API_URL` to be set in your deployment environment:

```bash
NEXT_PUBLIC_API_URL=https://nuflow.vercel.app
```

**Important:** The application will fail to start if `NEXT_PUBLIC_API_URL` is not set. This prevents accidentally using localhost endpoints in production.

### Optional Environment Variables

These can be configured via environment variables or through the UI:

```bash
NEXT_PUBLIC_ASSISTANT_ID=<your-assistant-id>
NEXT_PUBLIC_LANGSMITH_API_KEY=<your-langsmith-api-key>
```

If not set via environment variables, the application will prompt you to enter them through a configuration form.

### Deployment Setup

When deploying to Vercel, Netlify, or other platforms:

1. Navigate to your project's environment variables settings
2. Add `NEXT_PUBLIC_API_URL=https://nuflow.vercel.app` (required)
3. Optionally add `NEXT_PUBLIC_ASSISTANT_ID` and `NEXT_PUBLIC_LANGSMITH_API_KEY`
4. Set different values for Production and Preview environments if needed
5. Redeploy your application

### Local Development

For local development, create a `.env.local` file in the `apps/web` directory:

```bash
cp .env.example .env.local
# Edit .env.local and set NEXT_PUBLIC_API_URL at minimum
```

# TODO: ADD README
