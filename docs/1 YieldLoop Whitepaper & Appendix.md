# Doc 01: The Whitepaper & Technical Appendix
### Protocol Design, Economics, & Architecture
**Version 6.0 — BNB Smart Chain Hub**

---

## 1. Abstract
YieldLoop is a non-custodial yield optimization protocol built on the **BNB Smart Chain (BSC)**. It integrates industrial-grade reliability—born from a decade of naval engineering and industrial automation expertise—with advanced AI to manage risk and maximize yield across a diversified 8-token basket. 

The protocol’s core innovation is the **One-Direction Fee Ratchet**, a hard-coded commitment that platform fees can only decrease as the protocol grows. Version 6.0 introduces the **Dynamic Non-Stable Cap (30%–50%)**, a decentralized **Dead Man’s Switch** for estate planning, and the **Redemption at Par** model for epoch-exits. YieldLoop exists to generate yield for its users and, through **LoopLab**, to manufacture human opportunity in underserved regions.

---

## 2. Design Principles
* **Non-Custodial Sovereignty:** Users retain absolute cryptographic control. YieldLoop cannot freeze, move, or recover funds. If the company disappears, the smart contracts remain accessible to the user.
* **Trust Through Invariables:** Critical rules (Invariables) are encoded in smart contracts and cannot be altered without a 5-of-5 multisig, a re-audit, and a 30-day public notice.
* **One-Directional Fees:** The fee ratchet is a permanent commitment; the protocol base rate can only decrease.
* **Conservative by Default:** Capital protection is the primary objective, enforcing a structural floor of at least 50% stablecoin exposure at all times.
* **Vault-Driven Strategy:** The AI determines strategy eligibility (Staking, LP, Arb, etc.) based on individual vault health and parameters, not arbitrary protocol-wide AUM gates.
* **Intrusive Leadership (LoopLab):** We apply the Navy model of leadership to our social mission—digging into every facet of the trainee's life to ensure we produce high-value human assets.

---

## 3. Fee Architecture
### 3.1 Protocol Base Rate (AUM Ratchet)
The platform fee on profits starts at **12%** and drops automatically as total protocol Assets Under Management (AUM) cross permanent milestones.

| Protocol AUM Milestone | Protocol Base Rate | Status |
| :--- | :--- | :--- |
| **Launch** | 12% | Starting Rate |
| **$1,000,000** | 11% | Permanent Drop |
| **$5,000,000** | 10% | Permanent Drop |
| **$15,000,000** | 9% | Permanent Drop |
| **$40,000,000** | 8% | Permanent Drop |
| **$100,000,000** | 7% | Permanent Floor |

### 3.2 Vault Accelerator
Users earn an additional personal discount of up to **2 percentage points (2pp)** below the base rate through consistent activity. 
* **Signals:** Balance (30%), Deposit Volume (25%), Deposit Frequency (25%), and Deposit Quality (20%).
* **Persistence:** This rate freezes during dormancy and never reverses.

### 3.3 Genesis NFT Discounts
Discounts are applied to the best available rate (Base or Accelerated).
* **Lite:** 10% off (13-month duration).
* **Core:** 20% off (Lifetime).
* **Maxi:** 50% off (Lifetime).

---

## 4. Strategy & Token Economics
### 4.1 The 8-Token Basket
* **Crypto:** BTC (BTCB), ETH, BNB, XRP (BEP-20), SOL (BEP-20).
* **Stablecoins:** USDT, USDC, DAI.

### 4.2 Dynamic Non-Stable Cap (30%–50%)
* **Standard Floor:** 30% default cap on non-stable assets for all tiers.
* **Dynamic Expansion:** The AI may expand exposure up to **50%** for Growth-tier vaults only if volatility is low, vault health is high, and DEX liquidity is sufficient.
* **Safety Layer Override:** If market volatility spikes >10% in a 1-hour window, the Safety Layer forces a rebalance back to 30% immediately.

---

## 5. The LOOP Loyalty System
LOOP is a non-transferable internal accounting unit representing a claim on future protocol success.
* **Issuance:** Issued at $1.000 at each epoch close for elected profits.
* **The Ratchet:** At least once every 90 days, a Ratchet Event permanently increases the redemption value of all outstanding LOOP (0.25%–2.0%).
* **Redemption at Par:** On an **Immediate Exit**, LOOP from the current (incomplete) epoch is redeemed at its issuance value of **$1.000**. The user keeps their principal yield but loses the loyalty appreciation (ratchet) for that batch. 

---

## 6. Security & Governance
### 6.1 The Dead Man’s Switch (Estate Plan)
* **Dormancy Trigger:** 180 days of zero vault activity.
* **Challenge Period:** A pre-designated secondary address triggers a 30-day on-chain countdown.
* **Execution:** If no veto by primary owner within 30 days, vault control transfers to the secondary address.

---

## 7. Technical Appendix (The "Nuts & Bolts")

### A1. Mathematical Formulas
* **LOOP Redemption Value:** `LOOP_Value = 1.00 × PRODUCT(1 + ratchet_i)` for all ratchet events fired after issuance.
* **Vault Accelerator Score:** `(Bal × 0.3) + (Vol × 0.25) + (Freq × 0.25) + (Qual × 0.20)`.

### A2. NFT Economics & Limits
| Tier | Price | Max Deposit (USDT) | Max Profit (Monthly) |
| :--- | :--- | :--- | :--- |
| **Standard** | Free | $100,000 | $100,000 |
| **Core** | Paid | $200,000 | $200,000 |
| **Maxi** | Paid | $500,000 | $500,000 |

### A3. Glossary of Terms
* **Arb Pool:** Shared protocol cross-DEX arbitrage pool. 48-hour queued exit.
* **Invariable:** A hard-coded rule that cannot be changed without 5-of-5 multisig and 30-day notice.
* **Safety Layer:** Deterministic rules engine that vetoes any AI recommendation violating an Invariable.
* **OracleGateway:** Single Chainlink integration point for all price feeds.

---

## 8. LoopLab & Fee Allocation
10% of fees and NFT sales fund **LoopLab**.
* **The $1 Right:** LoopLab owns the IP it develops; the creator has a contractual right to license their work for **$1** before anyone else.

| Allocation | Percentage |
| :--- | :--- |
| **Protocol Pools** | 65% |
| **Operations** | 10% |
| **Marketing** | 10% |
| **LoopLab** | 10% |
| **Credit Pool** | 5% |
