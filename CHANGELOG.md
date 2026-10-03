# Changelog

## 2026-10-03

- Synced repository documentation with the current project direction.
- Phase 1 scope is Instagram, Threads, and Facebook.
- Removed X and Reddit from the current Phase 1 plan.
- YouTube is planned later as a separate video/Shorts pipeline.
- Documented OmniRoute as the current local AI gateway.
- Documented free vision AI and structured social-content output.
- Documented Telegram human approval as the default publishing gate.
- Documented credential placeholders and inactive-by-default safety behavior.
- Added the planned multi-provider free-first roadmap: OmniRoute, OpenRouter, Google AI Studio/Gemini, Groq, and NVIDIA.
- Added planned reliability, batch, scheduling, history, analytics, and dashboard work.

## 2026-10-02

- Created project repository structure.
- Added free-first architecture.
- Added original-image preservation rule.
- Switched image analysis from Ollama to OmniRoute.
- Selected a free vision-capable model path exposed through OmniRoute.
- Added approval-before-publish as the default.
- Added an importable Telegram → n8n → OmniRoute → JSON draft workflow.

## Security

Never commit access tokens, OAuth secrets, passwords, or `.env` files. Exported workflow examples must use placeholders.
