# @myhubstat ? Full-Stack Systems, Security Auditing, AI Automation & Compiler Engineering

**Independent Software Engineering & Security Research Studio** delivering production patches, vulnerability remediation, full-stack web/API systems, AI agent tooling, and compiler/runtime verification.

![Rust](https://img.shields.io/badge/Rust-Systems_%26_Compilers-000000?style=flat-square&logo=rust)
![Go](https://img.shields.io/badge/Go-Backend_%26_Concurrency-00ADD8?style=flat-square&logo=go)
![Python](https://img.shields.io/badge/Python-AI_%26_Automation-3776AB?style=flat-square&logo=python)
![TypeScript](https://img.shields.io/badge/TypeScript-Full--Stack_%26_Web3-3178C6?style=flat-square&logo=typescript)
![Security](https://img.shields.io/badge/Security-Auditing_%26_Bounties-2ea44f?style=flat-square)

---

### Engineering Capabilities & Domains
- **Full-Stack & API Engineering:** High-throughput REST/GraphQL services, TypeScript/React/Next.js applications, Go & Python microservices, database optimization.
- **AI Agents, MCP & Workflow Automation:** Autonomous CLI/SDK agents, MCP servers, browser/API scraping pipelines, LLM evaluation harnesses.
- **Security Auditing & Bug Bounties:** Static/dynamic vulnerability discovery, memory/concurrency race detection, smart-contract & backend hardening.
- **Systems & Compiler Toolchains:** AST/IR lowering, ownership & borrow-checking verification, differential testing (`Rust`, `Go`, `C/C++`).

---

### Selected Open-Source Patches & Security Audits

#### 1. Compiler Soundness & Codegen Verification ([`limitlessprojects/Go-Hybrid`](https://github.com/limitlessprojects/Go-Hybrid))
| Issue | Pull Request | Subsystem | Category | Summary |
|---|---|---|---|---|
| [#1752](https://github.com/limitlessprojects/Go-Hybrid/issues/1752) | [**PR #1753**](https://github.com/limitlessprojects/Go-Hybrid/pull/1753) | `hy-check` (`sendability.rs`) | **P0 Soundness** | Resolve generic callees (`f[T]`) in `spawn_callee_verdict` & `spawn_param_shapes` (`HYB-E3001` / `HYB-E4001`) |
| [#1808](https://github.com/limitlessprojects/Go-Hybrid/issues/1808) | [**PR #1809**](https://github.com/limitlessprojects/Go-Hybrid/pull/1809) | `hy-emit` (`lib.rs`) | **P0 Soundness** | Allocate N5 zero maps on named result parameters and `?` error-propagation returns to prevent `nil`-map panics |
| [#1761](https://github.com/limitlessprojects/Go-Hybrid/issues/1761) | [**PR #1762**](https://github.com/limitlessprojects/Go-Hybrid/pull/1762) | `hy-emit` (`stmt.rs`) | **P0 Buildable** | Lower type-ascribed `let` bindings (`let x T = e` / `let x T = f()?`) as typed Go `var` declarations |
| [#1763](https://github.com/limitlessprojects/Go-Hybrid/issues/1763) | [**PR #1764**](https://github.com/limitlessprojects/Go-Hybrid/pull/1764) | `hy-emit` (`expr.rs`) | **P0 Buildable** | Auto-address pointer parameters (`&arg`) and mangle value/parenthesized references on associated functions |
| [#1754](https://github.com/limitlessprojects/Go-Hybrid/issues/1754) | **RFC #1754** | Compiler IR | **Architecture** | Canonical `CalleeRef` IR + zero-transpile `go vet -vettool` analyzer architecture |

---

### Direct Bounty & Sponsorship Payment Rails
For open-source bounties, security disclosures, and direct grants:

- **USDC / USDT / ETH (Base, Ethereum, Arbitrum, Polygon, BNB Smart Chain ? EVM Self-Custody):**
  ```text
  0x669fBa588D75577610459a2577eabdbbBa080e4A
  ```
- **USDT ? Tron Network (`TRC-20`):**
  ```text
  TMbSRkXiuURMnMAvHp6p7Fpr5BrzU3YMDB
  ```
