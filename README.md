# Scott Sans — MANET Engineer · Prediction Market Trader · Applied AI Systems

**Hudson Valley, NY** | scott@hudsonvalleyforestry.com | [github.com/sansscott](https://github.com/sansscott)

I design and deploy production systems end-to-end — off-grid mesh networks for field operations, live algorithmic trading infrastructure on prediction markets, and applied AI pipelines with real-world deployment. I operate these systems under actual conditions: crews in dense canopy with no cell coverage, real capital at risk on Polymarket and Kalshi, and 97+ Docker containers running in production on self-managed bare-metal.

---

## MANET & Tactical Mesh Networking

Mobile Ad-hoc Networks are the backbone of resilient field operations in contested, degraded, and operationally limited (CDOL) environments. I build and operate open-source MANET infrastructure using the Reticulum Network Stack — a cryptographically addressed, transport-agnostic mesh protocol that operates over LoRa, TCP/IP, serial, and RF links with zero infrastructure dependency. Designed for delay-tolerant networking (DTN) and beyond line-of-sight (BLOS) communications where PACE plan contingencies require self-healing, self-organizing network topologies.

### [rns-atak-bridge](https://github.com/sansscott/rns-atak-bridge) — *public*

Bridges Reticulum mesh peers into ATAK Cursor-on-Target (CoT) events, making off-grid mesh nodes visible as situational awareness tracks in ATAK, iTAK, WinTAK, and TAK Server in real time. Enables common operating picture (COP) and position location information (PLI) sharing over a zero-infrastructure mesh — no internet, no cell, no server.

**Stack**: Python · Reticulum RNS · ATAK CoT XML · UDP multicast
**Topics**: `manet` `atak` `cursor-on-target` `reticulum` `tak-server` `mesh-networking` `tactical-communications` `situational-awareness` `delay-tolerant-networking` `off-grid`

### [sycamore-mesh](https://github.com/sansscott/sycamore-mesh) — *private*

Voice-first tactical comms and live tracking dashboard for ROW/pipeline/forestry field crews operating in remote terrain. Real-time node positions over WebSocket, Mapbox GL 3 terrain rendering, push-to-talk coordination layer. Built for crews who cannot rely on cellular — a practical field operations MANET deployment.

**Stack**: Node.js · Socket.io · React · Mapbox GL 3 · Zustand · Docker · Cloudflare Zero Trust
**Topics**: `manet` `mesh-networking` `tactical-communications` `field-operations` `real-time` `push-to-talk`

### [THR-Manet](https://github.com/sansscott/THR-Manet) — *private*

Full Reticulum MANET stack for HVF field operations. Transport node peered to the global RNS backbone via Frankfurt. NomadNet propagation node for store-and-forward messaging. LoRa interface planned for RF link extension. Decentralized network coordination with cryptographic addressing and forward secrecy — no central authority, no single point of failure.

**Node identity**: af60a4f4863c9bff05a9871359d67e1f

---

## Prediction Market Trading

I run systematic strategies across Polymarket and Kalshi — two of the primary regulated venues for binary event contracts in the US. The work sits at the intersection of market microstructure, probabilistic forecasting, and execution infrastructure.

**Current book:**

| Market | Exchange | Strategy | Sizing |
|---|---|---|---|
| Binary event arb | Polymarket CLOB | Cross-market mispricing · YES/NO spread capture | Kelly criterion · 924 active markets monitored |
| Binary event arb | Kalshi | Spread arbitrage · event correlation | Per-market circuit breakers · $300 max exposure |
| Weather/climate | Polymarket | Data-driven edge · NOAA/NSIDC/NCEI ingestion | 25% fractional Kelly |

**Approach**: I focus on markets where public data creates a systematic edge — weather outcomes, climate indices, macro event correlations. Position sizing follows fractional Kelly criterion. Risk controls include per-market circuit breakers, daily loss limits, and correlation-aware exposure caps.

**Infrastructure**: Real-time WebSocket feeds across 1,848 contract tokens. Event-driven execution architecture. Custom risk engine with configurable thresholds per market type. Live P&L tracking against a PostgreSQL backend.

The execution layer is proprietary. The edge is in the data sourcing and market selection, not latency.

---

## Applied AI & Model Context Protocol (MCP)

### [node4-mcp-servers](https://github.com/sansscott/node4-mcp-servers) — *public*

Self-hosted Model Context Protocol (MCP) server infrastructure on TrueNAS — 20 microservices behind nginx exposing 125 tools to Claude Code and Open WebUI. A production agentic AI toolchain with LLM integration across: Home Assistant, Docker, InfluxDB, PostgreSQL, Reticulum, APRS, Whisper STT, Odoo CRM, Hummingbot, PDF automation, OSHA regulatory lookup, weather safety, contractor registry, and more.

**Stack**: Python · FastAPI · nginx · Docker · MCP SDK
**Topics**: `mcp` `model-context-protocol` `self-hosted` `ai-tools` `agentic-ai` `llm`

### AI & Automation Stack

- **[upwork-ai-agent](https://github.com/sansscott/upwork-ai-agent)** — Semantic job scoring + automated proposal drafting via Claude API and Ollama embeddings (RAG pipeline, nomic-embed-text, pgvector)
- **[obsidian-linker](https://github.com/sansscott/obsidian-linker)** — Semantic auto-tagger for Obsidian using local LLM embeddings (384-dim, Ollama, applied AI on personal knowledge)
- **[whisper-stt-mcp](https://github.com/sansscott/whisper-stt-mcp)** — Self-hosted Whisper speech-to-text MCP server; OpenAI-compatible API for field meeting transcription
- **[claude-mattermost-bridge](https://github.com/sansscott/claude-mattermost-bridge)** — Async Claude Code ↔ Mattermost bridge for remote AI operations

---

## SaaS & Production Infrastructure

### [Sycamore-API](https://github.com/sansscott/Sycamore-API) — *private*

AI-powered multi-brand contractor registry SaaS. Custom JWT auth + magic-link via Resend. Stripe $19/mo payments. Semantic search with nomic-embed-text (384-dim pgvector embeddings via Ollama). 1,370+ seeded contractors across mulch/ROW verticals. Multi-brand routing (sycamore-mulch.com, sycamore-row.com). Ranked #1 on Google within days of launch — production-deployed, revenue-generating.

**Stack**: Next.js 14 · TypeScript · PostgreSQL/pgvector · Ollama · Stripe · Resend · Docker

### Production Infrastructure

Self-managed bare-metal infrastructure running 97+ Docker containers in production on TrueNAS (node4), with Proxmox cold-standby (node6) and automated failover. All access via Cloudflare Zero Trust — no open ports. This is not hobby infrastructure; it runs HVF business operations, live trading strategies, agentic AI toolchains, and mesh networking nodes 24/7.

- **[node6-backup-system](https://github.com/sansscott/node6-backup-system)** — Cold-standby DR on Proxmox. Three-layer health monitoring (ICMP + SSH + API), atomic locking, ZFS replication, tunnel token sync, failover/failback with zero external dependencies
- **Self-healing network**: Cloudflare WARP Zero Trust tunnel, UniFi UDM-SE, auto-failover watchdog scripts, launchd service management
- **Observability**: InfluxDB time-series + Grafana dashboards across all production services

---

## Ham Radio & Mesh Networking Operator

Licensed amateur radio operator. Operate a Reticulum node peered to the global RNS backbone. Built the ATAK CoT bridge (rns-atak-bridge) for situational awareness integration — open source, publicly available. APRS tracking integrated into production MCP toolchain. Actively building toward LoRa RF link integration for true off-grid MANET capability independent of IP backhaul.

---

## Field Context

I run [Hudson Valley Forestry](https://hudsonvalleyforestry.com) — commercial mulching and land clearing across NY and CT. The MANET infrastructure, tactical comms, and field operations tooling I build is used in real production environments: crews in remote terrain, equipment on job sites without cellular. The trading systems manage real capital with live market exposure. The AI toolchain handles real business workflows — CRM intake, competitor intelligence, analytics, lead routing.

This is not theoretical.

---

## Technical Stack

```
Languages:    Python · TypeScript · Rust · Shell · SQL · C# (NinjaTrader)
Frontend:     React · Mapbox GL 3 · Socket.io · HTMX · Vite · Next.js 14
Backend:      FastAPI · Flask · Node.js · Express · Next.js API routes
Infra:        TrueNAS · Docker/Compose · Proxmox · Cloudflare Zero Trust · nginx
Data:         PostgreSQL · pgvector · InfluxDB · Redis · Grafana
Networking:   Reticulum · ATAK CoT · UniFi UDM-SE · APRS · Cloudflare WARP
AI/LLM:       Claude API · Ollama · nomic-embed-text · MCP toolchain · Whisper
Trading:      Polymarket CLOB · Kalshi API · Kelly criterion · CCXT · NinjaTrader
```

---

*Open to applied work in field operations technology, defense infrastructure, prediction markets, distributed systems, and forward-deployed engineering. Reach out: [scott@hudsonvalleyforestry.com](mailto:scott@hudsonvalleyforestry.com)*
