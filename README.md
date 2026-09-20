# Seb4Ez

Systems and backend developer focused on deterministic AI runtimes, agentic tooling, and resilient client SDKs.

My work centers on bridging probabilistic AI systems with deterministic software engineering: eliminating unhandled edge cases in model outputs, optimizing payload latency with zero external dependencies, and contributing to open-source developer tooling and distributed protocols.

---

## Tech Stack & Tooling

### Languages & Runtimes
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)

### Frameworks & Libraries
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=for-the-badge&logo=express&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)

### Databases & Storage
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-039BE5?style=for-the-badge&logo=Firebase&logoColor=white)

### DevOps, CI/CD & Deployment
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab-FC6D26?style=for-the-badge&logo=gitlab&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)
![DigitalOcean](https://img.shields.io/badge/DigitalOcean-0080FF?style=for-the-badge&logo=digitalocean&logoColor=white)

### Observability, Data & Tooling
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=for-the-badge&logo=opentelemetry&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=for-the-badge&logo=grafana&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-ffffff?style=for-the-badge&logo=matplotlib&logoColor=black)
![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=for-the-badge&logo=eslint&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)

---

## Authored Projects

### [JevGuard](https://github.com/seb4ez/jevguard)
*Author & Maintainer | Deterministic Decision Runtime for TypeSafe AI (Jev / System One)*

A deterministic runtime that wraps TypeSafe AI probabilistic model evaluations with state pruning, closed-world escape injection, certainty calibration, and zero-token caching using only the Python standard library.

* **Zero-Dependency Architecture**: Built entirely on Python stdlib (`urllib`, `sqlite3`, `concurrent.futures`, `asyncio`), requiring zero external runtime packages.
* **Sub-Millisecond Local Overhead**: Local pipeline (pruning, hashing, calibration, caching) executes in under 0.22 ms, over 14x below production SLA budgets.
* **Deterministic RAM & Disk Cache**: Canonical SHA-256 fingerprinting with volatile key masking (`timestamp`, `trace_id`, `request_id`). Delivers 0.099 ms cache hits, yielding a 7,711x network speedup and 100% token savings.
* **Closed-World Escape Protection**: Automatically injects `UNRESOLVED_OR_OTHER` fallbacks to isolate out-of-distribution inputs from forcing false positive categorical choices.
* **Uncertainty Calibration**: Automatically flags bimodal ties and low-certainty scores as `AMBIGUOUS_STATE` before downstream business logic executes.
* **Empirical Live Benchmark**: Validated across 50 live production requests on TypeSafe AI's official endpoint with a 100% pass rate.

### [JevGuard MCP Server](https://github.com/seb4ez/jevguard-mcp)
*Author & Maintainer | Model Context Protocol Server for Claude, Cursor & LibreChat*

Official Model Context Protocol (MCP) server for JevGuard, exposing deterministic decision runtime, certainty calibration, state pruning, and SHA-256 fingerprint caching over standard input/output (stdio).

* **Zero External Dependencies**: Implemented strictly with the Python standard library, requiring zero npm, npx, or pip packages.
* **MCP 2024-11-05 Protocol Fidelity**: Fully compliant JSON-RPC 2.0 stdio framing supporting initialize handshakes, tool discovery, and tool execution.
* **Agent Integration**: Pre-configured for single-block integration into Claude Desktop (`claude_desktop_config.json`), Cursor IDE, and LibreChat.

---

## Open Source Contributions & Pull Requests

Contributor submitting targeted improvements, fixes, and client resilience features to upstream open-source repositories:

### [Lily-Protocol / lily-sdk](https://github.com/Lily-Protocol/lily-sdk)
*Decentralized Protocol Client SDK (TypeScript)*

* Contributed to client transport resilience, typed HTTP error taxonomies, and request timeout abort handlers.
* Helped ensure consistent error surfaces for API callers across non-200 HTTP responses.

### [monk-io / monk-plugin](https://github.com/monk-io/monk-plugin)
*AI Coding Agent Integration Plugin*

* Contributed automation scripts and process integration for AI coding agents and developer workflows.

---

## Agentic Systems & Ecosystem Focus

Deploying, testing, and tracking open-source architectures across the autonomous agent and backend ecosystem:

* **Autonomous Agent Runtimes**: Agent state management, episodic memory structures, and multi-agent coordination ([elizaOS](https://github.com/elizaOS/eliza), [LobeHub](https://github.com/lobehub/lobehub)).
* **Model Context Protocol (MCP) & Interfaces**: Tool execution schemas and multi-model interfaces ([LibreChat](https://github.com/danny-avila/LibreChat), [Open-WebUI](https://github.com/open-webui/open-webui)).
* **Backend Data Infrastructure**: Headless CMS engines, real-time databases, and auto-generated API layers ([Directus](https://github.com/directus/directus)).

---

## Technical Competencies

### Systems & Software Engineering
* **Languages**: Python, TypeScript, JavaScript, SQL, PowerShell, Bash.
* **Architecture**: Deterministic finite state machines, in-memory LRU caching, SQLite write-ahead logging (WAL), episodic session storage.
* **Concurrency & I/O**: Thread pool parallel evaluation (`concurrent.futures`), non-blocking asynchronous event loops (`asyncio`), process isolation.
* **Network & Transport**: Exponential backoff with random jitter, HTTP `Retry-After` parsing, connection pooling, typed exception hierarchies.

### AI Engineering & Evaluation
* **Inference Guardrails**: Deterministic validation, categorical escape injection, entropy and dispersion analysis.
* **Context Optimization**: Recursive state pruning, cycle reference protection, volatile metadata sanitization.
* **Testing & Verification**: Comprehensive unit suites, multi-threaded concurrency audits, empirical upstream latency benchmarks.

---

## Engineering Philosophy

1. **Deterministic Guarantees First**: Probabilistic outputs must be bounded by explicit validation layers before reaching critical application state.
2. **Minimal Dependencies**: Prefer robust standard library implementations over external dependency trees when building core runtimes.
3. **Empirical Validation**: Assert performance and reliability through reproducible benchmarks and live network telemetry rather than assumptions.
