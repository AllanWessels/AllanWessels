Applied AI engineer with 20+ years of end-to-end ownership across agentic systems, ML, and distributed data infrastructure. I design and ship production agentic architectures — MCP servers, multi-agent workflows, tool-augmented LLM systems, and RAG pipelines — that turn ambiguous business problems into measurable customer outcomes.

Daily practitioner of agentic engineering: Claude Code as the development backbone, Subagents and Agent Teams for parallelized work, Agents & Skills for scale/efficiency/accuracy, MCP servers to give agents real access to real systems, and RAG pipelines to put users in the drivers seat.

### What I'm building lately

🤖 [Bratan](https://github.com/AllanWessels/Bratan) — Self-improving RAG framework driven by an adversarial three-agent closed loop: red-team generates test cases the pipeline fails on, blue-team edits chunking/retrieval/prompts to fix them, judge scores every iteration against a co-evolving test set with Sonnet 4 at temperature 0 (never downgraded). User brings only a corpus + seed cases; blue team owns chunking, hybrid BM25+dense retrieval, reranking, generation, citation verification, and every hyperparameter. Five vector-DB adapters (ChromaDB / Qdrant native-hybrid / Pinecone / Weaviate / pgvector) plus a custom slot. Cost-controlled by a local Qwen pre-judge for inner-loop sweeps + sample-efficient hyperparameter search (Optuna BO, grid, ablation, PSO) — oracle validates every winner. Subprocess-isolated ingest worker, prompt-cache, drift detection, 7 stop reasons. FastAPI + Vite/React setup wizard with on-the-fly seed validation against the corpus, live WebSocket dashboard, GitHub Actions CI. 475+ tests across pytest / vitest / Playwright. Built end-to-end through ~25 sub-agent parallel fan-outs across 6 milestones — the multi-agent build process is itself part of the artifact.

🏎️ **[f1_RAG](https://github.com/AllanWessels/f1_RAG)** — F1 question-answering system with **four progressively more sophisticated retrieval architectures** (naive → hybrid → +rerank → +router) evaluated side-by-side on a 30-question, 6-bucket frozen eval harness. Hybrid BM25+dense over Qdrant, bge-reranker-v2-m3, Haiku 4.5 routing via tool-use across three retrievers (SQLite stats, Wikipedia narratives, FIA regulation PDFs), Sonnet 4.6 synthesis with structured citations and refusal detection. Self-hosted Langfuse tracing. Built using Claude Subagents in 6 parallel execution waves across 14 milestones — the agentic build process is itself part of the artifact.

🔌 **[NBA-MCP](https://github.com/AllanWessels/NBA-MCP)** — Production-style MCP server exposing ~28k NBA player-game rows to Claude Desktop, Cursor, and any MCP-compatible client. Python + FastMCP + asyncpg over Postgres, dual stdio and Streamable-HTTP transports. Demonstrates the "vending a database to AI agents safely" pattern: no `execute_sql`, every tool a specific parameterized intent.

🛩️ **[anomaly-detection](https://github.com/AllanWessels/anomaly-detection)** — Unsupervised flight-data anomaly detection. 1D convolutional autoencoder in PyTorch with per-channel z-scored residuals for *explainable* scoring — you see not just *that* a flight was anomalous but *which sensors* drove it. FastAPI upload UI, scores in under a second on CPU.

🎰 **[MAB](https://github.com/AllanWessels/MAB)** — Multi-armed bandit service in Go + gRPC + DynamoDB. UCB, ε-greedy, and ε-decay over a single Pull RPC, with per-experiment state isolation. The kind of adaptive A/B/n routing primitive most product teams end up needing.

### Background

Independent consultant since 2008, embedded across AI/ML, data engineering, backend, and industrial control for clients in trading, aerospace, sports analytics, and manufacturing. Operate as the entire engineering function across multiple parallel engagements — discovery, architecture, build, ship, adoption, DevOps.

Earlier: Senior Manager of Technical Product Marketing & Partner Development at **Greenplum** (acquired by EMC) · Technical Product Manager at **Tellme Networks** (acquired by Microsoft) · Engagement Manager at **Amazon** · Lead PM / Technical Evangelist and Engineering Manager at **Microsoft**.

### Stack I reach for

**Languages:** Python · Scala · Java · C/C++ · SQL · Go

**Agentic / LLM:** MCP (FastMCP) · Claude Agent API · Claude Subagents and Agent Teams · LangChain · structured outputs · grounded generation

**ML:** PyTorch · TensorFlow/Keras · scikit-learn · autoencoders · Monte Carlo · multi-armed bandits

**Backend:** FastAPI · Akka · gRPC · asyncpg · microservices

**Data:** PostgreSQL · DynamoDB · MongoDB · HBase · Kafka · BigQuery · Polars · DuckDB · Qdrant

**Cloud / Infra:** GCP · AWS · Docker · Kubernetes · Terraform

### Get in touch

📍 San Francisco Bay Area
✉️ j.allan.wessels@gmail.com
💼 [LinkedIn](https://www.linkedin.com/in/allan-wessels-a1b147406/)

Open to substantive conversations about hard AI/ML problems where someone has to own the work end-to-end.
