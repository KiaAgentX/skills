# AGENTS.md — Operating Contract

An agent that has read `SOUL.md` must obey this contract when working with Kia's knowledge.

## The ritual

```
1. Read SOUL.md        → personality + 8 Laws + quality bar
2. Read this file      → hard rules of engagement
3. Load only the skill modules the task needs (skills/*/SKILL.md)
4. Consult PROJECTS.md → cite the source project(s) behind every decision
5. Consult PRICING.md  → quote per module before starting paid work
```

## Hard rules

1. **Consolidate before adding.** If a request would create a 4th copy of an engine, extract a package instead.
2. **Ship a slice.** Every session must end with something runnable (even if ugly).
3. **Sim by default.** Any financial/blockchain integration ships in paper/testnet mode unless
   `LIVE_TRADING_ENABLED=true` / `MAINNET_ENABLED=true` is explicitly set by the user.
4. **Secret scan before commit.** Never commit keys, tokens, passwords, or `.env` files.
5. **Test before "done".** Backend tests ≥60% lines; frontend verified in a real DOM.
6. **Honest docs.** README with install/run/architecture/limitations. No vapor claims.
7. **Bilingual by default.** Persian products are full RTL; portfolio/marketing copy is English.
8. **Brand books for big products.** Flagship releases get a single-file HTML brand asset.
9. **Extract a skill after each deliverable.** Append learnings to the relevant `skills/*/SKILL.md`.
10. **Price per module.** Use PRICING.md ranges; never invent numbers.

## Session output template

```markdown
## Session: <task>
- Shipped: <runnable artifact + command>
- Projects referenced: <from PROJECTS.md>
- Skills used: <module ids>
- Limitations: <honest>
- Next staircase step: <vN+1 or consolidation>
```

## Escalation

Ask the user (do not guess) when:
- A change touches real money, mainnet, or private user data.
- A module estimate falls outside PRICING.md ranges.
- Two laws conflict (e.g., speed vs. consolidation) — state the tradeoff in one paragraph.
