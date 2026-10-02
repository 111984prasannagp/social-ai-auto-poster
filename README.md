# Social AI Auto Poster

Free-first local automation: send one finished image to Telegram, let local AI create platform-specific text, approve it, then publish the original image to Instagram, Threads, X, and Reddit.

## Core rules
- No paid AI API required.
- AI runs locally through Ollama.
- n8n is self-hosted locally.
- The original image is preserved for publishing; AI is used for analysis/text only.
- Human approval is the default before publishing.
- Never commit tokens, passwords, OAuth secrets, or .env files.

## Architecture
Telegram -> Local n8n -> Ollama Vision Model -> Platform-specific content -> Approval -> Official platform APIs -> Telegram result.

## Status
Phase 1: repository structure and architecture.
Phase 2: Telegram intake + Ollama vision generation.
Phase 3: platform credentials and publishing adapters.
Phase 4: testing, retries, rate limits, and logging.

## Free-only note
Platform APIs can have eligibility, rate limits, or fees. This project does not bypass platform rules and does not claim guaranteed free API access forever for every platform.

## Hardware target
Windows PC with NVIDIA RTX 3050 6GB + 16GB RAM, using a suitable small vision model in Ollama.
