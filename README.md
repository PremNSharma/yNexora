# yNexora — AI Research & Knowledge Assistant

> An AI/ML-powered research workspace for exploring papers, retrieving relevant context, analyzing technical content, generating structured summaries, and asking grounded questions over uploaded research.

## Overview

yNexora combines **retrieval-augmented generation (RAG)** with a **multi-agent workflow** to make research material easier to search, understand, and analyze. Instead of treating an LLM as a standalone chatbot, the system routes research tasks through specialized components for retrieval, analysis, summarization, and conversational question answering.

## What it does

- 📄 Ingests and works with research papers and their content
- 🔎 Retrieves relevant passages using a vector-search workflow
- 🧠 Analyzes research contributions, methodology, and limitations
- 📝 Generates technical summaries grounded in the uploaded material
- 💬 Answers research questions using retrieved context
- 📚 Provides page-level citations such as `[Page X]`
- 🤖 Uses a supervisor-driven agent workflow to select the appropriate research operation

## AI / ML Architecture

The research workflow is implemented with **LangGraph** and **LangChain**, with OpenAI models powering the language-processing layer.

```text
User Query
    ↓
Supervisor Agent
    ↓
┌───────────────┬──────────────┬────────────────┐
│   Retriever   │   Analyzer   │   Summarizer   │
└───────────────┴──────────────┴────────────────┘
    ↓
Grounded Context / Research Response
    ↓
Chat / Follow-up Interaction
```

The backend uses a stateful graph to route requests between retrieval, analysis, summarization, and chat operations. Retrieved document context is passed to the language model so responses remain grounded in the selected research material.

## Core Technologies

### AI / ML
- Python
- OpenAI API
- LangChain
- LangGraph
- Retrieval-Augmented Generation (RAG)
- Vector search
- LLM-based document analysis

### Backend & Data
- FastAPI
- MongoDB
- Qdrant
- Docker

### Engineering
- Modular agent architecture
- Async Python workflows
- API-based application design
- Environment-based configuration

## Project Structure

```text
backend/
└── app/
    ├── agents/          # Research agent workflow
    ├── api/              # API routes and endpoints
    ├── database/         # MongoDB / Qdrant integrations
    ├── rag/              # Retrieval and vector-store logic
    └── config.py         # Application configuration
```

## Why yNexora?

yNexora is an exploration of how modern AI systems can move beyond simple prompt-and-response applications toward **grounded, tool-oriented workflows**. The project focuses on making LLM-based research assistance more structured, traceable, and useful for technical material.

## Status

Active development and experimentation.

## Author

**Prem Sharma**

- GitHub: https://github.com/premsharma8168
- LinkedIn: https://www.linkedin.com/in/prem-narayan-sharma-316291
