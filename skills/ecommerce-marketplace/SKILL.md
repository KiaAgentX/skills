# SKILL: ecommerce-marketplace

**Gives the agent:** commerce products end-to-end — Telegram storefronts, wallets, referrals,
digital-goods marketplaces and Web3 launchpads.
**Sources:** DropAgentX Marketplace v1.0 ($18K, 38K LOC) · DropAgentX Bot ($12K) ·
DropAgentX Monorepo ($16K) · FISHKAL Ecosystem ($28K) · GhostVault ($6.5K) · Xmarket v0.1 ($6.5K).

## When to use
- Selling inside Telegram (mini-app + bot + payments).
- Digital product delivery with referrals/rewards.
- Marketplace with sellers, listings, escrow-like flows, on-chain touches.

## Core capabilities
1. **Telegram commerce bot**: catalog, cart, checkout, `/links` command hub with glob/regex
   filtering, referral codes, gamification hooks (pattern: DropAgentX Bot).
2. **Mini-app front**: PWA served into Telegram WebApp, dark RTL-first UI, deep-link routing.
3. **Wallet ledger**: double-entry in-app wallets, top-up/withdraw audit trail, idempotent
   transactions — DB constraints guard every balance change.
4. **Digital delivery**: signed expiring download links, license keys, buyer/seller ledgers
   (pattern: GhostVault simulated USDC/Solana settlement).
5. **Referral & rewards**: multi-tier percentages, anti-self-referral rules, payout queue.
6. **Launchpad (Web3)**: listings, upvotes, mint flows — devnet/testnet default; mainnet behind
   `MAINNET_ENABLED=true` (Law L2: Xmarket v0.1 simulated → v0.2 real).
7. **FISHKAL ecosystem pattern**: Turborepo with site + game + mini-app + shop + analytics sharing
   types and DB — monorepo over micro-repos (Law L1).

## Workflows
- **Bot MVP:** catalog import → cart → manual payment confirm → iterate on auto-payments.
- **Marketplace launch:** seller onboarding → listing schema → escrow rules → dispute path → rewards.
- **Consolidation:** three bots → one LLM router + shared core (DropAgentXmain pattern).

## Quality bar
- Money math tested with property tests (sum of ledger = 0 always).
- Webhook handlers idempotent (duplicate delivery safe).
- RTL + LTR both verified; prices formatted per-locale.

## Price anchor
Bot $6.5–10K · Marketplace $10–16K · Launchpad $9–14K · Monorepo consolidation $16–18K → `PRICING.md` §4.
