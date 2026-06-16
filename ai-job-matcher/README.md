# AI Job Matcher

An automated job-matching pipeline that scrapes IT vacancies from jobsearch.az, filters them by AI/Automation keywords, scores each vacancy against a candidate's CV using Google Gemini, and sends Telegram notifications for high-match opportunities.

## How it works

1. **Schedule Trigger** – runs daily at 9:00 AM
2. **HTTP Request** – scrapes the jobsearch.az IT vacancies listing page
3. **Code (JavaScript)** – extracts vacancy links via regex and filters by keywords (`ai`, `automation`, etc.)
4. **Split in Batches** – loops through vacancies one by one to respect LLM API rate limits
5. **HTTP Request** – fetches each vacancy's full page
6. **Code (JavaScript)** – extracts title, description, and canonical URL from the raw HTML
7. **AI Agent (Google Gemini)** – compares the vacancy against the candidate's CV and returns a JSON match score (0–100%) with a short reasoning
8. **Code (JavaScript)** – parses and cleans the AI's JSON response
9. **IF** – filters vacancies with `match_percent > 70`
10. **Telegram** – sends a notification with the vacancy title, match %, reasoning, and link
11. **Wait** – adds a delay between iterations to avoid LLM rate limits, then loops back to step 4

## Tools

- n8n (workflow automation)
- Google Gemini (LLM for CV–vacancy matching)
- Telegram Bot API (notifications)
- jobsearch.az (data source, via HTML scraping)

## Why I built this

As a Software Engineering student actively job-hunting, I wanted an automated way to surface relevant AI/automation-focused vacancies without manually checking job boards every day. This project also demonstrates real-world web scraping, AI agent orchestration, rate-limit handling, and third-party API integration — skills directly relevant to automation and backend engineering roles.

## Setup

1. Import `ai-job-matcher.json` into your n8n instance
2. Add your Google Gemini API credentials
3. Add your Telegram Bot token and chat ID
4. Update the candidate CV details inside the AI Agent's System Message
5. Activate the workflow

---

Author: Fidan Teymurova
