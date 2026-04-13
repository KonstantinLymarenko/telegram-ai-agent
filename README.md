# Telegram AI Agent

A Telegram bot powered by an AI agent with conversation memory, built with **n8n** (no-code automation platform).

## What it does

Send a message to the Telegram bot — the AI agent reads it, remembers context from previous messages in the session, and replies intelligently.

## Architecture

```
Telegram (user message)
        ↓
  Telegram Trigger
        ↓
    AI Agent  ←→  Simple Memory (conversation buffer)
        ↓
Google Gemini (LLM)
        ↓
  Send Reply
        ↓
Telegram (response)
```

## Stack

| Component | Tool |
|-----------|------|
| Automation platform | [n8n](https://n8n.io) |
| LLM | Google Gemini |
| Memory | n8n Window Buffer Memory |
| Interface | Telegram Bot API |

## How to use

1. Import `workflow.json` into your n8n instance
2. Create credentials:
   - **Google Gemini API** — get key at [Google AI Studio](https://aistudio.google.com)
   - **Telegram Bot** — create bot via [@BotFather](https://t.me/BotFather)
3. Connect credentials to the nodes
4. Activate the workflow
5. Message your bot

## Files

- `workflow.json` — n8n workflow export (ready to import)

## Notes

Built as a learning project to explore n8n agentic workflows and LLM integration via no-code tools.
