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

### [MCPHub RS](https://github.com/beejmaxx/mcphub-rs)

Rust-native MCP gateway and capability-control experiment.

- supervises a real stdio MCP child and exposes modern Streamable HTTP;
- bounds frames, requests, concurrency, stderr retention, and shutdown;
- propagates cancellation and owns child-process cleanup;
- validates origins, exact routes, structured results, and advertised schemas;
- records capability routing, policy decisions, runtime links, and effects in
  SQLite.

### [Aikido Systematic Trading](https://github.com/beejmaxx/aikido-systematic-trading)

Rust-first systematic-research and execution workspace spanning deterministic
backtests, predicate sweeps, evidence retention, replay, runtime checks, and
operator-facing inspection surfaces.

The relevant engineering is the boundary between research evidence and runtime
state: reproducible inputs, explicit provenance, typed strategy contracts,
account/risk modeling, and integrations whose failures must remain visible.

### [rithmic-rs](https://github.com/beejmaxx/rithmic-rs)

Unofficial asynchronous Rust client for the Rithmic R Protocol API. It uses
actor-style Tokio tasks and channels for order, market-data, PnL, and history
connections, with explicit connection strategies, health events, heartbeat
handling, and reconnection behavior.

### [codex-recent](https://github.com/beejmaxx/codex-recent)

A small shell/fzf tool for finding and resuming recent Codex CLI conversations.
It is intentionally narrow: one recurring developer-workflow problem, a fast
local solution, and no unnecessary service or framework.

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
