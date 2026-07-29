# Bijan Pourriahi

**Senior Software Engineer - Platform Engineering, APIs & Developer Tooling**  
Rust · Python · APIs · Integrations · Developer Tooling · AI Workflows · Production Systems

I build developer-facing platforms, APIs, integrations, workflow systems, and production infrastructure that make complex systems easier to develop, debug, operate, and trust.

My strongest work is in systems where reliability, clear interfaces, reproducible workflows, observability, and operational usefulness matter: API/integration layers, CLIs, internal tools, runtime systems, data pipelines, dashboards, automation workflows, and production monitoring.

I have built SaaS products, market research platforms, browser automation infrastructure, financial systems, research platforms, dashboards, browser extensions, CLIs, and backend services. The common thread is ownership: architecture, implementation, deployment, debugging, operations, and iteration until the system is usable in practice.

Recent work includes Rust/Python platform infrastructure where I was the primary user, so developer experience, debugging speed, fast feedback loops, and operational visibility directly shaped the architecture.

## Developer Platform & Tooling

I build systems that reduce friction around complex workflows: clear APIs, CLI tools, reproducible execution, workflow automation, evidence capture, local debugging tools, dashboards, and operational review surfaces.

Recent work includes:

- Rust/Python runtime and platform components for replay, simulation, live evaluation, account-state tracking, risk controls, and operational review
- CLI tools and local workflows for inspecting system state, running repeatable evaluations, and reviewing results
- MCP interfaces and agent-facing tools for AI-assisted interaction with internal services
- tmux-based Codex CLI / Claude Code workflows for architecture exploration, implementation, debugging, testing, documentation, and automation
- dashboards and monitoring views that make complex runtime behavior easier to inspect and trust

## APIs & Integrations

I have built integration layers across external systems with different reliability characteristics, including REST APIs, WebSocket services, authentication flows, broker/execution APIs, market-data providers, browser automation systems, CLIs, dashboards, and internal tooling.

Relevant work includes:

- API and WebSocket command/control flows
- authentication and external-provider integration handling
- broker, execution, market-data, and provider access integrations
- browser automation infrastructure with proxy/session management, account isolation, provider access routing, retries, logging, failure recovery, Dockerized workers, and monitoring
- internal APIs and tools for SaaS products, research systems, dashboards, and operational workflows

## Production Systems Example: Financial Infrastructure

I built an internal futures execution and monitoring workstation for managing multiple live accounts from one operator surface. The system combined execution, account fan-out, risk controls, live state monitoring, strategy dispatch, replay workflows, and operational review.

The important engineering problem was not trading itself. It was building a reliable platform where correctness, observability, external integrations, failure handling, and operator clarity mattered.

Key capabilities:

- Managed 10+ accounts simultaneously from a single execution and monitoring UI
- Fan-out/copy execution across account groups with per-account position, balance, drawdown, and guardrail visibility
- Live state monitoring, account health checks, risk controls, kill switches, flatten/cancel controls, and operator-facing explanations
- Replayable workflows for historical simulation, live evaluation, dispatch review, and reproducible result capture
- Strategy/configuration comparison views for reviewing system behavior across large evaluation runs

![Trading fleet dashboard](./assets/trading-fleet-dashboard.png)

![Strategy explorer](./assets/strategy-explorer.png)

![Live execution dashboard](./assets/live-execution-dashboard.png)

![Mobile control surface](./assets/mobile-control-surface.png)

## Featured Engineering Work

### [QuantBox / Aikido Systematic Trading](https://github.com/beejmaxx/aikido-systematic-trading)

Rust-first research and runtime platform combining simulation, replay, data pipelines, operational tooling, and execution workflows for systematic financial infrastructure.

**What it demonstrates:**

- Rust/Python platform engineering
- Runtime and simulation architecture
- Replayable workflows
- API/integration design
- Evidence capture and operational review
- Risk/state modeling
- Production-oriented debugging and observability

### [Vector Backtester](https://github.com/beejmaxx/vector-backtester)

ClickHouse-backed analytics and evaluation engine using SQL-native vectorized execution for high-volume historical data workflows.

**What it demonstrates:**

- Data modeling
- ClickHouse analytics
- Query optimization
- SQL-native evaluation workflows
- High-volume data processing
- Performance-oriented system design

### [Polymarket Trader Intelligence](https://github.com/beejmaxx/polymarket-trader-intelligence)

CLI toolkit for wallet alerts, replayable market analysis, SQLite storage, and local intelligence workflows.

**What it demonstrates:**

- CLI product design
- Data extraction and normalization
- SQLite-backed local workflows
- Replayable event storage
- User-facing automation tools

### [Matching System](https://github.com/beejmaxx/matching-system)

Explainable event-matching system for cross-platform market analysis.

**What it demonstrates:**

- Event matching
- Data normalization
- Explainable matching logic
- Cross-platform data modeling
- Research tooling

### Frontend / Product Work

Built complete product interfaces, dashboards, admin tools, browser extensions, and customer-facing workflows across SaaS, analytics, automation, and internal operations products.

**What it demonstrates:**

- Full-stack product development
- TypeScript/React interfaces
- Dashboards and admin tools
- Browser extensions
- UX for complex data workflows
- API integration

## Core Engineering Areas

- Platform engineering and developer tooling
- API design and external integrations
- Rust/Python systems engineering
- Workflow systems, CLIs, and internal tools
- AI-assisted development workflows, MCP interfaces, and agent tooling
- Backend architecture and service design
- Data modeling and database design
- Query optimization and performance tuning
- Monitoring, observability, dashboards, and production debugging
- DevOps, Linux systems, deployment automation, and CI/CD
- SaaS products, operational platforms, and data-heavy systems

## Stack

**Languages:** Rust, Python, Ruby, Go, TypeScript, SQL  
**Systems/APIs:** API design, WebSockets, REST integrations, command/control flows, CLIs, internal tools, browser tools, GraphQL ecosystem, federation patterns  
**AI tooling:** Codex CLI, Claude Code, MCP servers/tools, agent workflows, AI-assisted debugging/review/documentation  
**Backend:** Ruby on Rails, FastAPI, APIs, WebSockets, background jobs, service architecture, CLI systems  
**Data:** PostgreSQL, ClickHouse, SQLite, ETL, data modeling, event logs, analytics pipelines  
**Infrastructure:** Kubernetes, Docker, AWS, Linux, Ansible, CI/CD, sysadmin, Grafana, Prometheus, monitoring  
**Domains:** SaaS, internal tools, automation, analytics, research infrastructure, financial systems, data-heavy products

## Links

- Portfolio: [beejmaxx.github.io](https://beejmaxx.github.io/)
- Resume: [beejmaxx.github.io/resume.pdf](https://beejmaxx.github.io/resume.pdf)
- Email: bijan.pourriahi@gmail.com
