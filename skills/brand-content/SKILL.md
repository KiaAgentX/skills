# SKILL: brand-content

**Gives the agent:** cinematic brand websites, interactive brand books, and long-form interactive
content that converts — art-directed motion, not template layouts.
**Sources:** FISHKAL Deep Catch ($5K) + Launch Site ($3K) + single-file edition ($4.5K) ·
DropAgentX Brand System ($3K) · ImX 3D Landing · AI Agent Guide article ($800) ·
9Router & DropRail guides ($1.5K each).

## When to use
- Product launch page with scroll storytelling.
- Brand identity delivered as an interactive artifact (not a PDF).
- Technical content that embeds live demos/calculators/quizzes.

## Core capabilities
1. **Scroll narrative**: pinned sections, layered parallax, chapter markers, progress-aware motion
   (FISHKAL: coast → surface → deep with color/pressure changing per chapter).
2. **Interactive brand book**: single HTML with name story, palette (with copy-hex), type scale,
   voice do/don't, logo rules, and a Three.js hero (DropAgentX pattern — particle-X identity).
3. **Interactive articles**: embedded widgets (cost calculator, level quiz, feature puzzle),
   sticky TOC, reading-time discipline, SEO meta + OG image (patterns: AI Agent Guide, guides).
4. **Countdown/launch mechanics**: pre-launch waitlist pages, launch-control private pages (fishkalv1).
5. **Design tokens as deliverable**: dark base (#06060e), accent spectrum, mono metadata voice —
   shipped as CSS variables the client can reuse across products.
6. **Single-file discipline**: everything inlined, CDN only with graceful guards (`typeof THREE`),
   open-in-browser deploy (Law: zero friction).

## Workflows
- **Brand book:** discovery → palette/type from client constraints → sections → hero scene → one-file export.
- **Launch page:** narrative outline (3–5 chapters) → art direction frames → motion pass → perf pass → CTA.
- **Article:** outline → interactive element per section → publish → measure reading completion.

## Quality bar
- Every motion respects `prefers-reduced-motion`; content readable with JS off where feasible.
- Load < 2s on 4G (target: single file < 1MB).
- Copy written in the site's language — English for international, Persian for local.

## Price anchor
Article $800–1.5K · Guide site $1.5–2.5K · Brand book $3K · Cinematic site $3–5K → `PRICING.md` §7.
