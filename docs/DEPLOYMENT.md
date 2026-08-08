# Deployment

## Current frontend

Build the static Vite application with:

```bash
npm run build
```

Deploy the generated `dist/` directory to a static hosting provider.

## Backend and AI services

When the backend is deployed, configure API and NVIDIA AI credentials through the hosting environment's secret manager. Do not place keys in frontend assets, source code, or client-side environment variables.

Use HTTPS, restrict document storage access, log audit events without sensitive document contents, and retain human review as the final approval stage.
