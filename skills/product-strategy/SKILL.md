# SKILL: product-strategy

**Gives the agent:** how Kia decides *what* to build — the 8 Laws, staircase versioning,
consolidation audits, architecture & roadmap documents investors take seriously.
**Sources:** xpp Laws (L1–L8) · DropAgentX Architecture & Roadmap docs · Hermes Company Structure ·
the portfolio's own Roadmap (10 predicted projects, $191K pipeline) · observed evolution:
v1 single-file → v2 feed → v3 monorepo → v4 Unity.

## When to use
- Choosing between a new repo vs. versioning an existing one.
- Writing architecture/roadmap/company documents.
- Auditing N overlapping codebases before quoting a consolidation.

## Core capabilities
1. **Law framework (memorize):**
   - L1 staircase versioning: v1→v2→v3, **v4 = consolidation**
   - L2 simulate first, real later
   - L3 brand-book companion for big products
   - L4 scattered engines → one package
   - L5 3D brain = signature UI
   - L6 Persian RTL twist for every idea (once)
   - L7 study third-party repo → recreate your own
   - L8 extract a skill `.md` after every demo
2. **Pattern detection from codebases:** count duplicated engines, version suffixes, README promises
   vs. test reality → predict the honest next version (this is how the Roadmap's 10 predictions
   were derived: observed pattern → prediction → stack → estimate).
3. **Consolidation audit (deliverable):** inventory → overlap matrix → target architecture →
   package extraction plan → migration order → risk register. Output = one HTML doc + one MD.
4. **Architecture document:** services, data flows, gateways, deployment topology on one visual page
   (single-file HTML, SC/DropAgentX style).
5. **Roadmap document:** phases with exit criteria, current traction, outlook, honest limitations —
   investor-ready in Persian or English.
6. **Estimation method:** market-equivalent $ = f(LOC band, module count, integration risk,
   consolidation debt); anchor to shipped comparables from `PROJECTS.md`, never vibes.
7. **Naming/version voice:** `<Product> v<X>.<Y> "<Codename>"` (e.g., GQR-v4 "Live",
   Xmarket v0.2 "Mainnet Preview") — codename states the leap, not marketing filler.

## Workflows
- **What next?** map repo history → apply L1 → if 3+ forks exist → consolidation wins.
- **Quote a rebuild:** overlap matrix → which modules merge → price via `PRICING.md` → ±15% band.
- **Document pack:** architecture + roadmap + structure chart as single-file HTMLs (§10 pricing).

## Quality bar
- Predictions cite observed evidence (file names, versions, test counts) — no fantasy.
- Documents use spec-sheet voice: tables, mono metadata, honest Limitations section.
- Every strategy ends with an executable first slice (ship-first, per SOUL).

## Price anchor
Architecture $1.2K · Roadmap $1K · Structure $1K · Consolidation audit $3K → `PRICING.md` §10.
