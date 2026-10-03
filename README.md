# Social AI Auto Poster

Free-first local automation for turning one finished image into platform-specific social copy, getting human approval in Telegram, and publishing the original image through official platform APIs.

## Current Phase 1

Telegram → local n8n (Docker) → OmniRoute (Windows) → free vision-capable AI → structured social copy → Telegram approval → Instagram / Threads / Facebook publishing → Telegram report.

### Platforms
- Instagram — 1 account
- Threads — 1 account
- Facebook — 1 Page
- YouTube — planned later as a separate video/Shorts pipeline

X and Reddit are currently out of Phase 1.

## Status

- [x] Local n8n foundation
- [x] Telegram image intake
- [x] Preserve downloaded image binary
- [x] Local OmniRoute OpenAI-compatible endpoint
- [x] Free vision-capable AI path
- [x] Structured JSON content generation
- [x] Platform-specific Instagram/Threads/Facebook copy design
- [x] Telegram human approval gate
- [x] Credential placeholders in exported workflow
- [x] Safe inactive-by-default workflow design
- [ ] Final live publishing validation
- [ ] Automatic retry and failure handling
- [ ] Duplicate protection
- [ ] Publishing dashboard
- [ ] Multi-provider AI failover
- [ ] Batch/album manager
- [ ] Scheduling and post history
- [ ] Analytics
- [ ] YouTube video/Shorts pipeline

## Free-first rules

Free model/provider availability can change; nothing is guaranteed free forever. Official platform API eligibility, limits, and policies still apply. Never commit tokens, passwords, OAuth secrets, or `.env` files.

## Quality rule

AI generates text metadata. The uploaded image remains the publishing media asset.

## Safety mode

Human approval is the default before publishing. Keep publishing disabled while credentials and platform APIs are being tested.
