# ai-rag-agent-guide-site

Static, trilingual **OpenRouter embedding models** field guide: RAG use cases, price hints, public example sources, and links to model pages. **English**, **繁體中文**, and **简体中文**.

- Site root: [`rag_model_site/`](./rag_model_site/)
- Long-form reference: [`OPENROUTER_EMBEDDING_MODELS.md`](./OPENROUTER_EMBEDDING_MODELS.md) (also under `rag_model_site/` for publishing)

## Local preview

```bash
cd rag_model_site
python3 -m http.server 8765
# open http://127.0.0.1:8765/
```

Use a local server (not `file://`) so `data/models.json` loads.

## Refresh model data (OpenRouter)

Requires `OPENROUTER_API_KEY`:

```bash
export OPENROUTER_API_KEY="sk-or-..."
uv run python scripts/collect_openrouter_models.py
# optional: --dry-run
```

## GitHub Pages

The workflow [`.github/workflows/pages.yml`](./.github/workflows/pages.yml) deploys the `rag_model_site/` folder. In the repo **Settings → Pages**, set the source to **GitHub Actions**.

See [`rag_model_site/VERIFICATION.md`](./rag_model_site/VERIFICATION.md) for a manual checklist.
