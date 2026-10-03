# Current Project Status

Updated: 2026-10-03

## Current goal

Build a local, free-first AI social media image auto-poster.

## Current flow

Telegram image → n8n Docker → OmniRoute on Windows → free vision-capable AI → platform-specific draft → Telegram approval → official platform APIs.

## Phase 1 platforms

- Instagram
- Threads
- Facebook Page

## Later

- Multi-provider AI failover
- Automatic retry and duplicate protection
- Publishing status dashboard
- Batch/album processing
- Scheduling and post history
- Analytics
- YouTube video/Shorts pipeline
- Additional platform adapters

## Explicitly out of current Phase 1

- X
- Reddit
- Paid AI APIs
- Automatic multi-account publishing
- Ollama-based provider failover

## Current safety state

The workflow is designed to stay inactive until credentials and platform publishing are configured and tested. Human approval remains the default before publishing.

## Important implementation note

The repository documents the intended architecture and project state. Live credentials and local runtime state stay outside GitHub.
