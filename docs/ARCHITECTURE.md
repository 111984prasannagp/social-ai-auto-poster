# Architecture

## Current Phase 1

Telegram image → Telegram Trigger → download image → preserve image binary → OmniRoute local API → free vision model → structured JSON → Telegram approval → Instagram / Threads / Facebook → Telegram result.

## Current components

### Telegram intake
The user sends one finished image to the Telegram bot. The workflow selects the largest Telegram photo variant and downloads it. For exact original bytes, sending the image as a Telegram document/file is preferred because Telegram photo messages may contain resized variants.

### Original-image preservation
n8n keeps the downloaded image binary separately from AI-generated text. The AI does not replace the publishing media.

### OmniRoute
n8n calls the local OmniRoute OpenAI-compatible endpoint on the Windows host through Docker networking:
`http://host.docker.internal:20128/v1/chat/completions`

The current design uses a free vision-capable model through OmniRoute.

### Content contract
The intended Phase 1 output is:

```json
{
  "topic": "",
  "audience": "",
  "hook": "",
  "instagram": {"caption": "", "hashtags": []},
  "threads": {"text": "", "hashtags": []},
  "facebook": {"caption": "", "hashtags": []}
}
```

The AI should use the image as the source of truth, avoid invented facts, avoid spammy/repetitive hashtags, and never promise guaranteed virality, followers, views, or likes.

### Approval
Telegram approval is the default safety gate. Publishing must stop unless the approval result is explicitly accepted.

### Platform adapters
Phase 1 targets Instagram, Threads, and a Facebook Page. Each adapter should be isolated so later reliability logic can retry only failed platforms.

## Planned multi-provider AI

The planned free-first provider set is:
1. OmniRoute
2. OpenRouter
3. Google AI Studio / Gemini
4. Groq
5. NVIDIA

Ollama is not part of the current provider-failover implementation.

Planned routing includes capability matching, model fallback, retryable-error detection, rate-limit handling, circuit breaking, and a cost guard that blocks paid models.

## Planned reliability layer

- Duplicate protection
- Automatic retry with backoff
- Per-platform success/failure tracking
- Error logging
- Telegram completion reports
- Health check
- Publishing dashboard
- Configuration backup

These are planned features, not all currently implemented.
