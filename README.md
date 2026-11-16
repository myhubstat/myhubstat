# (`@myhubstat`) — Smart Contract & Protocol Security Researcher

[![Portfolio & Audits](https://img.shields.io/badge/Security%20Portfolio-myhubstat%2Faudits-181717?logo=github)](https://github.com/myhubstat/audits)
[![EVM Static Analyzer](https://img.shields.io/badge/Tooling-evm--bounty--guard-blue)](https://github.com/myhubstat/evm-bounty-guard)

Independent smart contract and protocol security researcher specializing in **EVM / Solidity DeFi AMMs and share-accounting invariants**, **Rust L1/L2 wallet & confidential transfer security**, and **Solana Token-2022**.

Looking for paid audit and bounty work — fixed-price audits with escrow, and in-scope bug bounties.

- **Security Portfolio & Public Disclosures:** [**`github.com/myhubstat/audits`**](https://github.com/myhubstat/audits)
- **Audit Methodology:** Manual architectural & state-transition review, boundary rounding / interest-math verification, and custom static analysis. Reports in `audits` are written summaries — no Foundry PoCs are published there yet.

---

## Featured Security Research & Public Disclosures

| Target Protocol | Disclosure / PR | Vulnerability Class & Impact | Status |
| :--- | :--- | :--- | :--- |
| **`Dex223` AMM Core & Periphery** | **[Audit #36](https://github.com/rroland10/dex223-bug-bounty/issues/36)** · **[Fix PR #138](https://github.com/EthereumCommonwealth/Dex223-contracts/pull/138)** | `Dex223QuoteLib.quoteSwap` exact-output return inversion, `Dex223Pool.quoteSwap` `Error(string)` ABI-decode corruption, `ProtocolFeeCollector` 300k gas OOG on ERC-223 conversion, and `swapExactInput` negative `amountSpecified` guard. Audit filed in `rroland10/dex223-bug-bounty`, not in the upstream Dex223 repo. | **Audit closed 2026-11-03 · Fix PR closed, unmerged** |
| **`tari-project/tari-ootle`** (Tari L2 Confidential Wallet & Daemon) | **[PR #3135](https://github.com/tari-project/tari-ootle/pull/3135)** · **[PR #3158](https://github.com/tari-project/tari-ootle/pull/3158)** · **[PR #3157](https://github.com/tari-project/tari-ootle/pull/3157)** · **[PR #3155](https://github.com/tari-project/tari-ootle/pull/3155)** | Fixed live network broadcast during `--dry-run` confidential transfers (`MERGED`), hardened `walletd` `value_summaries` against `amount_leaving: 0` approval-card spoofing ([#3150](https://github.com/tari-project/tari-ootle/issues/3150)), and fixed SQLite cross-account output lock overwrite ([#3156](https://github.com/tari-project/tari-ootle/issues/3156)). | **MERGED** |
| **`limitlessprojects/Go-Hybrid`** (`Rust` / `Go` Ownership & Borrow Verifier) | **[PR #1998](https://github.com/limitlessprojects/Go-Hybrid/pull/1998)** · **[PR #1918](https://github.com/limitlessprojects/Go-Hybrid/pull/1918)** · **[PR #1897](https://github.com/limitlessprojects/Go-Hybrid/pull/1897)** · **[PR #1809](https://github.com/limitlessprojects/Go-Hybrid/pull/1809)** | Soundness work on `any`-field composite share tracking (`HYB-E3004`), closure alias `A3` loan windows (`HYB-E3102`), managed-block audit metadata injection (`HYB-E0003`), and truncated constant-key collisions. | **Open, unmerged — needs rebase** |
| **`SlopDotCash/slopdotcash`** (Solana `Token-2022` & Governance) | **[PR #1435](https://github.com/SlopDotCash/slopdotcash/pull/1435)** · **[PR #1348](https://github.com/SlopDotCash/slopdotcash/pull/1348)** | Preserved verified Solana `Token-2022` program ID across browser vault initialization (`MERGED`) and enforced reviewer independence on appeal denials. | **MERGED** |

---

## Security Tooling & Open-Source Repositories

- **[`myhubstat/audits`](https://github.com/myhubstat/audits)** — Public smart contract & protocol security disclosures (written reports).
- **[`myhubstat/evm-bounty-guard`](https://github.com/myhubstat/evm-bounty-guard)** — Static security analyzer for EVM/Solidity smart contracts. 5 detectors implemented (`EBG-001`–`EBG-005`, regex-based, `--json` output). 24 more detectors are described in `RULES.md` and not yet implemented.

---

<details>
<summary><b>Verified Settlement & On-Chain Identity</b></summary>

- **Primary EVM (`Base` / `Ethereum` / `Arbitrum` / `Optimism` / `Polygon` — `USDC` / `USDT` / `ETH`):** `0x669fBa588D75577610459a2577eabdbbBa080e4A`
- **Backup Tron (`TRC-20` — `USDT-TRC20` / `TRX`):** `TMbSRkXiuURMnMAvHp6p7Fpr5BrzU3YMDB`

</details>

<!-- slop-wallet:v1 {"address":"0x669fba588d75577610459a2577eabdbbba080e4a","chain":"base"} -->
<!-- slop-wallet:v1 {"address":"0x669fba588d75577610459a2577eabdbbba080e4a","chain":"ethereum"} -->
<!-- slop-wallet:v1 {"address":"0x669fba588d75577610459a2577eabdbbba080e4a","chain":"robinhood"} -->
<!-- slop-wallet:v1 {"address":"Cj1Nt6k36Fzie9KsgYaBnpw7J4oxm7nXbfBQeTzfboqi","chain":"solana"} -->
