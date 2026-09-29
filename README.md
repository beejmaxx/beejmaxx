**Systems engineer building runtimes, integrations, and tools for complex,
stateful systems.**

I build around external processes and imperfect boundaries: durable state,
reconciliation, cancellation and recovery, protocol design, evidence capture,
and operator-facing controls. I work primarily in Rust, Python, and TypeScript
and have owned systems from architecture and integration through production
debugging and operations.

My recent work includes applying that systems discipline to external AI agents
and agent-facing protocols. The focus is not another model wrapper; it is the
operational infrastructure around long-running work.

## Selected work

### [Aikido](https://github.com/beejmaxx/aikido-systematic-trading)

Rust-first infrastructure for systematic-trading research, replay, simulation,
runtime decisions, and evaluation.

- unifies accounting behavior in an event-driven, one-account state machine
  with explicit invariants;
- turns large predicate-search spaces into staged bitset and graph search,
  reserving canonical simulation for finalist verification;
- reconciles desired exposure against observed broker state and retains input
  lineage, evaluation contracts, and reproducible artifacts.

### [Agent Supervisor](https://github.com/beejmaxx/agent-supervisor)

A Rust research prototype for supervising external AI agents as long-running,
unreliable processes.

- models durable attempts, interruption, generation fencing, and SQLite-backed
  recovery;
- records effects before dispatch, preserves receipts, and represents ambiguous
  outcomes explicitly;
- distinguishes hosted, managed, and external authority while keeping observed
  workspace changes separate from agent claims.

It is an experiment in lifecycle, authority, and evidence—not a production
security boundary or a universal agent framework.

### [MCPHub RS](https://github.com/beejmaxx/mcphub-rs)

A Rust-native MCP gateway that supervises stdio servers behind bounded
Streamable HTTP, propagates cancellation, and owns child-process cleanup. It
validates routes, origins, schemas, and structured results while recording
capability routing and execution decisions in SQLite.

### [Polymarket MCP](https://github.com/beejmaxx/polymarket-mcp-rs)

A self-contained Rust MCP server that exposes live market data, recording, and
authenticated trading through explicit capability profiles. Mutation requires
separate opt-in and per-operation confirmation; financial values and large
identifiers remain exact across the JSON boundary.

### [HTTP Bot Defense Lab](https://github.com/beejmaxx/http-bot-defense-lab)

A synthetic Go environment for request-time policy, behavioral correlation,
adversarial replay, analyst operations, and intervention review. It keeps false
positives, missed abuse, review capacity, and detector limits visible rather
than presenting synthetic results as production accuracy.

### [Depthfield](https://github.com/beejmaxx/depthfield)

A backendless WebGPU market-depth instrument driven by public exchange data. It
reconstructs the order book from REST snapshots and sequenced WebSocket diffs,
detects gaps, retains bounded history in IndexedDB, and renders it in one GPU
pass.

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
- shorten the loop between an incident, an explanation, and a verified fix;
- preserve enough evidence for another engineer to inspect what happened.

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
