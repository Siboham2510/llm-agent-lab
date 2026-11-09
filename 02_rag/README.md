# 02 — Retrieval-Augmented Generation

## Objectives

Understand how external knowledge can be prepared, retrieved, and supplied to a language model, and how to measure the quality of each stage.

## Concepts to understand

- Document ingestion, PDF/text extraction, cleaning, and metadata
- Chunk size, overlap, and structure-aware splitting
- Embedding models and vector representations
- Vector databases, similarity search, and hybrid retrieval
- Reranking, context assembly, and answer grounding
- Retrieval and generation evaluation, including failure analysis

## Planned implementations

- Load and normalize small text and PDF collections.
- Compare chunking strategies and embedding-based nearest-neighbor results.
- Build a complete retrieve-then-generate pipeline with source references.
- Compare vector and hybrid search, then evaluate reranking.
- Create a small retrieval evaluation set and report measurable results.

## Relevant technologies

Python, Jupyter, document extraction utilities, embedding APIs or models, vector stores, and reranking tools as needed.

## Suggested progression

1. Inspect extraction and preprocessing on a tiny corpus.
2. Compare chunks and embeddings independently.
3. Add vector search and inspect retrieved evidence.
4. Connect retrieval to generation with citations.
5. Measure retrieval and answer quality before tuning components.
