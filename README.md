# Bijan Pourriahi

**Systems engineer focused on reliable agent infrastructure, developer tooling,
and stateful execution systems.**

I build around unreliable external processes: process supervision, durable
state, cancellation and recovery, protocol boundaries, evidence capture, and
operator-facing tools. I work primarily in Rust, Python, and TypeScript and
have owned systems from architecture and integration through production
debugging and operations.

My recent work applies that systems discipline to autonomous agents. The goal
is not another LLM wrapper; it is making long-running agent activity easier to
observe, interrupt, reconcile, and trust.

## Selected work

### [Agent Supervisor](https://github.com/beejmaxx/agent-supervisor)

Experimental Rust infrastructure for treating autonomous agents as unreliable
external processes.

- durable attempts, immutable manifests, generation fencing, and SQLite state;
- journal-before-dispatch effects with receipts and explicit
  `outcome_unknown` recovery;
- hosted, managed, and external trust tiers that distinguish what the host can
  actually guarantee;
- Codex app-server and ACP process adapters, foreground interruption, durable
  delegation, and an engine-neutral TUI/JSON-RPC client boundary;
- before/after Git observations kept separate from agent claims.

This is deliberately a research prototype, not a production security boundary
or a universal agent framework. Its README documents the implemented boundary,
adversarial tests, and rejected abstractions.

### [Polymarket MCP](https://github.com/beejmaxx/polymarket-mcp-rs)

A self-contained Rust MCP server that turns live market APIs into bounded,
typed agent capabilities.

- separates public research, realtime recording, and authenticated trading
  into explicit tool profiles;
- removes hidden tools from both discovery and dispatch, while mutation
  requires an additional opt-in gate and per-operation confirmation;
- preserves decimal financial values and 256-bit identifiers across JSON;
- records observed realtime state and dropped updates in SQLite without
  presenting local replay as complete exchange history;
- ships installers, package-manager manifests, release artifacts, SBOMs,
  production canaries, and CI across its supported surfaces.

### [MCPHub RS](https://github.com/beejmaxx/mcphub-rs)

Rust-native MCP gateway and capability-control experiment.

- supervises a real stdio MCP child and exposes modern Streamable HTTP;
- bounds frames, requests, concurrency, stderr retention, and shutdown;
- propagates cancellation and owns child-process cleanup;
- validates origins, exact routes, structured results, and advertised schemas;
- records capability routing, policy decisions, runtime links, and effects in
  SQLite.

### [engine-sim-rs](https://github.com/beejmaxx/engine-sim-rs)

A safe-Rust port of a coupled piston-engine simulation, scripting runtime,
audio pipeline, and renderer-independent model.

- keeps the upstream C++ implementation as a behavioral oracle instead of
  claiming semantic equivalence by inspection;
- separates platform-independent simulation, audio synthesis, device output,
  rendering math, CLI, and WebAssembly boundaries;
- compares deterministic Rust traces against C++ fixtures across engine,
  solver, scripting, and audio behavior;
- exposes a backendless browser utility while retaining a headless testable
  core.

### [HTTP Bot Defense Lab](https://github.com/beejmaxx/http-bot-defense-lab)

A synthetic Go environment for request-time policy, longer-window behavioral
correlation, adversarial replay, analyst operations, and intervention review.

- makes assumptions, observable boundaries, and validation requirements
  explicit rather than presenting synthetic results as production accuracy;
- replays candidate and shadow policy against the same deterministic event
  stream;
- keeps false positives, missed abuse, review capacity, user friction, and
  detector failure modes visible;
- includes regression scenarios for timing jitter, cover traffic, identifier
  rotation, coordination, and legitimate high-intensity use.

### [Depthfield](https://github.com/beejmaxx/depthfield)

A backendless WebGPU market-depth instrument driven by live public exchange
data.

- reconstructs the order book from REST snapshots and sequenced WebSocket
  diffs, detecting gaps instead of silently continuing;
- moves ingestion and reconstruction into a Web Worker and renders history in
  one GPU pass;
- retains bounded multi-resolution history in IndexedDB and exports portable
  recordings;
- includes a public live demo that works without an account, API key, or
  application server.

## Production background

I have built and operated SaaS products, API integrations, browser-automation
infrastructure, data pipelines, internal tools, dashboards, and financial
systems. One internal futures workstation coordinated more than ten accounts
from a single operator surface with per-account state, risk controls, health
checks, kill switches, replay workflows, and operational review.

Across those domains, the recurring work has been similar:

- turn ambiguous operational requirements into explicit interfaces and state;
- integrate external systems with different failure and authentication models;
- make retries, partial failure, cancellation, and recovery visible;
- build tools that shorten the loop between an incident, an explanation, and a
  verified fix;
- preserve enough evidence that another engineer can inspect what happened.

## Tools and languages

- **Languages:** Rust, Python, TypeScript, Go, Ruby, SQL
- **Systems:** async services, CLIs, WebSockets, JSON-RPC, MCP, REST, SQLite,
  PostgreSQL, ClickHouse
- **Infrastructure:** Linux, Docker, Kubernetes, AWS, CI/CD, Grafana,
  Prometheus
- **Product surfaces:** developer tools, dashboards, browser extensions,
  operational control panels

## Links

- [Technical portfolio and case studies](https://beejmaxx.github.io/)
- [Resume](https://beejmaxx.github.io/resume.pdf)
- [bijan.pourriahi@gmail.com](mailto:bijan.pourriahi@gmail.com)
