Doc 05: The Developer Guide
Smart Contract Architecture, Multi-Chain Logic, and Deployment Specs
Version 6.0 — Effective Feb 2026
1. Technical Philosophy
YieldLoop’s codebase is built for reliability and modularity. The architecture follows a "Hub-and-Spoke" model where the BNB Smart Chain (BSC) serves as the permanent home for all protocol-wide accounting, governance, and loyalty logic, while other chains serve as execution venues for individual vaults.
2. Smart Contract Architecture
The protocol is comprised of three primary contract categories:
2.1 The Vault System (The "Spoke")
 * Vault.sol: The core user-facing contract. Manages deposits, claims, and the 6-step activation flow. It strictly enforces Invariable contribution and profit caps.
 * StrategyRouter.sol: Receives signed allocation payloads from the AI Safety Layer and executes swaps across white-listed DEX venues.
 * RecoverySwitch.sol: Implements the Dead Man’s Switch logic, tracking the 180-day dormancy period and 30-day challenge window.
2.2 The Protocol Hub (BSC Only)
 * AUMRatchet.sol: Permanently tracks protocol-wide AUM and manages the One-Direction Fee Ratchet logic.
 * LOOPLedger.sol: Manages internal issuance and the RatchetEngine for credit appreciation.
 * NFTRegistry.sol: Stores Genesis NFT states and their bound multipliers for vault ceilings.
2.3 The Safety & Oracle Layer
 * OracleGateway.sol: A hardened single-point integration for Chainlink Price Feeds.
 * SafetyGuard.sol: Acts as the deterministic firewall that vetoes any transaction breaching the 30% (or dynamic 50%) non-stable cap.
3. Strategy Execution & Integration
Developers must ensure all strategy integrations adhere to the following rules:
 * Liquidity Provision: All LP positions must be routed through audited aggregators like Beefy or Krystal.
 * Staking: Liquid staking is restricted to stkBNB (Stader) and ankrBNB (Ankr) with immediate secondary market exit capability.
 * Lending: Only Supply-Only positions on Venus Protocol are permitted; no borrowing or liquidation risk is allowed.
 * Best Execution: The router must compare prices between PancakeSwap V3 and BiSwap for every swap.
4. Multi-Chain Data Propagation
The BSC Hub communicates with Spoke chains via standard messaging bridges to maintain a unified state:
 * AUM Tracking: Spoke vaults report their balance to the BSC Hub to trigger protocol-wide fee drops.
 * Accelerator Sync: Earned personal discounts on the Hub are propagated to Spoke vaults for fee calculation.
 * LOOP Issuance: Spoke vaults trigger credit issuance events on the BSC Hub at the close of each epoch.
5. Deployment Requirements
Mainnet deployment is prohibited until the following conditions are met:
 * Independent Audit: Full report from a third-party firm with all critical/high issues resolved.
 * Bug Bounty: Program must be active for at least 2 weeks prior to launch.
 * Testnet Pilot: Minimum 30-day community testing period on BSC Testnet.
6. Emergency & Access Control
 * Multisig: Standard operations use 3-of-5, while Invariable changes require 5-of-5.
 * Timelock: All Invariable changes must pass through a 30-day on-chain timelock.
 * Pause: An emergency key can pause specific functions for a maximum of 72 hours.

