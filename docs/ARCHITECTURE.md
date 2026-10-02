# Architecture

Telegram image -> Telegram Trigger -> Download original image -> Ollama vision analysis -> Generate platform-specific JSON -> Approval -> Publish original image -> Telegram result.

## Quality rule
The AI never replaces the original upload. The original Telegram file remains the publishing binary. AI output is text metadata only.

## AI output contract
{
  "topic": "",
  "audience": "",
  "hook": "",
  "instagram": {"caption": "", "hashtags": []},
  "threads": {"text": "", "hashtags": []},
  "x": {"text": "", "hashtags": []},
  "reddit": {"title": "", "body": "", "hashtags": []}
}

The model must return valid JSON only.
