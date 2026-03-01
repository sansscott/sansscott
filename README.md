# Scott Sans

**Builder. Operator. Field engineer.**

I design and deploy systems that work in the real world — off-grid mesh networks, live trading infrastructure, AI-powered SaaS platforms, and tactical comms tools for crews working where there is no cell signal.

---

## Open MANET Work

Mobile Ad-hoc Networks are the backbone of resilient field operations. I build and operate open-source MANET infrastructure using Reticulum Network Stack — a cryptographically addressed, transport-agnostic mesh protocol designed to work over LoRa, TCP/IP, serial, and RF links with zero infrastructure dependency.

### [rns-atak-bridge](https://github.com/sansscott/rns-atak-bridge) — *public*
Bridges Reticulum mesh peers into ATAK Cursor-on-Target (CoT) events. Makes off-grid mesh nodes visible as SA tracks in ATAK, iTAK, WinTAK, and TAK Server in real time. No internet. No server. Just mesh.

**Stack**: Python · Reticulum RNS · ATAK CoT XML · UDP multicast  
**Use case**: DoD/government situational awareness over zero-infrastructure mesh

### [THR-Manet](https://github.com/sansscott/THR-Manet) — *private*
Full MANET stack for HVF field operations — forestry crews working in dense canopy with no cell coverage. Reticulum transport node (peered to global RNS backbone), NomadNet messaging, and MCP tool integration for remote mesh management.

**Interfaces**: AutoInterface (LAN) · TCP backbone peering · LoRa (planned) · Cloudflare Zero Trust tunnel  
**Node identity**: af60a4f4863c9bff05a9871359d67e1f

### [Sycamore Mesh](https://github.com/sansscott/sycamore-mesh) — *private*
Voice-first tactical comms and live tracking dashboard for ROW/pipeline/forestry field crews. Real-time node positions over WebSocket, Mapbox GL 3 terrain rendering, push-to-talk coordination. Built for crews who cannot rely on cellular.

**Stack**: Node.js · Socket.io · React · Mapbox GL 3 · Zustand · Docker · Cloudflare Zero Trust

---

## Production Infrastructure

Self-hosted infrastructure running 97+ Docker containers on TrueNAS (node4), Proxmox cold-standby (node6), and Mac Studio — all behind Cloudflare Zero Trust with no open ports.

### [node4-mcp-servers](https://github.com/sansscott/node4-mcp-servers) — *public*
Self-hosted MCP (Model Context Protocol) server infrastructure — 20 microservices behind nginx exposing 125 tools to Claude Code and Open WebUI. Services span Home Assistant, Docker, InfluxDB, PostgreSQL, Reticulum, APRS, Whisper STT, Odoo, Hummingbot, PDF automation, OSHA lookup, weather safety, and more.

### [node6-backup-system](https://github.com/sansscott/node6-backup-system) — *private*
Automated cold-standby DR on Proxmox. Three-layer health monitoring (ICMP + SSH + API), atomic locking, ZFS replication, tunnel token sync, and failover/failback scripts. No external dependencies.

### [compintel-mcp](https://github.com/sansscott/compintel-mcp) — *public*
Daily competitive intelligence scraping and analysis for the forestry mulching market in Hudson Valley NY and CT. MCP tool interface for Claude Code integration.

---

## Trading & Market Systems

Live and paper prediction market bots across Polymarket and Kalshi, plus a Rust latency-arb engine.

| Repo | Market | Status | Notes |
|------|--------|--------|-------|
| [aetherclaw](https://github.com/sansscott/aetherclaw) | Polymarket YES/NO | Live | 924 markets, 1848 WS tokens, Kelly sizing |
| [kalshi-arb](https://github.com/sansscott/kalshi-arb) | Kalshi binary | Live | Per-market circuit breakers,  max exposure |
| [stormclaw](https://github.com/sansscott/stormclaw) | Polymarket weather | Paper | NOAA + NSIDC + NCEI data ingestion |
| [polybot](https://github.com/sansscott/polybot) | Polymarket BTC | Dev | Rust, low-latency execution |

---

## AI & Automation

- **[upwork-ai-agent](https://github.com/sansscott/upwork-ai-agent)** — Semantic job scoring + automated proposal drafting via Claude API and Ollama embeddings
- **[obsidian-linker](https://github.com/sansscott/obsidian-linker)** — Semantic auto-tagger for Obsidian vaults using nomic-embed-text (384-dim) via local Ollama
- **[whisper-stt-mcp](https://github.com/sansscott/whisper-stt-mcp)** — Self-hosted Whisper STT MCP server for construction site meeting transcription
- **[claude-mattermost-bridge](https://github.com/sansscott/claude-mattermost-bridge)** — Claude Code ↔ Mattermost bridge for async AI ops

---

## Field Context

I run [Hudson Valley Forestry](https://hudsonvalleyforestry.com) — commercial mulching and land clearing across NY and CT. The mesh networking, tactical comms, and field operations tooling I build is used in actual production environments: crews in remote terrain, equipment on job sites, coordination without cell coverage. This is not theoretical infrastructure.

---

## Stack at a Glance



---

*Open to applied work in field operations, defense infrastructure, prediction markets, and distributed systems. Reach out via [scott@hudsonvalleyforestry.com](mailto:scott@hudsonvalleyforestry.com)*
