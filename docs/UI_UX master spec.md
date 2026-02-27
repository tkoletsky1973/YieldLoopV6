Doc 06: UI/UX Master Specification
Complete Interface Design, All Screens & Flows, and Non-Negotiable Rules
Version 6.0 — Effective Feb 2026
1. Core Design Principles
The YieldLoop interface is designed for radical transparency and ease of use, ensuring that sophisticated DeFi tools are accessible to everyone.
 * Fee Visibility: The protocol base, vault accelerated rate, and effective rate are shown per-vault at all times.
 * Rate Trajectory: Show users where the fee is going, not just its current state.
 * Risk Front-and-Center: Risk warnings are never buried behind scrolls or hidden menus.
 * No Dark Patterns: No pre-ticked boxes, hidden costs, or misleading confirmation flows.
 * Mobile-First: All flows are optimized for a 375px viewport.
2. The Fee Estimator Tool
Available pre-login on the landing page and post-login on the dashboard, this is a primary trust-building tool.
 * Inputs: Initial deposit, monthly top-up, frequency, NFT tier, and planning timeframe.
 * Output: A monthly breakdown of the projected protocol base, vault rate, and monthly savings.
 * Mandatory Caveat: The phrase "Estimated — not guaranteed" must appear with the same visual weight as the projected numbers.
3. Vault Creation Flow (The 6-Step Journey)
The AI Onboarding Guide contextualizes the form, acting as a conversational partner to explain stakes before inputs.
 * Step 1: Deposit Amount: Minimum $1,000 USDT.
 * Step 2: Gas Reserve: Option for "Auto-Rebalance" (Recommended) which uses ~2% of profits to top up gas automatically.
 * Step 3: Profit Distribution: Choose between USDT-only, 50/50, or LOOP-only.
 * Step 4: Overflow Routing: Set destination for capital exceeding vault caps (e.g., external wallet or second vault).
 * Step 5: AI Conversation: AI recommends a strategy tier based on user goals and displays "Kitchen Table Outcomes" in dollar terms.
 * Step 6: Acknowledgment: Users must check 10 individual boxes and manually type "I UNDERSTAND AND ACCEPT RESPONSIBILITY" to activate.
4. Dashboard & Vault Management
 * Portfolio Summary: Displays total balance, USDT ready for claim, and total LOOP value.
 * Accelerator Score: Shows progress toward the next rate reduction with specific tips to improve scores.
 * Token Allocation: Visual breakdown of all assets, highlighting the current percentage of the 30% (or dynamic 50%) non-stable cap.
 * Emergency UI: During a protocol pause, a red non-dismissible banner appears; balances remain visible, but new actions are disabled.
5. Withdrawal & Exits
 * Standard Closure: A clean wind-down over 5–7 days with no penalties.
 * Immediate Exit: Shows a full dollar-based breakdown of friction costs and the 20% urgency premium.
 * LOOP Treatment: Past-epoch LOOP is clearly labeled GREEN + SAFE, while current-epoch LOOP is labeled RED + FORFEITED.
6. Non-Negotiable UI Rules
These rules cannot be overridden by any team decision:
 * Stop-Loss Notifications: Always sent via push/email regardless of user opt-in settings.
 * Acknowledgment Input: Paste and autocomplete are disabled for the activation phrase.
 * Backup Phrase: Users MUST type back two randomly selected words to confirm their 12-word seed.
 * Tax Export: Always available, never gated, with no minimum period required.

