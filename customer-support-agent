# Customer Support AI Agent

An intelligent email automation system that classifies incoming emails, retrieves relevant information from a knowledge base, drafts professional replies, and notifies the team via Telegram.

## How It Works

1. Gmail Trigger monitors incoming emails
2. AI classifies email as Promotional or Support
3. For Support emails:
   - Vector Store retrieves relevant info from NovaMart Knowledge Base
   - AI Agent drafts a professional email reply
   - Draft is saved in Gmail
   - Team is notified via Telegram

## Tech Stack

- **n8n** — workflow automation
- **Google Gemini** — LLM + embeddings
- **Supabase** — vector database (pgvector)
- **Gmail** — email trigger + draft creation
- **Telegram** — team notifications

## Demo

> **Incoming Email:** "I placed an order 7 days ago and still haven't received it. My order ID is #12345."
>
> **AI Response:** Drafted a professional reply referencing NovaMart's shipping policy and support procedures, signed by James.

## Setup

1. Import `Customer Support AI Agent.json` into n8n
2. Configure credentials: Gmail OAuth, Google Gemini, Supabase, Telegram Bot
3. Upload your knowledge base PDF to Supabase via ingestion workflow
4. Activate the workflow
