Doc 04: The AI System & Rules Engine
Architecture, Strategy Execution, and Safety Protocols
Version 6.0 — Effective Feb 2026
1. Three-Layer System Architecture
The YieldLoop AI operates through three distinct layers that work in a strict sequence to ensure user intent is translated into safe on-chain actions.
 * The Communication Layer (The "Bridge"): Conducts the initial goal-setting conversation, translating your plain-English objectives into a specific strategy tier.
 * The Optimization Model (The "Navigator"): Uses machine learning (XGBoost-class) to calculate precise allocation weights across the 8-token basket and sets autonomous stop-loss/take-profit thresholds.
 * The Safety Layer (The "Hull"): A deterministic rules engine that validates every recommendation against the protocol's Invariables; it has the absolute power to veto any action that breaches safety limits.
2. Strategy Eligibility & Execution
Strategy access is vault-driven, meaning there are no protocol-wide wealth gates.
 * Individual Assessment: The AI evaluates each vault based on size, risk tier, and current market conditions to determine the best strategy mix (e.g., Staking, Lending, LP, or Arb).
 * Autonomous Stop-Loss: When a position reaches its drawdown threshold, the AI issues an immediate sell order without waiting for user confirmation to prevent further loss.
 * Best Execution: For all trades, the AI compares prices between PancakeSwap and BiSwap to route your order to the exchange offering the best price.
3. V6.0 Dynamic Non-Stable Cap (30%–50%)
The Safety Layer enforces a strict stablecoin floor to ensure capital protection.
 * Default Safe Harbor: The standard cap for non-stable assets (BTC, ETH, BNB, XRP, SOL) is 30%.
 * Expansion Logic: In V6.0, the AI can recommend increasing this cap to 50% for Growth-tier vaults if market volatility is low and vault health is high.
 * The Self-Correction Flag: If the system detects a market move greater than 10% within a one-hour window, the Safety Layer automatically forces the vault back to the 30% cap to preserve capital.
4. Anomaly Explanations & Transparency
YieldLoop graduates from a simple engine to an active UX partner by explaining non-routine events.
 * Proactive Notifications: If a stop-loss fires or the Safety Layer vetoes an AI recommendation, the Communication Layer generates a plain-language explanation of what happened and why.
 * Narrative Summaries: At each epoch close, you receive a human-readable interpretation of your vault's performance, highlighting which strategies were the strongest performers.
5. Authority Matrix: What the AI Cannot Do
To maintain user sovereignty, the AI is strictly prohibited from several actions:
 * Cannot raise the protocol fee or a vault's effective rate.
 * Cannot exceed the hard-coded 30% (or dynamic 50%) non-stable cap.
 * Cannot add or remove tokens from the whitelist (this is for governance only).
 * Cannot access, move, or freeze your funds directly—it can only manage allocations within your vault.
6. Failure Modes & Redundancy
 * AI Fallback: If the primary Communication Layer (Gemini) is unavailable, the system automatically falls back to secondary models (Claude or GPT) to ensure continuity.
 * Safety Default: If the Optimization Model fails to produce a valid recommendation, the Safety Layer defaults the vault to its last-known safe parameters.

