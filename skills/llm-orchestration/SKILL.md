# SKILL: llm-orchestration

**Gives the agent:** multi-provider LLM routing with fallbacks, streaming, cost control and
OpenAI-compatible gateways — one API in front of many models.
**Sources:** NEXUS Gateway ($4.5K) · NEXOS/key UI ($3.5K) · NOVA Platform ($9K) ·
DropAgentX LLM Gateway Monorepo ($16K) · 9Router reference guide · craft Gemini playground ($6K).

## When to use
- App must survive provider outages and price changes.
- One API key/end-point for many providers (OpenAI-compatible surface).
- Cost ceilings, per-tenant quotas, usage metering.

## Core capabilities
1. **Router core**: provider adapters (OpenAI, Anthropic, Gemini, Groq, DeepSeek, OpenRouter, Ollama…),
   unified request/response types, streaming passthrough (SSE), token & cost accounting per call.
2. **Three-layer fallback** (from 9Router): primary → cheapest-capable → last-resort offline;
   per-model health scores; circuit breaker with cooldown.
3. **Gateway surface**: `/v1/chat/completions` compatible endpoint so any existing SDK works unchanged.
4. **Credential vault**: keys stored encrypted at rest (Fernet/age), never in repo, rotation endpoint.
5. **Prompt cache & context trimming**: dedupe system prompts, cache by hash (Redis), trim history
   to budget before dispatch — measurable token savings.
6. **Model fleet admin**: capability matrix (vision/tools/json-mode), price table, enable/disable per tenant.
7. **Chat UI**: streaming tokens, history, tool/thinking traces (pattern: NEXUS playground).

## Workflows
- **Add a provider:** adapter (~200 LOC) → capability entry → price entry → chaos test (kill switch).
- **Cost incident:** meter report → route shifts to cheaper model → alert threshold added.
- **Gateway cutover:** run gateway in shadow mode, diff responses, then flip base URL.

## Quality bar
- Contract tests per adapter against recorded fixtures (no live calls in CI).
- Fallback paths covered by tests simulating 429/5xx/timeouts.
- Streaming must not buffer (chunk-level latency asserted).

## Price anchor
Router $4.5–7K · Full gateway $7–12K · Mesh + admin $12–18K → `PRICING.md` §2.
