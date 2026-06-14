# RAG AI Agent

A document-based Q&A system that answers questions from uploaded PDF files using Retrieval Augmented Generation (RAG).

## How It Works

1. PDF file is uploaded to Google Drive
2. n8n reads and splits the document into chunks
3. Gemini converts chunks into vector embeddings
4. Embeddings are stored in Supabase (pgvector)
5. User asks a question via chat
6. System finds relevant chunks and generates an answer

## Tech Stack

- **n8n** — workflow automation
- **Google Gemini** — LLM + embeddings
- **Supabase** — vector database (pgvector)
- **Google Drive** — document storage

## Demo

> **Q:** What are the response time and resolution targets for a Priority 1 incident?
>
> **A:** Response Time: Within 1 hour. Resolution Target: Within 4 hours.

## Setup

1. Import `RAG AI Agent.json` into n8n
2. Configure credentials: Google Drive, Gemini API, Supabase
3. Upload your PDF to Google Drive
4. Run the ingestion workflow
5. Start chatting!
