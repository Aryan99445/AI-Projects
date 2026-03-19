# AI Multi-Agent Research Assistant

An automated research pipeline that takes a topic from the user, searches the web, summarizes sources and generates a structured report, all using 4 specialized AI agents working together.

<br>

## How It Works

The pipeline runs 4 agents in sequence:

**Planner Agent** — Takes the research topic and breaks it down into focused search queries using an LLM.

**Search Agent** — Searches the web for each query using DuckDuckGo (no API key needed).

**Summarizer Agent** — Reads each search result and writes a concise summary using an LLM.

**Report Agent** — Combines all summaries into a structured research report in Markdown format.

<br>

## Features

- Fully automated end to end research pipeline
- No paid search API required — uses DuckDuckGo
- Exports report as both `.md` and `.json`
- Retry logic for API errors
- Configurable number of queries, results and model

<br>

## Tech Stack

| Tool | Purpose |
|------|---------|
| Groq (Llama 3.1) | LLM for all 4 agents |
| DuckDuckGo Search | Free web search |
| Rich | Terminal output formatting |

<br>

## Setup

1. Get a free Groq API key at https://console.groq.com
2. Open the notebook in Google Colab
3. Run all cells and enter your API key when prompted

<br>

## Output

The report is structured into:
- Executive Summary
- Key Findings
- Detailed Analysis
- Current Trends
- Conclusion
- Sources

<br>

