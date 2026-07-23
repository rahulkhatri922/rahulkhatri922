# Hi, I'm Rahul Khatri 👋

Full-stack engineer building **applied-AI and ML products** — FastAPI / Django /
Flask backends, React frontends, LLM integrations (RAG, semantic search, prompt
engineering, model evaluation), and classic ML (anomaly detection). I care about
clean APIs, well-tested code, and shipping things that actually run.

Below are seven end-to-end projects. Every one is **public**, **Dockerized**,
**runs offline with no API key** (real OpenAI/LLM calls are optional, with
heuristic/local fallbacks), and has **CI** with tests.

## 🚀 Projects

| Project | What it does | Stack | CI |
| --- | --- | --- | --- |
| [🏆 model-eval-benchmark](https://github.com/rahulkhatri922/model-eval-benchmark) | Benchmark & compare LLM outputs (GPT-4, GPT-3.5, Claude) across standardized eval tasks; multi-dimension human ratings, leaderboards, head-to-head win rates, and inter-rater agreement (Cohen's κ). | Django REST Framework · PostgreSQL · React (Recharts) | [![CI](https://github.com/rahulkhatri922/model-eval-benchmark/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/model-eval-benchmark/actions/workflows/ci.yml) |
| [🚨 log-anomaly-detector](https://github.com/rahulkhatri922/log-anomaly-detector) | Ingests app logs (Apache/Nginx/JSON/syslog), engineers rolling-window features, and flags anomalies in real time with Isolation Forest + Z-score detection; time-series dashboard with anomaly regions and true/false-positive labeling. No LLMs — classic ML. | FastAPI · scikit-learn · React (Recharts) | [![CI](https://github.com/rahulkhatri922/log-anomaly-detector/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/log-anomaly-detector/actions/workflows/ci.yml) |
| [🔍 ai-code-reviewer](https://github.com/rahulkhatri922/ai-code-reviewer) | Reviews Python for bugs, security, performance & style with an engineered GPT-4 prompt + an offline AST/regex analyzer; GitHub-PR-style inline annotations and a `rich` CLI. | FastAPI · React (Monaco) · SQLite | [![CI](https://github.com/rahulkhatri922/ai-code-reviewer/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/ai-code-reviewer/actions/workflows/ci.yml) |
| [📄 resume-matcher](https://github.com/rahulkhatri922/resume-matcher) | Parses resumes (PDF/DOCX) into structured data and matches candidates to jobs via embedding cosine similarity + skill-gap analysis; radar-chart breakdown and a leaderboard. | FastAPI · PostgreSQL · React (Recharts) | [![CI](https://github.com/rahulkhatri922/resume-matcher/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/resume-matcher/actions/workflows/ci.yml) |
| [📖 book-summary-platform](https://github.com/rahulkhatri922/book-summary-platform) | Create, browse, search & publish book summaries with automatic Medium cross-posting; PostgreSQL full-text search. | Django REST Framework · PostgreSQL · React | [![CI](https://github.com/rahulkhatri922/book-summary-platform/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/book-summary-platform/actions/workflows/ci.yml) |
| [📚 rag-book-chatbot](https://github.com/rahulkhatri922/rag-book-chatbot) | Local Retrieval-Augmented Generation chatbot over a library of book summaries; semantic search + cited answers. | LangChain (LCEL) · FAISS · Streamlit | [![CI](https://github.com/rahulkhatri922/rag-book-chatbot/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/rag-book-chatbot/actions/workflows/ci.yml) |
| [🧪 llm-prompt-testing-dashboard](https://github.com/rahulkhatri922/llm-prompt-testing-dashboard) | A/B test prompts across multiple language models and track hallucination rates over time. | Flask · PostgreSQL · React (Recharts) | [![CI](https://github.com/rahulkhatri922/llm-prompt-testing-dashboard/actions/workflows/ci.yml/badge.svg)](https://github.com/rahulkhatri922/llm-prompt-testing-dashboard/actions/workflows/ci.yml) |

## 🛠️ Tech

**Languages:** Python, JavaScript, SQL
**Backend:** FastAPI · Django REST Framework · Flask · SQLAlchemy · PostgreSQL · SQLite
**Frontend:** React · Vite · Recharts · Monaco
**AI / ML:** OpenAI (GPT-4, embeddings) · Anthropic (Claude) · LangChain · FAISS · RAG · prompt engineering · semantic search · model evaluation (Cohen's κ) · scikit-learn · Isolation Forest · anomaly detection · pandas
**DevOps:** Docker · docker-compose · nginx · GitHub Actions

## What ties them together

- **Pluggable LLM providers** — real OpenAI when a key is set, deterministic offline fallbacks (heuristics + local embeddings) otherwise, so everything runs and tests without credentials.
- **`docker compose up`** brings up each full stack (backend + nginx-served React frontend + database where needed).
- **Tested** — pytest suites with coverage gates up to 100% on the projects that ship one; the RAG project runs an offline ingest + retrieval smoke test in CI.

<sub>All projects are MIT-licensed. Each repo's README covers setup, tests, env vars, and its API reference.</sub>
