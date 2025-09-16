# graph-rag-neo4j-starter — Actionable Tasks

## Day 0–1 (Scaffold)

- [ ] Create repo with LICENSE=MIT, `.gitignore`, `.env.example`
- [ ] Initialize Python package with uv and minimal FastAPI entrypoint
- [ ] Add Streamlit stub page (upload, simple search box)
- [ ] Add CI (lint + tests) and badges

## Day 2–7 (MVP)

- [ ] Ingestion pipeline for PDFs/HTML/TXT
  - Acceptance: given sample docs, chunks with metadata are saved to a local cache folder
- [ ] Entity + relation extraction module
  - Acceptance: returns entities and relations with types and confidence on test text
- [ ] Graph writer to Neo4j with chunk-node linking
  - Acceptance: nodes, relationships, and provenance edges created; cypher checks pass
- [ ] Text indexer to OpenSearch/Elasticsearch
  - Acceptance: search by keyword returns chunk ids with scores
- [ ] Query API with modes (text/entity/relationship/combined)
  - Acceptance: each mode returns answers with citation ids and sources
- [ ] Streamlit UI: query box, results with citations panel
  - Acceptance: user can ask a question and click to view cited chunks
- [ ] README Quickstart verified in a clean environment

## Week 2 (Polish)

- [ ] Health endpoints, metrics, and structured logging
- [ ] Basic error handling and input validation
- [ ] Minimal e2e smoke test against test containers
- [ ] Docker Compose profiles (dev vs demo data)

## Backlog (Nice-to-have)

- [ ] Observability dashboard in Grafana
- [ ] Benchmarks/evals doc for extraction quality and retrieval accuracy
- [ ] Docker image hardening and non-root user

## Labels

- `type:feature`, `type:bug`, `type:chore`, `good first issue`
