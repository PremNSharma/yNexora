# yNexora

An AI-powered application for working with technical documents through retrieval, analysis, summarization, and grounded question answering.

## Overview

yNexora combines **retrieval-augmented generation (RAG)** with a supervisor-driven workflow to route different document tasks through specialized components. The system is designed to keep LLM responses connected to the source material rather than relying only on free-form generation.

## Capabilities

- Research-document ingestion and processing
- Relevant-context retrieval through vector search
- Technical content analysis
- Grounded summaries
- Question answering over document context
- Page-level source references
- Supervisor-driven task routing

## AI Architecture

```text
User Request
     ↓
Supervisor
     ↓
┌────────────┬─────────────┬──────────────┐
│ Retriever  │   Analyzer  │  Summarizer  │
└────────────┴─────────────┴──────────────┘
     ↓
Grounded Response
     ↓
Conversation / Follow-up
```

The workflow is implemented with LangGraph and LangChain, with OpenAI models providing the language-processing layer. Retrieved context is passed into downstream generation so responses can remain grounded in the selected documents.

## Technology Stack

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

## Project Structure

```text
backend/
└── app/
    ├── agents/       # Agent workflow
    ├── api/          # API routes
    ├── database/     # MongoDB / Qdrant integrations
    ├── rag/          # Retrieval and vector-store logic
    └── config.py     # Configuration
```

## Project Goal

yNexora explores practical AI application design beyond simple prompt-and-response interfaces, with an emphasis on retrieval, task routing, grounded generation, and traceable document-based answers.

## Status

Active development and experimentation.

## Author

**Prem Sharma**

GitHub: https://github.com/premsharma8168
LinkedIn: https://www.linkedin.com/in/prem-narayan-sharma-316291
