# Social AI Auto Poster Security

## Secrets
Never commit `.env`, access tokens, OAuth secrets, cookies, or platform credentials.

## Publishing safety
Human approval remains the default. Credentials should be disabled while workflows are being developed or tested.

## AI output
Treat generated captions, hashtags, and metadata as untrusted input. Validate structure and length before sending data to platform APIs.

## Media
Preserve the original media binary and avoid unnecessary transformations that could reduce publishing quality.
