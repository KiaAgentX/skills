# SKILL: ai-agents

**Gives the agent:** ability to design, build and ship autonomous agent systems — runtimes, memory,
tool use, multi-agent orchestration, and agent marketplaces.
**Sources:** AGI/Zenovix Platform ($35K, 120K LOC) · SenP Neural OS ($8K) · xA/Hermes Desk ($14K) ·
0xElon Railway Agent Template ($4K) · Kia-Agent & kiarouter (in dev) · GOLD SNIPER agent skills.

## When to use
- Building an agent that must run persistently (workers, queues, sessions).
- Adding skills/tools/memory to an LLM app.
- Turning a chatbot into a product (dashboard, tenants, billing).

## Core capabilities
1. **Agent runtime loop**: plan → tool call → observe → respond, with persisted session state
   (SQLite/Postgres + JSON event log), timeouts, and retry policy.
2. **Skill system**: loadable `.md` skill files with frontmatter (`name`, `description`), scoped
   toolsets per skill, hot-reload — same pattern as this repository.
3. **Multi-agent topology**: orchestrator + worker pool (arq/Celery/Redis), task handoff via queue,
   idempotent jobs, dead-letter handling (pattern: DropAgentX worker pool).
4. **Channels as adapters**: Telegram (aiogram 3), Discord (discord.py 2.4), web — one core,
   N thin adapters. Never fork the core per channel.
5. **Persistent deployment**: containerized worker + state volume (pattern: 0xElon Railway template).
6. **Agent marketplace**: MCP-compatible skill registry (JSON-RPC 2.0), multi-tenant admin,
   quotas — the DropAgentX v4 "Unity" blueprint in `xpp/hermes-build-manifest.json`.

## Workflows
- **Greenfield agent:** runtime loop → one skill → one channel → tests → containerize → extract skill.
- **Consolidation:** inventory duplicated engines across repos → extract `packages/<engine>` →
  point every repo at it (Law L4).
- **Safety:** LLM output always schema-validated (Pydantic/zod); tools are allow-listed;
  destructive actions require confirmation tokens.

## Quality bar
- Deterministic replay tests for the agent loop (mock LLM), ≥60% backend coverage.
- Every agent ships with a `Limitations` README section (hallucination boundaries, context limits).
- Secrets via env only; session data never logged raw.

## Price anchor
Single runtime $4–7K · Multi-agent platform $14–28K · Marketplace $26–35K → see `PRICING.md` §1.
