# Hi, I'm @myhubstat

**Compiler Soundness, Static Analysis & Systems Engineer** specializing in ownership verification, concurrency safety, and Rust/Go compiler toolchains.

![Rust](https://img.shields.io/badge/Rust-Compiler_%26_Static_Analysis-000000?style=flat-square&logo=rust)
![Go](https://img.shields.io/badge/Go-Runtime_%26_Codegen-00ADD8?style=flat-square&logo=go)
![Focus](https://img.shields.io/badge/Focus-P0_Soundness_%26_Verification-2ea44f?style=flat-square)

---

### Featured Compiler Soundness & Codegen Contributions ([`limitlessprojects/Go-Hybrid`](https://github.com/limitlessprojects/Go-Hybrid))

| Issue | Pull Request | Subsystem | Rule / Track | Technical Summary |
|---|---|---|---|---|
| [#1752](https://github.com/limitlessprojects/Go-Hybrid/issues/1752) | [**PR #1753**](https://github.com/limitlessprojects/Go-Hybrid/pull/1753) | `hy-check` (`sendability.rs`) | **P0 Soundness** (`O4` / `N1` / Row 5) | Resolve folded generic callees (`f[T]`) in `spawn_callee_verdict` and substitute type arguments in `spawn_param_shapes` to close `HYB-E3001` (`*T` auto-addressing race across task boundaries) and `HYB-E4001` (`nil` into generic map/slice/chan parameter inside `managed`) |
| [#1808](https://github.com/limitlessprojects/Go-Hybrid/issues/1808) | [**PR #1809**](https://github.com/limitlessprojects/Go-Hybrid/pull/1809) | `hy-emit` (`lib.rs`) | **P0 Soundness** (`N5` / `N3` / Row 6) | Allocate N5 zero maps on named result parameters (`(m map[K]V)`, `(b bag)`) at function entry and in `zero_value` on `?` error-propagation returns to prevent runtime `assignment to entry in nil map` panics |
| [#1761](https://github.com/limitlessprojects/Go-Hybrid/issues/1761) | [**PR #1762**](https://github.com/limitlessprojects/Go-Hybrid/pull/1762) | `hy-emit` (`stmt.rs`) | **P0 Buildable** (`E3` / `N1` / Row 13) | Lower type-ascribed `let` bindings (`let x T = e` and `let x T = f()?`, SPEC 1.3) through typed `var` emission while preserving `?` hoisting and pointer/shape registration |
| [#1763](https://github.com/limitlessprojects/Go-Hybrid/issues/1763) | [**PR #1764**](https://github.com/limitlessprojects/Go-Hybrid/pull/1764) | `hy-emit` (`expr.rs`) | **P0 Buildable** (Row 13) | Unify associated-function (`S.f`) identifier mangling in `Expr::Field` and apply `fn_shapes` pointer-parameter auto-addressing (`&arg`) across associated and parenthesized calls |
| [#1754](https://github.com/limitlessprojects/Go-Hybrid/issues/1754) | **RFC #1754** | Architecture / IR | **Wildcard Track** | Kill the `.hy`/`.go` split and string-folded AST via a canonical `CalleeRef` IR and zero-transpile `go vet -vettool` analyzer mode |

---

### Core Areas
- **Static Analysis & Ownership Type Systems:** Sendability verification, alias/loan lifetime tracking, interprocedural summary analysis.
- **Compiler Codegen & Lowering:** AST-to-Go emission, generic instantiation, error-propagation (`?`) desugaring, zero-value invariants.
- **Verification & Fuzzing:** Differential oracle testing (`hyb check` vs. `go build` / `go run -race`), minimal counterexample synthesis.
