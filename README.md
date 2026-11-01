# Maaz (`@myhubstat`) — Smart Contract & Protocol Security Researcher

[![Portfolio & Audits](https://img.shields.io/badge/Security%20Portfolio-myhubstat%2Faudits-181717?logo=github)](https://github.com/myhubstat/audits)
[![EVM Static Analyzer](https://img.shields.io/badge/Tooling-evm--bounty--guard%20v1.0.0-blue)](https://github.com/myhubstat/evm-bounty-guard)

Independent smart contract and protocol security researcher specializing in **EVM / Solidity DeFi protocols** (`ERC-20`, `ERC-223`, `ERC-4626`, `EIP-7702`, lending routers, concentrated liquidity AMMs, and share-accounting invariants), **Rust L1/L2 wallet & confidential transfer security**, and **compiler/static-analysis soundness**.

- **Security Portfolio & Public Disclosures:** [**`github.com/myhubstat/audits`**](https://github.com/myhubstat/audits)
- **Audit Methodology:** Manual architectural & state-transition review backed by stateful **Foundry (`forge test`)** PoCs, boundary rounding/interest math verification, and custom static analyzers.

---

## Featured Security Research & Public Disclosures

| Target Protocol | Disclosure / PR | Vulnerability Class & Impact | Status |
| :--- | :--- | :--- | :--- |
| **`EthereumCommonwealth/Dex223-contracts`** (`DEX223` AMM Core & Periphery) | **[Audit #36](https://github.com/rroland10/dex223-bug-bounty/issues/36)** · **[Fix PR #138](https://github.com/EthereumCommonwealth/Dex223-contracts/pull/138)** | `Dex223QuoteLib.quoteSwap` exact-output return inversion, `Dex223Pool.quoteSwap` `Error(string)` ABI-decode corruption, `ProtocolFeeCollector` 300k gas OOG on ERC-223 conversion, and `swapExactInput` negative `amountSpecified` guard. | **Public Audit + Upstream Fix PR** |
| **`EthereumCommonwealth/Dex223-contracts`** (`DEX223` Exchange & Listing Registry) | **[Issue #25](https://github.com/rroland10/dex223-bug-bounty/issues/25)** · **[Issue #26](https://github.com/rroland10/dex223-bug-bounty/issues/26)** | EIP-7702 (`0xef0100`) delegated EOA callback bypass in `ERC223` transfer flow and duplicate fee-token tier overwrite in `AutoListingsRegistry`. | **Public Disclosure + Foundry PoC** |
| **`tari-project/tari-ootle`** (Tari L2 Confidential Wallet & Daemon) | **[PR #3135](https://github.com/tari-project/tari-ootle/pull/3135)** · **[PR #3158](https://github.com/tari-project/tari-ootle/pull/3158)** · **[PR #3157](https://github.com/tari-project/tari-ootle/pull/3157)** · **[PR #3155](https://github.com/tari-project/tari-ootle/pull/3155)** | Fixed live network broadcast during `--dry-run` confidential transfers (`MERGED`), hardened `walletd` `value_summaries` against `amount_leaving: 0` approval-card spoofing ([#3150](https://github.com/tari-project/tari-ootle/issues/3150)), and fixed SQLite cross-account output lock overwrite ([#3156](https://github.com/tari-project/tari-ootle/issues/3156)). | **MERGED / Active Upstream PRs** |
| **`limitlessprojects/Go-Hybrid`** (`Rust` / `Go` Ownership & Borrow Verifier) | **[PR #1998](https://github.com/limitlessprojects/Go-Hybrid/pull/1998)** · **[PR #1918](https://github.com/limitlessprojects/Go-Hybrid/pull/1918)** · **[PR #1897](https://github.com/limitlessprojects/Go-Hybrid/pull/1897)** · **[PR #1809](https://github.com/limitlessprojects/Go-Hybrid/pull/1809)** | Fixed soundness bypasses in `any`-field composite share tracking (`HYB-E3004`), closure alias `A3` loan windows (`HYB-E3102`), managed-block audit metadata injection (`HYB-E0003`), and truncated constant-key collisions. | **`bot:land-candidate` (`9/9 Pareto`)** |
| **`SlopDotCash/slopdotcash`** (Solana `Token-2022` & Governance) | **[PR #1435](https://github.com/SlopDotCash/slopdotcash/pull/1435)** · **[PR #1348](https://github.com/SlopDotCash/slopdotcash/pull/1348)** | Preserved verified Solana `Token-2022` program ID across browser vault initialization (`MERGED`) and enforced reviewer independence on appeal denials. | **MERGED Upstream** |

---

## Security Tooling & Open-Source Repositories

- **[`myhubstat/audits`](https://github.com/myhubstat/audits)** — Public smart contract & protocol security disclosures, Foundry PoC harnesses, and remediation diffs.
- **[`myhubstat/evm-bounty-guard`](https://github.com/myhubstat/evm-bounty-guard)** — Static security analyzer for EVM/Solidity smart contracts (`ERC-20`, `ERC-223`, `CREATE2`, reentrancy, and unchecked low-level call detectors).

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
