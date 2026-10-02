# Local Setup

## Ollama

Install/update Ollama and pull the first vision model:

```powershell
ollama pull qwen2.5vl:3b
```

The official Ollama registry lists qwen2.5vl:3b as a text+image model with a download size of about 3.2 GB. The project uses this smaller vision model first because the target laptop has 6 GB VRAM.

## Docker n8n to Windows Ollama

Inside the n8n Docker container, use:

```text
http://host.docker.internal:11434
```

Do not use localhost:11434 from inside the container.

## Telegram

Create a bot with BotFather and create an n8n Telegram credential using the bot token. Never commit the token to GitHub.

## Import

Import `n8n/social-ai-draft.json` into the local n8n instance. Select your Telegram credential for the Telegram Trigger and Telegram nodes.

## First test

Send one finished image to the bot. The workflow should download the image, send the original binary to Ollama vision, parse the structured response, and send the generated platform drafts back to Telegram.

Publishing is intentionally not connected yet. We will add official platform API adapters after this local image-to-AI test passes.

## Quality rule

The uploaded image is the media asset. AI is used for image understanding and copy generation only; it must not regenerate or replace the original image.