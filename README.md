# Seb4Ez

Systems and backend developer focused on deterministic AI runtimes, agentic tooling, and resilient client SDKs.

My work centers on bridging probabilistic AI systems with deterministic software engineering: eliminating unhandled edge cases in model outputs, optimizing payload latency with zero external dependencies, and contributing to open-source developer tooling and distributed protocols.

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
