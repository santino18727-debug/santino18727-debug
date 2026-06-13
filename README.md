# Eric — Builder, applied AI 🦇

> Local-first RAG, agents & automation. I ship working systems, not demos.

I build **applied AI** with a bias for **running locally** (privacy, cost, control):
retrieval-augmented generation, agentic workflows, and the glue that turns them into
products people actually use. Most of it runs on a single workstation with an
RTX GPU + Ollama, no cloud bill required.

---

### 🧠 What I work on

- **Local RAG, end to end** — a personal knowledge base ("mybrain") served through a
  stdlib **MCP server**: `nomic-embed-text` embeddings on Ollama → Qdrant cosine search →
  sourced top-k chunks. Offline-first, with a keyword-grep fallback when the vector DB is
  down, and a weekly **recall@5 / MRR** eval harness (golden set + cross-encoder reranking).
- **Agentic automation** — an "Alfred" concierge stack on **n8n**: LinkedIn / Meta content
  workflows, Telegram control surface, digest scheduling, webhook integrations.
- **Flutter apps** — educational games and tools (math practice for kids, a headless
  game-logic engine ported 1:1 from Rust to Dart with full test parity).
- **Local AI dev stack** — Ollama + `deepseek-coder-v2` as a manager/worker pattern:
  premium model designs & reviews, local model does the mechanical code. ~10× cheaper.

### 🔧 Stack

`Python` · `Flutter / Dart` · `n8n` · `Ollama` · `Qdrant` · `Docker` · `MCP` ·
`FastAPI` · `Tauri (Rust)` · `Bash / PowerShell`

### 🌱 Open source

I contribute where I have real expertise — **RAG, evaluation, local inference tooling**.

- **DSPy** — evaluation & adapter fixes:
  [#9912](https://github.com/stanfordnlp/dspy/pull/9912) (expose `timeout`/`straggler_limit` on
  `dspy.Evaluate`), [#9914](https://github.com/stanfordnlp/dspy/pull/9914) (stop `dspy.History`
  leaking into the system prompt), [#9915](https://github.com/stanfordnlp/dspy/pull/9915) (clear
  error on reserved `ReAct` output names), [#9913](https://github.com/stanfordnlp/dspy/pull/9913)
  & [#9916](https://github.com/stanfordnlp/dspy/pull/9916) (preserve media metadata in LM content
  blocks).
- **LangChain** — [#38131](https://github.com/langchain-ai/langchain/pull/38131): make
  `ChatHuggingFace.with_structured_output` return Pydantic instances (not plain dicts) for
  `json_schema` / `json_mode`, matching the documented behavior.
- **Haystack** — [#11618](https://github.com/deepset-ai/haystack/pull/11618) (TopPSampler integer
  scores & `top_p=0.0` override), [#11619](https://github.com/deepset-ai/haystack/pull/11619)
  (BM25 `ZeroDivisionError` on a tokenless corpus),
  [#11617](https://github.com/deepset-ai/haystack/pull/11617) /
  [#11616](https://github.com/deepset-ai/haystack/pull/11616) (telemetry decorator & throttle fixes).

---

<sub>📍 Switzerland · Open to collaboration on applied-AI / RAG / automation projects.</sub>
