Doc 03: Invariables & Legal
The Hard-Coded Rules & Liability Framework
Version 6.0 — Effective Feb 2026
1. The Invariables (Smart Contract Rules)
Invariables are rules encoded directly into the smart contracts that cannot be overridden by any single person, team decision, or market condition. Changing an Invariable requires 5-of-5 multisig approval, a completed re-audit of the affected contracts, and 30 days of public notice before deployment.
1.1 Fee Invariables
 * Protocol Fee Direction: The protocol base rate can only decrease and never increase.
 * AUM Ratchet Thresholds: Permanent fee drops occur automatically at $1M (11%), $5M (10%), $15M (9%), $40M (8%), and $100M (7%).
 * Vault Accelerator Direction: A vault's personal rate can only stay the same or decrease; it can never be reversed, even during dormancy.
 * Accelerator Maximum: No vault can earn a reduction of more than 2 percentage points below the current protocol base rate.
1.2 Strategy & Safety Invariables
 * Base Ceiling: A standard vault has a $100,000 contribution cap and a $100,000 profit cap, for a $200,000 total ceiling.
 * NFT Cap Multipliers: Genesis Core raises the ceiling to $400,000 (2x), and Genesis Maxi raises it to $1,000,000 (5x).
 * Dynamic Asset Cap: A maximum of 30% of a vault's value may be held in non-stable assets (BTC, ETH, BNB, XRP, SOL). In Version 6.0, the AI may expand this to 50% under strict low-volatility conditions as verified by the Safety Layer.
 * Oracle Source: Chainlink BSC price feeds are the exclusive source for valuations and stop-loss triggers.
 * Whitelist Notice: New tokens added to the protocol require a 7-day notice period before they can activate in your vault.
1.3 Governance & Estate Invariables
 * Pause Maximum: The protocol cannot be paused for more than 72 consecutive hours without a 5-of-5 multisig vote.
 * Dead Man's Switch: If a vault remains inactive for 180 days, a pre-designated recovery address can trigger a 30-day countdown to claim control.
 * Overflow Timelock: Changes to your overflow routing destination take effect after a 48-hour delay to prevent immediate unauthorized redirects.
2. Legal Disclaimers & Entity Info
 * Jurisdiction: YieldLoop Ltd. is incorporated in the Republic of Seychelles.
 * Non-Custodial Reality: YieldLoop is a tool, not a service; we do not hold, control, or have access to user funds at any time.
 * Not Financial Advice: Nothing in any YieldLoop document or AI conversation constitutes financial, investment, or tax advice.
 * LOOP Token Status: LOOP is an internal, non-transferable accounting unit with no value outside the protocol.
3. Risk Disclosures
Digital asset investments involve substantial risk, including the complete loss of principal. Risks include:
 * Market Risk: Severe and sustained market declines can cause losses that exceed yield.
 * Smart Contract Risk: Despite audits, bugs or vulnerabilities in the protocol or partner contracts (Venus, Beefy, etc.) can occur.
 * Oracle Risk: Failure or manipulation of price feeds could trigger incorrect trades.
 * Liquidity Risk: Not all capital is immediately liquid; urgent exits carry premiums and costs.
4. Sanctions & Compliance
 * Screening: YieldLoop performs sanctions screening at every wallet connection against international watchlists (OFAC, EU, UN, UK).
5. Taxes
 * User Responsibility: Users are solely responsible for determining and meeting their tax obligations in their jurisdiction.
 * Tax Export: YieldLoop provides a universal CSV export of all vault activity to assist your accountant.
6. The Emergency Playbook
If an exploit or major failure occurs, a pause may be triggered:
 * Pause State: New deposits and withdrawals are suspended, but existing positions continue to process or remain held safely.
 * Transparency: Status updates are required every 6 hours during a protocol pause.

