# Build Plan

## Phase 1 — Foundation
- Local n8n
- Telegram bot
- OmniRoute on Windows
- Free vision-capable model
- JSON output contract
- Safe-mode approval

## Phase 2 — Content generation
- Analyze image
- Detect topic and useful context
- Generate clear, attractive, non-spammy platform-specific copy
- Generate relevant hashtags
- Avoid guaranteed-viral claims
- Preserve the original image as the only media asset

## Phase 3 — Publishing
- Instagram official API
- Threads official API
- Reddit official API
- X official API only if current access/cost is acceptable

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

- [x] Added `.env.example` for local configuration.
- [x] Added the social content-generation prompt.
- [x] Added an importable n8n workflow: Telegram image -> original binary -> OmniRoute free vision -> structured JSON -> Telegram draft.
- [x] Added local OmniRoute setup instructions.
- [ ] Add Telegram approval gate.
- [ ] Add official Instagram/Threads publisher.
- [ ] Add Reddit publisher.
- [ ] Add X publisher only if current API access/cost is acceptable.
- [ ] Add retry, duplicate detection, and completion reporting.
