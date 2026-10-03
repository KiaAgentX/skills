# SKILL: infra-deploy

**Gives the agent:** shipping and keeping systems alive — Docker packaging, PaaS deploys, CI/CD
with quality gates, and resumable operations on bad networks.
**Sources:** 0xElon Railway Template ($4K) · DropAgentXBot/DropAgentXmain Docker stacks ($12K/16K) ·
Zenovix GitHub Actions CI · fly-gold-trader compose · portfolio pipeline itself
(chunked pushes, secret redaction, resume-on-failure).

## When to use
- Turning a repo into a deployed service (VPS, Railway, Fly, GitHub Pages).
- CI that blocks bad releases (tests, coverage, secret scan).
- Operating over slow/unreliable connections (resumable uploads, batch limits).

## Core capabilities
1. **Docker discipline**: multi-stage builds (builder → slim runtime), non-root user, healthchecks,
   `.dockerignore`, compose files per environment; secrets via env/file mount only.
2. **PaaS patterns**: `railway.json`/`Procfile`, persistent volume for state (agent workers),
   worker + web as separate services, one-click template repo (0xElon).
3. **CI/CD gates**: GitHub Actions — lint → unit → coverage threshold (60% backend) → build →
   secret scan → deploy; branch protection; conventional commits.
4. **Static publishing**: GitHub Pages via chunked resumable pushes (≤4–9MB commits with retry —
   proven on a 134MB site over 408-prone connections), `gh-pages` branch, relative base paths.
5. **Secret hygiene**: pre-commit scan for provider key patterns (gsk_, sk-, ghp_, AKIA, AIza,
   telegram tokens…), redact-then-rotate runbook — taken from the leaked-Groq incident response.
6. **Rate-limit citizenship**: serial API calls, ≥1s between mutations, exponential backoff on
   403/429 secondary limits, batch caps (GitHub rules — protects accounts from bans).
7. **Observability basics**: structured logs, exit codes that mean something, resume/checkpoint
   files (`.checkpoint.json`) for long jobs.

## Workflows
- **Repo → production:** containerize → local compose smoke → staging env → CI green → prod with rollback tag.
- **Pages site:** build → secret scan → chunked push → post-deploy link verification.
- **Recovery:** failed job → read log → resume from checkpoint → never force-push history.

## Quality bar
- Image < 300MB runtime where possible; builds cache-friendly (deps layer first).
- No secret ever touches the repo (scan before every commit — AGENTS.md rule 4).
- Deploys verifiable: post-deploy HTTP smoke checks with explicit expected status.

## Price anchor
Docker $2–3.5K · PaaS pipeline $3–5K · CI/CD + gates $4–8K → `PRICING.md` §9.
