# n8n AI Workflows

A collection of real-world AI automation projects built with n8n, LLMs, and modern AI tools.

## Projects

### 1. RAG AI Agent
A document-based Q&A system that answers questions from uploaded PDF files using Retrieval Augmented Generation (RAG).
- **Tools:** n8n, Google Gemini, Supabase (pgvector), Google Drive
- **Folder:** [rag-ai-agent](./rag-ai-agent)

### 2. Customer Support AI Agent
An intelligent email automation system that classifies incoming emails, drafts AI-powered replies using a knowledge base, and notifies the team via Telegram.
- **Tools:** n8n, Google Gemini, Supabase (pgvector), Gmail, Telegram
- **Folder:** [customer-support-agent](./customer-support-agent)

### 3. Research AI Agent
An AI-powered company research system that searches the web and saves detailed analysis to Google Sheets.
- **Tools:** n8n, Google Gemini, Tavily API, Google Sheets
- **Folder:** [research-agent](./research-agent)

### 4. AI Job Matcher
An automated job-matching pipeline that scrapes IT vacancies from jobsearch.az, scores them against a candidate's CV using Google Gemini, and sends Telegram notifications for high-match opportunities.
**Tools:** n8n, Google Gemini, Telegram, jobsearch.az (web scraping)
**Folder:** `ai-job-matcher`

## Tech Stack
- n8n (workflow automation)
- Google Gemini (LLM + embeddings)
- Supabase (vector database)
- Google Drive, Gmail, Google Sheets
- Tavily API (web search)
- Telegram

## Author
Fidan Teymurova — fidanteymrva@gmail.com
