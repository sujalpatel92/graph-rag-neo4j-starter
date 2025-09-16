# graph-rag-neo4j-starter

> Starter template for evidence-grounded question answering using GraphRAG with Neo4j and FastAPI.

## Features

- Local-first Docker Compose stack with Neo4j, OpenSearch, Redis
- Ingestion for PDFs, HTML, and text files with provenance
- Query modes: text, entity, relationship, combined with citations

## Quickstart

```bash
# clone
git clone https://github.com/{{GITHUB_USER}}/{{REPO_SLUG}}.git && cd {{REPO_SLUG}}

# Python setup with uv
curl -LsSf https://astral.sh/uv/install.sh | sh && uv venv .venv && uv pip install -e ".[dev]"

# run example service
uv run python -m {{PACKAGE_ENTRYPOINT}}
```

## Architecture (Sketch)

- Ingestion → Extraction → Graph writer → Indexer → Query API → UI

- Include Mermaid or PNG diagram later.

## Configuration

- Copy `.env.example` to `.env` and fill values.

## Development

- Lint: `uv run ruff check .` | Format: `uv run black .`

- Test: `uv run pytest -q`

## Roadmap

- MVP → Observability → Deploy

## License

MIT
