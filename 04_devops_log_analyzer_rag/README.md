# AI DevOps Log Analyzer (RAG)

An AI-powered log analysis system that reads server or system logs, detects anomalies, identifies root causes and generates a structured incident report using a RAG (Retrieval Augmented Generation) pipeline. Also includes a FastAPI deployment that serves the full pipeline as a REST API endpoint.

<br>

## How It Works

Log entries are parsed, chunked and embedded using a sentence transformer model. The embeddings are stored in ChromaDB as a local vector database. When an anomaly is detected, the most relevant log chunks are retrieved from ChromaDB and passed as context to the LLM. The LLM then suggests a root cause based on the retrieved context rather than the full log, making the analysis more focused and accurate.

<br>

## Features

- Accepts logs via file upload or direct paste
- Detects anomalies: ERROR, CRITICAL, WARNING, FATAL and more
- RAG pipeline for context-aware root cause analysis
- Generates a structured incident report in Markdown
- Free-form Q&A (Ask any question about your logs)
- FastAPI endpoint that accepts log text and returns full analysis as JSON
- Exports report as `.md` and `.json`

<br>

## Tech Stack

| Tool | Purpose |
|------|---------|
| Groq (Llama 3.1) | LLM for root cause analysis and report generation |
| ChromaDB | Vector database for log storage and retrieval |
| Sentence Transformers | Embedding log chunks for semantic search |
| FastAPI | REST API endpoint for serving the pipeline |
| localtunnel | Exposing the API publicly from Colab |
| Rich | Terminal output formatting |

<br>

## What is RAG

RAG (Retrieval Augmented Generation) is a technique where relevant context is retrieved from a knowledge base before querying an LLM. Instead of sending the entire log file to the LLM, only the most relevant chunks are retrieved and sent, making responses more accurate and avoiding token limits.

<br>

## Files

- `AI_DevOps_Log_Analyzer_API.ipynb`: Full pipeline with FastAPI deployment, file upload and downloadable reports

<br>

## Setup

1. Get a free Groq API key at https://console.groq.com
2. Open the notebook in Google Colab
3. Run all cells and enter your API key when prompted
4. Upload a log file or use the built-in sample logs to test
5. The FastAPI server starts automatically and the public URL is printed

<br>

## Output

The generated incident report includes:
- Incident Summary
- Timeline of Events
- Detected Anomalies
- Root Cause Analysis
- Recommended Actions
- Severity Assessment
