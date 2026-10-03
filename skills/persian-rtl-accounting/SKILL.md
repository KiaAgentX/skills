# SKILL: persian-rtl-accounting

**Gives the agent:** Persian-language (RTL) financial products — audit toolkits, accounting suites,
learning academies — offline-first, zero-dependency, legally aware.
**Sources:** Hesaban Suite v3.3 ($25K, 69K LOC) · accounting Audit Toolkit ($6K, 21K LOC) ·
Khaneh Hesabdari Academy ($9K, 36K LOC) · Hesabdari Pro (roadmap target $35K).

## When to use
- Any product for Iranian/Gulf users: invoices, ledgers, trial balance, financial statements.
- Full RTL interfaces that must feel native (not mirrored afterthoughts).
- Offline-first tools (no server, no CDN dependency) for accountants with unreliable networks.

## Core capabilities
1. **Domain core**: chart of accounts, journal entries (debit/credit enforced), trial balance,
   working papers, balance sheet / income / cash-flow statements — formulas unit-tested against
   hand-worked fixtures.
2. **RTL-first UI**: `dir="rtl"`, logical CSS properties (inline-start/end), Vazirmatn font,
   Persian numerals with locale toggle, mirrored iconography rules.
3. **Zero-dependency architecture**: single-file HTML modules, localStorage persistence,
   PWA service worker for offline — the house style for all three shipped suites.
4. **Audit workflows**: tie-out checks, sampling tables, anomaly flags (balance mismatches,
   round-number clusters), evidence trail per working-paper line.
5. **Educational layer**: 24-session structured paths, progress tracking, quizzes with scoring,
   mini-apps per topic (invoice, payroll, ledger, inventory, budget, CRM) — academy pattern.
6. **Legal/tax templates** (Hesabdari Pro target): invoice formats aligned to Iranian tax rules,
   VAT lines, salary slip with insurance tiers — always versioned as `rule-year`.
7. **Assistant**: rule-based NOVA-style helper answering accounting questions from local docs
   (works offline; LLM optional).

## Workflows
- **New module:** domain spec with accountant → fixture-based tests → RTL UI → offline audit → release.
- **Suite consolidation:** three repos → one package + one design system (Law L1/L4 → Hesabdari Pro).
- **Client demo:** import sample book → auto trial-balance → export PDF/Excel.

## Quality bar
- Every financial formula has a golden fixture test; rounding rules explicit (rial vs. toman).
- Works with JS disabled? No — but works fully offline after first load (PWA verified).
- Full RTL visual QA (no mixed-direction glitches in tables).

## Price anchor
Static toolkit $6K · Academy $9K · Full suite $25K · SaaS $35K → `PRICING.md` §6.
