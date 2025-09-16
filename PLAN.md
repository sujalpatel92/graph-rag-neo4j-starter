# graph-rag-neo4j-starter — Plan (Architecture & Stack)

## Guiding Principles

- Prefer free/open-source components.
- Python projects: Python 3.12+ with uv for env+deps.
- Keep local dev friction low (Docker Compose first).

## High-Level Architecture

- Ingestion: watch a local folder, parse PDFs/HTML/text, produce cleaned chunks with metadata.
- NLP pipeline: entity and relation extraction on chunks, produce entity/edge candidates with confidence.
- Graph build: write entities, relations, and chunk-node links into Neo4j CE; maintain provenance.
- Indexing: push chunk text and enriched fields into OpenSearch/Elasticsearch; cache hot answers in Redis.
- Query service: FastAPI exposes query modes (text, entity, relationship, combined) and returns citations.
- UI: Streamlit app for upload, graph preview, search, and a citations panel.

## Tech Choices

- Language(s): Python (FastAPI, Streamlit) first
- API/UI: FastAPI for backend APIs; Streamlit for simple UI
- Storage: Neo4j CE for graph; optional Postgres later if needed
- Caching/Queue: Redis (simple cache, optional task queue pattern)
- Search/Index: OpenSearch or Elasticsearch
- Graph (optional): Neo4j Community
- Auth: Demo token or no-auth locally; plan JWT later
- Observability: OpenTelemetry traces, Prometheus/Grafana via Compose
- Packaging: uv (Python)
- Containerization: Docker (multi-stage)
- Deploy targets: Docker Compose; ECS optional later

## Diagrams

- Add a simple system diagram (Mermaid or PNG) in README later.

## Security & Privacy Considerations

no secrets in repo, local .env for API keys

## Local Development

- `docker compose up` for services
- `uv sync` for deps or `uv pip install -e ".[dev]"`

## Testing Strategy

- Unit tests for ingestion, extraction, and query routing
- Lightweight e2e smoke via CI against mocked services

## Licensing

- MIT
