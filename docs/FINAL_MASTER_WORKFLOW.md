# Final Master Workflow

## What this workflow contains

The final master workflow is designed as one local n8n workflow with these feature groups:

### Intake and control
- Telegram photo/document trigger
- Original-file handling
- Duplicate protection
- Batch-friendly independent draft queue
- Telegram command center
- Human approval
- Approve All
- Per-platform approval
- Edit and regenerate commands
- Emergency STOP / RESUME

### AI engine
- OmniRoute
- OpenRouter free router
- Gemini free-tier path
- NVIDIA free endpoint
- Provider failover
- JSON parsing
- Capability-aware vision input
- Quality guard
- Safety guard
- Brand-voice baseline
- Platform-specific content
- Hashtag generation
- Caption variants
- AI provider metadata

### Publishing
- Instagram
- Threads
- Facebook Page
- Automatic HTTP retries
- Instagram container status polling
- Publishing result reporting
- Platform toggles

### Management
- Scheduling
- History
- Analytics counters
- Status endpoint
- Health endpoint
- Telegram reports
- Public image relay for Meta APIs

## Important configuration

Before activating the workflow, replace these placeholders:

- REPLACE_WITH_OMNIROUTE_API_KEY
- REPLACE_WITH_OPENROUTER_API_KEY
- REPLACE_WITH_GEMINI_API_KEY
- REPLACE_WITH_NVIDIA_API_KEY
- REPLACE_WITH_INSTAGRAM_ACCESS_TOKEN
- REPLACE_WITH_THREADS_ACCESS_TOKEN
- REPLACE_WITH_FACEBOOK_PAGE_ACCESS_TOKEN

Also verify:

- Instagram user ID
- Threads user ID
- Facebook Page ID
- Current Cloudflare public HTTPS URL

## Safety

The workflow is inactive by default. Do not activate it until each configured provider and publishing API has been tested. Never commit real tokens to GitHub.

## Current scope

X and Reddit are not part of the current Phase 1 publishing path. YouTube is reserved for the later video/Shorts pipeline.

## Runtime assumption

n8n is local/Docker-based, OmniRoute is reachable from the n8n container through host.docker.internal, and the public image relay is reachable over HTTPS by Meta.