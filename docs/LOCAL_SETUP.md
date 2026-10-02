# Local Setup

## Stack
- Windows
- Docker n8n
- Telegram Bot
- OmniRoute running on Windows
- A free vision-capable model routed through OmniRoute
- Official platform APIs for publishing

## OmniRoute

The local OmniRoute server is expected at:

    http://localhost:20128

From inside the n8n Docker container, use:

    http://host.docker.internal:20128/v1

The ready-made workflow uses:

    openrouter/minimax/minimax-m3:free

The model catalog supplied for this project reports this model as vision-capable and accepting text + image input. fileciteturn11file2

## Authentication

Do not commit your OmniRoute API key to GitHub.

After importing the workflow, open **OmniRoute Free Vision AI** and replace:

    Bearer REPLACE_WITH_YOUR_OMNIROUTE_API_KEY

with your real local OmniRoute API key.

For production, prefer an n8n credential or protected environment variable rather than storing the key in an exported workflow.

## Telegram

Create a Telegram bot with BotFather and create an n8n Telegram credential using the bot token. Never commit the token to GitHub.

Select the Telegram credential for the Telegram Trigger, Telegram Get File, and Send Draft to Telegram nodes.

## Import

Import `n8n/social-ai-draft.json` into your local n8n instance.

## First test

1. Keep the workflow inactive.
2. Configure Telegram and OmniRoute authentication.
3. Listen for the Telegram Trigger and send one finished image to the bot.
4. The workflow downloads the image, preserves its binary data, sends it to OmniRoute vision, parses structured JSON, and returns platform drafts to Telegram.

The AI only understands the image and generates text. It does not regenerate or replace the original image.

## Free-cost note

The selected model is marked `:free` in the model catalog used for this project. Free-model availability and rate limits can change. Platform publishing APIs are separate and may require approved apps, permissions, account eligibility, rate limits, or paid access.

## Publishing

Publishing is intentionally disabled in this first import. Once the image-to-AI test works, add official Instagram, Threads, Reddit, and optionally X publishing adapters.

Never bypass platform API restrictions or scrape private endpoints.