## ***-In process of migrating from Bitbucket to GitHub***




### What I'm building lately

🤖 [Bratan](https://github.com/AllanWessels/Bratan) — Self-improving RAG framework driven by an adversarial three-agent closed loop: red-team generates test cases the pipeline fails on, blue-team edits chunking/retrieval/prompts to fix them, judge scores every iteration against a co-evolving test set with Sonnet 4 at temperature 0 (never downgraded). User brings only a corpus + seed cases; blue team owns chunking, hybrid BM25+dense retrieval, reranking, generation, citation verification, and every hyperparameter. Five vector-DB adapters (ChromaDB / Qdrant native-hybrid / Pinecone / Weaviate / pgvector) plus a custom slot. Cost-controlled by a local Qwen pre-judge for inner-loop sweeps + sample-efficient hyperparameter search (Optuna BO, grid, ablation, PSO) — oracle validates every winner. Subprocess-isolated ingest worker, prompt-cache, drift detection, 7 stop reasons. FastAPI + Vite/React setup wizard with on-the-fly seed validation against the corpus, live WebSocket dashboard, GitHub Actions CI. 475+ tests across pytest / vitest / Playwright. Built end-to-end through ~25 sub-agent parallel fan-outs across 6 milestones — the multi-agent build process is itself part of the artifact.

🏎️ **[f1_RAG](https://github.com/AllanWessels/f1_RAG)** — F1 question-answering system with **four progressively more sophisticated retrieval architectures** (naive → hybrid → +rerank → +router) evaluated side-by-side on a 30-question, 6-bucket frozen eval harness. Hybrid BM25+dense over Qdrant, bge-reranker-v2-m3, Haiku 4.5 routing via tool-use across three retrievers (SQLite stats, Wikipedia narratives, FIA regulation PDFs), Sonnet 4.6 synthesis with structured citations and refusal detection. Self-hosted Langfuse tracing. Built using Claude Subagents in 6 parallel execution waves across 14 milestones — the agentic build process is itself part of the artifact.

🔌 **[NBA-MCP](https://github.com/AllanWessels/NBA-MCP)** — Production-style MCP server exposing ~28k NBA player-game rows to Claude Desktop, Cursor, and any MCP-compatible client. Python + FastMCP + asyncpg over Postgres, dual stdio and Streamable-HTTP transports. Demonstrates the "vending a database to AI agents safely" pattern: no `execute_sql`, every tool a specific parameterized intent.

### Get in touch

📍 San Francisco Bay Area
✉️ j.allan.wessels@gmail.com


