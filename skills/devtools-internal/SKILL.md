# SKILL: devtools-internal

**Gives the agent:** internal tools people actually keep using — editors, studios, dashboards,
valuation engines, prompt managers — local-first, keyboard-driven, honest UI.
**Sources:** SC Studio ($7K, 600KB single file) · DropAgentX Valuation Dashboard ($9K) ·
Neon Prompt Studio ($3.5K) · Neon PromptPad 3D ($4K) · Zenovix Chat Widget ($7K) ·
antigravity simulators ($5.5K/6.5K) · craft Gemini Studio ($6K).

## When to use
- An internal workflow exists in spreadsheets/heads → make it a tool.
- Pricing/valuation engines, admin consoles, editors, management studios.
- Must run locally (privacy) with optional sync.

## Core capabilities
1. **Single-file app architecture**: state store + render diff + persistence layer in one HTML —
   SC Studio proves 600KB can hold a full requirements-engineering studio.
2. **Editor-class UX**: command palette (Ctrl+K), autosave, undo stack, keyboard shortcuts,
   split panes, dirty-state guards — same muscle memory as professional tools.
3. **Valuation/analysis engines**: rule-based scoring (LOC, complexity, test density, docs) →
   USD estimate, per-file breakdown, interactive sandbox to tweak weights (DropAgentX Valuation).
4. **Prompt studios**: categories, tags, variable interpolation `{{var}}`, run history, import/export,
   offline PWA persistence (Neon tools: 124 curated prompts).
5. **Embeddable widgets**: chat/support widget with multi-page front + Python backend + CI,
   drop-in script tag (Zenovix pattern), theme via CSS variables.
6. **Mission-control dashboards**: live telemetry simulation, classified archives, calculators —
   fictional-science styling with real state machines (antigravity pattern).
7. **Three-mode studios**: playground (params), workbench (collaborative doc), factory (schema→dataset
   →CSV) — one shell, three workflows (craft pattern).

## Workflows
- **Tool MVP:** shadow the manual workflow → single screen with one killer shortcut → autosave → share.
- **Scoring engine:** define weighted rules → backtest against known values → interactive sandbox → export.
- **Adoption check:** if the user needs a manual, cut scope until they don't.

## Quality bar
- Zero-setup: open file / one command → working tool (no accounts for local mode).
- Every destructive action undoable; every export round-trips (import = export format).
- A11y: full keyboard path, visible focus, ARIA on dynamic panels.

## Price anchor
Single tool $2.5–4K · Studio $6–8K · Dashboard/engine $7–9K → `PRICING.md` §8.
