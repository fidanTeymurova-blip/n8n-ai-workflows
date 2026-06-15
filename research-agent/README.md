# Research AI Agent

An AI-powered company research system that automatically gathers and analyzes information about any company using web search, then saves the results to Google Sheets.

## How It Works

1. User submits a form with company name and website
2. AI Agent searches the web using Tavily API
3. Agent analyzes and summarizes the company's target audience, products, and business model
4. Results are automatically saved to Google Sheets

## Tech Stack

- **n8n** — workflow automation
- **Google Gemini** — LLM for analysis and summarization
- **Tavily API** — real-time web search
- **Google Sheets** — data storage and reporting
- **n8n Form** — user input interface

## Demo

> **Input:** Company: OpenAI, Website: openai.com
>
> **Output:** Detailed analysis including target audience, product offerings (ChatGPT, DALL-E, Sora), business model (PLG + Enterprise), and key partnerships — automatically saved to Google Sheets.

## Setup

1. Import `Research AI Agent.json` into n8n
2. Configure credentials: Google Gemini API, Tavily API, Google Sheets OAuth
3. Run the workflow and submit the form
4. View results in your connected Google Sheet
