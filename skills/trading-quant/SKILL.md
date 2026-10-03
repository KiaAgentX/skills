# SKILL: trading-quant

**Gives the agent:** algorithmic trading systems — data pipelines, backtesting, RL agents, risk
management, MT5 integration — always **paper-first**.
**Sources:** fly-gold-Trader PRO ($22K, 166K-neuron net) · GQR-v1/v2/v3 series ($10K/6K/9K) ·
SOL/mt5-fetcher ($5K) · TypeSafe Jev chat · GOLD SNIPER Skills ($2.5K) · DOGE simulators ($8K).

## When to use
- Market data ingestion (MT5/CSV/exchange feeds), indicators, backtests.
- RL/ML strategy research with reproducible training.
- A trading product that must never risk real money by accident.

## Core capabilities
1. **Data layer**: MT5 package fetch (symbol/timeframe/date), synthetic demo mode when broker is
   unavailable, parquet/CSV storage, gap detection (pattern: mt5-fetcher).
2. **Indicators**: 14+ TradingView-compatible indicators computed in TS or Python (RSI, MACD, ATR,
   Supertrend, Ichimoku…), unit-tested against reference values.
3. **Backtesting**: event-driven engine, Monte Carlo resampling, slippage/fee model, equity curves,
   Sharpe/max-drawdown report (pattern: GQR backtester).
4. **RL agent**: observation = features + position state; PPO/FusedActorCritic; train/paper/eval
   modes; checkpoints; cross-symbol fusion (XAUUSD + EURUSD pattern from GOLD SNIPER).
5. **Risk manager**: position sizing (fractional Kelly capped), daily loss limit, max drawdown kill,
   per-trade stop — hard-stops enforced in code, not prompts.
6. **Execution adapters**: MT5 terminal bridge, paper broker, exchange connectors behind ONE
   `ExecutionGateway` interface (paper default; live requires `LIVE_TRADING_ENABLED=true`).
7. **Ensembles**: 7-strategy voting with pattern playbook (20 patterns) and confidence gates.

## Workflows
- **New strategy:** define pattern → backtest → walk-forward → paper 2 weeks → live flag (never before).
- **Model research:** data audit → feature store → train → regime check → paper.
- **Productize:** engine → API → arena/dashboard → trade log DB → oracle (LLM explainability).

## Quality bar
- **No real money by default.** Live mode double-gated (env + explicit CLI confirm).
- Backtests must resist lookahead bias — enforced by shifted-index tests.
- Every run reproducible from seed + config hash.

## Price anchor
Data/backtest $6–9K · RL agent $10–16K · Full platform $16–22K → `PRICING.md` §3.
