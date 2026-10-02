# Build Plan

## Phase 1 — Foundation
- Local n8n
- Telegram bot
- Ollama
- Vision model
- JSON output contract
- Safe-mode approval

## Phase 2 — Content generation
- Analyze image
- Detect topic and useful context
- Generate clear, attractive, non-spammy platform-specific copy
- Generate relevant hashtags
- Avoid guaranteed-viral claims

## Phase 3 — Publishing
- Instagram official API
- Threads official API
- X official API if access/cost conditions are acceptable
- Reddit official API

## Phase 4 — Reliability
- Validation
- Duplicate detection
- Retry with backoff
- Rate-limit handling
- Per-platform success/failure
- Telegram completion report

## Phase 5 — Documentation
- Setup guide
- Credential guide
- Troubleshooting
- Changelog
- Example workflow export

Publishing stays disabled until credentials are configured and the user approves generated content.


## Current implementation status

- [x] Added `.env.example` for local Ollama configuration.
- [x] Added the social content-generation prompt.
- [x] Added the first importable n8n draft workflow: Telegram image -> original binary -> Ollama vision -> structured JSON -> Telegram draft.
- [x] Added local setup instructions.
- [ ] Add approval/publish workflow.
- [ ] Add official Instagram/Threads publisher.
- [ ] Add Reddit publisher.
- [ ] Add X publisher only if its current API access/cost is acceptable.
