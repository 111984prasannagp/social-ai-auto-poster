# Build Plan

## Phase 1 — Foundation and safe image workflow
**Status: in progress**

- [x] Local n8n in Docker
- [x] Telegram intake
- [x] Preserve image binary
- [x] Local OmniRoute connection
- [x] Free vision-capable AI path
- [x] Structured JSON response
- [x] Human approval gate
- [x] Instagram / Threads / Facebook scope
- [x] Credential placeholders
- [x] Safe inactive-by-default workflow
- [ ] Complete live publishing validation

## Phase 2 — Content quality
**Status: in progress**

- [x] Analyze image topic/context
- [x] Platform-specific copy
- [x] Relevant hashtags
- [x] Non-spammy output
- [x] No guaranteed-viral claims
- [ ] AI caption quality checker
- [ ] Brand voice
- [ ] Content safety checker
- [ ] Caption variations
- [ ] Regenerate/edit before publishing

## Phase 3 — Reliability
**Status: planned**

- [ ] Duplicate protection
- [ ] Automatic retry
- [ ] Retry only failed platforms
- [ ] Error logging
- [ ] Publishing status dashboard
- [ ] Health check
- [ ] Configuration backup

## Phase 4 — Multi-provider AI
**Status: planned**

Target free-first providers: OmniRoute, OpenRouter, Google AI Studio/Gemini, Groq, NVIDIA.

Planned behavior: capability matching, compatible model fallback, timeout/rate-limit handling, circuit breaker, recently-failed provider cooldown, and a cost guard that rejects paid models.

## Phase 5 — Scale and convenience
**Status: planned**

- [ ] Batch/multiple-image processing
- [ ] Telegram approval center
- [ ] Approve All
- [ ] Scheduling
- [ ] Post history/database
- [ ] Analytics
- [ ] Multiple accounts later
- [ ] YouTube video/Shorts pipeline
- [ ] Additional platforms later

## Important rule

Build and test one layer at a time. Automatic publishing stays disabled until credentials, image delivery, AI output, approval, and platform publishing are validated.
