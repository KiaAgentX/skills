# PRICING.md — Itemized by Module

All figures are **market-equivalent build prices** (agency rates for the same scope), USD.
Ranges exist because module cost depends on consolidation scope (how many legacy systems merge)
and depth (single module vs. full platform). Anchors come from the 59 shipped projects ($462K total).

## 1. ai-agents — Agent Systems

| Deliverable | Includes | Price |
|---|---|---|
| Agent runtime (single) | tool calling, memory, skills, one LLM provider | $4,000 – $7,000 |
| Multi-agent platform | orchestrator + workers + task queue + dashboard | $14,000 – $28,000 |
| Agent marketplace | MCP-compatible skill store, multi-tenant admin, billing | $26,000 – $35,000 |
| Agent channel pack (add-on) | Telegram / Discord / Slack / WhatsApp adapter | +$2,500 each |

*Anchors: Zenovix Platform $35K · SenP $8K · xA/Hermes Desk $14K · Kia-Agent (in dev).*

## 2. llm-orchestration — Routing & Gateways

| Deliverable | Includes | Price |
|---|---|---|
| Provider router | 3–5 providers, fallback chain, streaming, cost meter | $4,500 – $7,000 |
| OpenAI-compatible gateway | credential vault, model fleet, chat playground | $7,000 – $12,000 |
| Mesh + admin portal | 10+ providers, RAG, quotas/billing, Next.js admin | $12,000 – $18,000 |
| Token-optimization audit (add-on) | prompt cache, context trimming, savings report | +$2,000 |

*Anchors: NEXUS Gateway $4.5K · NOVA $9K · DropAgentX gateway monorepo $16K · 9Router guide.*

## 3. trading-quant — Trading Systems

| Deliverable | Includes | Price |
|---|---|---|
| Data & backtest module | MT5/CSV ingestion, indicators, Monte Carlo backtest | $6,000 – $9,000 |
| RL trading agent | PPO training, paper execution, risk manager | $10,000 – $16,000 |
| Full quant platform | live connector (paper-first), arena, oracle, trade log DB | $16,000 – $22,000 |
| Live-mode unlock (add-on) | explicit env-gated live trading + kill switch | +$3,000 |

*Anchors: GQR-v3 $9K · fly-gold-trader PRO $22K · mt5-fetcher $5K · GOLD SNIPER skills.*

## 4. ecommerce-marketplace — Commerce

| Deliverable | Includes | Price |
|---|---|---|
| Telegram commerce bot | catalog, cart, wallets, referrals, mini-app front | $6,500 – $10,000 |
| Marketplace platform | sellers, listings, rewards, analytics, moderation | $10,000 – $16,000 |
| Launchpad (Web3) | minting, on-chain leaderboard, wallet adapter | $9,000 – $14,000 |
| Full monorepo consolidation | bots + LLM router + billing + web panel | $16,000 – $18,000 |

*Anchors: DropAgentX Marketplace $18K · DropAgentX Monorepo $16K · Ghost $6.5K · Xmarket v0.1 $6.5K.*

## 5. web3d-gpu — Games & Immersive 3D

| Deliverable | Includes | Price |
|---|---|---|
| Single-file 3D experience | Three.js hero/scene, responsive, offline | $2,500 – $5,000 |
| Vite WebGL app/UI | scenes, telemetry, Tailwind design system | $5,500 – $9,000 |
| Browser game (full) | game loop, economy, assets, save system | $18,000 – $30,000 |
| Custom GPU engine (add-on) | WebGPU/WGSL or C++/WASM kernels | +$8,000 |

*Anchors: Tidewater $30K · WaterCuda $20K · win12/W12 $6.5K/7K · 3DMIND $7.5K · Fable Berger $2.5K.*

## 6. persian-rtl-accounting — RTL Fintech

| Deliverable | Includes | Price |
|---|---|---|
| Audit toolkit (static) | trial balance, working papers, statements — PWA | $6,000 |
| Academy + mini-apps | sessions, progress, quizzes, 8 practice apps | $9,000 |
| Full accounting suite | 24 sessions, ledgers, trading hub, assistant | $25,000 |
| SaaS module (Next.js + DB) | multi-user, tax forms, legal templates | $35,000 |

*Anchors: accounting $6K · khanehesabdari $9K · Hesaban $25K · Hesabdari Pro (roadmap) $35K.*

## 7. brand-content — Brand & Content

| Deliverable | Includes | Price |
|---|---|---|
| Cinematic one-page site | scroll storytelling, art-directed motion | $3,000 – $5,000 |
| Interactive brand book | palette, type, voice, 3D hero, logo rules | $3,000 |
| Long-form interactive article | embedded demos, calculators, quizzes | $800 – $1,500 |
| Full guide/documentation site | multi-page reference, 3D visuals | $1,500 – $2,500 |

*Anchors: FISHKAL sites $3K–5K · DropAgentX Brand $3K · AI Agent Guide $800 · 9Router/Railway guides $1.5K.*

## 8. devtools-internal — Internal Tools

| Deliverable | Includes | Price |
|---|---|---|
| Single-page internal tool | local-first, zero-dep, keyboard-driven | $2,500 – $4,000 |
| Dashboard + analytics | charts, valuation/pricing engine, exports | $7,000 – $9,000 |
| Studio (editor-class) | editor UX, persistence, presets, share | $6,000 – $8,000 |

*Anchors: SC Studio $7K · DropAgentX Valuation $9K · Neon Prompt Studio $3.5K · PromptPad 3D $4K.*

## 9. infra-deploy — Infrastructure

| Deliverable | Includes | Price |
|---|---|---|
| Docker packaging | multi-service compose, env discipline, healthchecks | $2,000 – $3,500 |
| PaaS deploy pipeline | Railway/Fly configs, zero-downtime, preview envs | $3,000 – $5,000 |
| CI/CD + quality gates | tests, coverage thresholds, secret scanning, CD | $4,000 – $8,000 |

*Anchors: 0xElon Railway template $4K · Zenovix CI · DropAgentXBot Docker $12K (bundle).*

## 10. product-strategy — Strategy & Docs

| Deliverable | Includes | Price |
|---|---|---|
| Architecture document | services, data flows, topology, one visual page | $1,200 |
| Roadmap / investor doc | phases, traction, outlook | $1,000 |
| Company structure chart | entity, product lines, operating units | $1,000 |
| Consolidation audit (3 repos → 1) | mapping, migration plan, package extraction | $3,000 |

*Anchors: DropAgentX Architecture/Roadmap, Hermes Company Structure (Docs & Strategy section).*

## Rules of quotation

1. Never quote below the module floor — scope creep is priced by adding modules, not renegotiating.
2. Three-module bundles get −10%; full-platform contracts (≥5 modules) get −15%.
3. Every quote lists deliverables, acceptance criteria (from AGENTS.md), and the source projects
   from `PROJECTS.md` proving the capability exists.
4. Roadmap projects (portfolio `Roadmap` section) are quoted at their published estimate ±15%.

## 11. procedural-canvas-game � Procedural Canvas Experiences

| Deliverable | Includes | Price |
|---|---|---|
| Interactive canvas scene | Noise/FBM water & sky, bezier hero paths, particle pools, procedural audio | $2,500 � $5,000 |
| Full single-file game | Loop, HUD, achievements, i18n (13 langs), device caps, 60fps budget | $5,000 � $12,000 |

*Anchor: FISHKAL Deep Catch single-file edition (113 render/game functions, zero assets).*

---
Updated: 2026-10-04 � includes the procedural-canvas-game module extracted from FISHKAL Deep Catch.
