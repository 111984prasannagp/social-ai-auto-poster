# Current Project Status

Updated: 2026-10-03

## Final master workflow

A complete Social AI Auto Poster - Free Master n8n workflow has been generated as the final import artifact:

- 69 nodes
- Telegram image/document intake
- Human approval gate
- Instagram + Threads + Facebook publishing adapters
- Free-first AI routing with OmniRoute, OpenRouter, Gemini and NVIDIA
- Groq registered as an extension point but disabled by default because the currently verified Groq vision model pricing is not zero
- AI quality and safety guard
- Duplicate protection
- Telegram commands
- Regeneration
- Editing commands
- Per-platform approval
- Approve All
- Scheduling
- Publishing status
- History and analytics counters
- Emergency STOP / RESUME
- Health endpoint
- Status endpoint
- Public image relay endpoint for Meta APIs
- Automatic HTTP retries
- Instagram media-processing polling
- Configuration designed around placeholders; no live secrets are stored in the workflow artifact

## Phase 1 platforms

- Instagram
- Threads
- Facebook Page

## Future extensions

- YouTube video/Shorts pipeline
- Additional platform adapters
- Multi-account support
- More provider plugins
- Deeper analytics and growth optimization
- More advanced batch/media-group orchestration

## Free-only policy

The master workflow is configured around free/free-tier providers and a cost-guard mindset. Free tiers and model availability can change, so the workflow does not claim any provider is free forever.

## Safety

- Workflow imports inactive by default.
- Human approval is required before publishing.
- Publishing can be stopped with /stop and resumed with /resume.
- Live API credentials are not included in GitHub.
- Platform publishing remains subject to each platform's API permissions and rules.

## Runtime note

The current public image relay uses the configured Cloudflare quick-tunnel URL. Quick-tunnel URLs are temporary; if the URL changes, update the public image URL in the workflow before publishing.

## Repository note

The repository documentation is synchronized with the master design. The downloadable final import artifact is the authoritative generated workflow for this build step.