# LexRAG FR

Production-grade Retrieval-Augmented Generation (RAG) assistant over versioned French legal documents.

## Goal

LexRAG FR explores reliable question answering over French labour law using official, versioned legal sources. The project focuses on retrieval quality, temporal validity, grounded generation, citations, and reproducible evaluation rather than building a generic legal chatbot.

## Initial scope

The first corpus is the French **Code du travail**. The ingestion pipeline will transform official DILA/LEGI source data into a normalized dataset while preserving article identifiers, status and validity dates.

## Planned pipeline

```text
Official DILA / LEGI data
        ↓
Ingestion & parsing
        ↓
Normalized legal articles
        ↓
Legal-aware chunking
        ↓
Semantic + lexical retrieval
        ↓
Fusion & reranking
        ↓
Grounded LLM generation
        ↓
Answers with legal citations
```

## Roadmap

- [x] Initialize repository
- [ ] Ingest Code du travail source data
- [ ] Normalize articles and temporal metadata
- [ ] Implement legal-aware chunking
- [ ] Build semantic retrieval baseline
- [ ] Add hybrid retrieval
- [ ] Add reranking
- [ ] Generate grounded answers with citations
- [ ] Build retrieval and RAG evaluation suite
- [ ] Expose the pipeline through FastAPI
- [ ] Build a Next.js chat interface
- [ ] Deploy the application

## Project status

**Milestone 01 — Data ingestion**

Current objective: build a reproducible pipeline producing a normalized `code_travail.jsonl` corpus from official French legal data.

## Disclaimer

LexRAG FR is an engineering and research project. It is not a substitute for professional legal advice.
