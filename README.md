# Projects

A collection of full-stack and applied-AI projects. Every one is **public**,
**Dockerized**, **runs offline with no API key** (real OpenAI/LLM calls are
optional, with a heuristic/local fallback), and ships with **CI**.

| Project | What it does | Stack | CI |
| --- | --- | --- | --- |
| [🔍 ai-code-reviewer](https://github.com/rahulkhatri922/ai-code-reviewer) | Reviews Python for bugs, security, performance & style with an engineered GPT-4 prompt + an offline AST/regex analyzer; GitHub-PR-style inline annotations and a `rich` CLI. | FastAPI · React (Monaco) · SQLite | [![CI](https://github.com/rahulkhatri922/ai-code-reviewer/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/ai-code-reviewer/actions/workflows/ci.yml) |
| [📄 resume-matcher](https://github.com/rahulkhatri922/resume-matcher) | Parses resumes (PDF/DOCX) into structured data and matches candidates to jobs via embedding cosine similarity + skill-gap analysis; radar-chart breakdown and a leaderboard. | FastAPI · PostgreSQL · React (Recharts) | [![CI](https://github.com/rahulkhatri922/resume-matcher/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/resume-matcher/actions/workflows/ci.yml) |
| [📖 book-summary-platform](https://github.com/rahulkhatri922/book-summary-platform) | Create, browse, search & publish book summaries with automatic Medium cross-posting; PostgreSQL full-text search. | Django REST Framework · PostgreSQL · React | [![CI](https://github.com/rahulkhatri922/book-summary-platform/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/book-summary-platform/actions/workflows/ci.yml) |
| [📚 rag-book-chatbot](https://github.com/rahulkhatri922/rag-book-chatbot) | Local Retrieval-Augmented Generation chatbot over a library of book summaries; semantic search + cited answers. | LangChain (LCEL) · FAISS · Streamlit | [![CI](https://github.com/rahulkhatri922/rag-book-chatbot/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/rag-book-chatbot/actions/workflows/ci.yml) |
| [🧪 llm-prompt-testing-dashboard](https://github.com/rahulkhatri922/llm-prompt-testing-dashboard) | A/B test prompts across multiple language models and track hallucination rates over time. | Flask · PostgreSQL · React (Recharts) | [![CI](https://github.com/rahulkhatri922/llm-prompt-testing-dashboard/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/llm-prompt-testing-dashboard/actions/workflows/ci.yml) |

### Common design
- **Pluggable LLM providers** — real OpenAI (GPT-4 / ada-002) when a key is set, deterministic offline fallbacks (heuristics + local embeddings) otherwise, so everything runs and tests without credentials.
- **`docker compose up`** brings up each full stack (backend + nginx-served React frontend + database where needed).
- **Tested** — pytest suites with coverage gates (up to 100%) on the projects that ship one; the RAG project runs an offline ingest + retrieval smoke test in CI.

_Each repo's own README covers setup, tests, environment variables, and its API reference._
