# graph-rag-neo4j-starter — Specifications

## Summary (What)

Starter template for evidence-grounded question answering using GraphRAG with Neo4j and FastAPI.

## Problem & Why Now

Developers struggle to connect LLMs with structured graph knowledge for verifiable answers

## Target Users & Use Cases

- Users: AI engineers, researchers, backend developers
- Primary use cases:
document ingestion, entity+relation extraction, chunk-node linking, query modes (text/entity/relationship/combined), citations panel

## Success Criteria (Outcomes, not outputs)

Ability to ingest documents, build a knowledge graph, and query via RAG with citations

## In Scope

document ingestion, entity+relation extraction, chunk-node linking, query modes (text/entity/relationship/combined), citations panel

## Out of Scope (Non-Goals)

production-scale security, enterprise auth, multilingual support

## Constraints & Assumptions

must run locally via Docker Compose, free OSS only

## Data Sources

PDFs, HTML, text files
