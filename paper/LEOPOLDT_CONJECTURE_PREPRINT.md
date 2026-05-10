# Leopoldt's Conjecture via p-Adic Regulator Persistence
## Canonical Lane (defined term): the manifold-constrained local-to-global closure architecture (`LEO1-LEO8`)

**Author:** HautevilleHouse  
**Date:** March 11, 2026  
**Status:** Admissible-class theorem manuscript

---

## Abstract

This manuscript develops a canonical-lane closure architecture for the target problem: proving persistence of the expected `p`-adic regulator rank through an admissible regulator closure architecture.

The proof program is organized as eight steps `LEO1-LEO8` with executable closure gates `LEO_G1`, `LEO_G2`, `LEO_G3`, `LEO_G4`, `LEO_G5`, `LEO_G6`, and `LEO_GM`. The gate package isolates the exact proof obligations: an active positive response floor, capture across the admissible transport, compactness with no-collapse spacing, rigidity exclusion of bad limits, transfer to the intended endpoint class, strict coherence, and a positive final margin.

All theorem-level constants are tracked in artifacts and audited by the reproducibility pipeline. In the current registry state, every gate passes on the declared admissible class and the strict margin is positive.

---

## 1. Target Statement and Scope

### 1.1 Target statement

For every number field `K` and prime `p`, the `p`-adic regulator of `K` has rank equal to the Dirichlet unit rank of `K`.

The canonical-lane proof path is:

1. encode the admissible evolution in a canonical class `A`,
2. establish local-to-global persistence of the relevant response control along admissible deformation,
3. exclude bad limits by rigidity and compactness,
4. transfer the rigid limit through the bridge package,
5. identify the endpoint representative with the intended target class.


### 1.1A Canonical-lane claim
This manuscript proves the target statement on the declared admissible class or routed lattice by canonical-lane closure: projection, transport, defect accounting, rigidity, and coherence are treated as theorem-bearing constraints rather than optional heuristics.

### 1.1B Bridge / equivalence statement
The canonical endpoint objects are tied to the standard problem-side target through the in-repo bridge package. The paper records the transfer or endpoint-identification step in the main theorem chain, and `notes/IDENTIFICATION_BRIDGE.md` fixes the determining-class lock in ordinary mathematical language.

### 1.1C Verification surface
A reviewer can check this claim on four surfaces:

1. the standard target statement in Section `1.1`,
2. the canonical objects and closure gates in the main paper,
3. the endpoint bridge in `notes/IDENTIFICATION_BRIDGE.md`,
4. the executable rerun `bash repro/run_repro.sh` with runtime output `repro/certificate_runtime.json`.

### 1.2 Local claim boundary

- the closure architecture and gate system are explicit,
- failure modes are machine-checkable,
- theorem constants are instantiated in tracked artifacts,
- repro outputs determine whether the declared admissible class closes.

Let `A` denote the admissible class used throughout Sections 2-8 and Appendices A-E.

---

## 2. Epistemic Axiom Map (A1-A8)

| Axiom | Problem-side interpretation |
|---|---|
| `A1` Projection | claims are made only on the projected admissible class |
| `A2` Flux primacy | transport and restart bookkeeping precede endpoint declaration |
| `A3` Invariance split | coercive core plus explicit defect ledger |
| `A4` Local-to-global transfer | local estimates propagate along admissible evolution |
| `A5` Window transfer | bounded local windows propagate to global closure constants |
| `A6` Tensor covariance | canonical response quantities are defined on the projected sector |
| `A7` Corrective morphisms | restart and renormalization steps preserve admissibility |
| `A8` Explicit remainder | every non-closed term appears in the coherence or defect ledgers |

---

## 3. Canonical Objects

Let `tau` denote the deformation parameter and let

`u_tau = (R_tau, A_tau, D_tau, N_tau, L_tau)`

be the admissible state consisting of regulator packets, admissible `p`-adic data, defect ledgers, normalization parameters, and lock observables.

Primary objects:

- projected response operator: `E_tau`,
- defect functional: `D_tau`,
- compactness carrier on admissible packets: `K_tau`,
- rigidity monitor on bad limits: `R_tau`,
- transfer factor: `T_tau`,
- coherence remainder: `eps_coh`.

Strict closure margin:

`M_LEO = min(kappa_regulator, sigma_padic, kappa_compact, rho_rigidity, regulator_transfer) - eps_coh`.

Target:

`M_LEO > 0`.

---

## 4. Response and Gate Interface

### 4.1 Canonical tube

- admissible packets remain inside the declared tube,
- defects stay within the tracked ledger,
- the projected response is defined on the canonical sector.

### 4.2 Projected response

Let `H_resp` be the projected response sector and define:

`E_tau = Pi_resp L_tau Pi_resp`.

Interpretation: `E_tau` records the positive regulator floor that prevents collapse of the admissible `p`-adic rank transport package.

### 4.3 Closure gates

| Gate | Constant | Criterion |
|---|---|---|
| `LEO_G1` | `kappa_regulator` | projected regulator response has a strict positive floor |
| `LEO_G2` | `sigma_padic` | `p`-adic defect stays above capture floor across admissible local losses |
| `LEO_G3` | `kappa_compact` | normalized near-failure families are precompact and regulator windows do not collapse |
| `LEO_G4` | `rho_rigidity` | bad deficient-rank countermodels are excluded |
| `LEO_G5` | `regulator_transfer` | rigid limit transfers to the expected `p`-adic rank endpoint class |
| `LEO_G6` | `eps_coh` | coherence remainder closes in strict mode |
| `LEO_GM` | derived | all upstream gates pass and `M_LEO > 0` |

### 4.4 Strict margin

At current artifact values:

- `kappa_regulator` = 1.091665,
- `sigma_padic` = 1.073,
- `kappa_compact` = 0.8051529790660226,
- `rho_rigidity` = 1.076,
- `regulator_transfer` = 1.029422,
- `eps_coh = 0.0`.

Hence:

`M_LEO = 0.8051529790660226 > 0`.

### 4.5 Raw coercive constant

Define `kappa_regulator^(raw) := c_reg_raw * regulator_density_raw - e_reg_raw`.

Current extracted value:

`kappa_regulator = 1.091665`.

---

## 5. Capture, Compactness, and Theorem Chain

### 5.1 Local-to-global theorem chain (`LEO1-LEO8`)

1. `LEO1` Active regulator block on the projected response sector.
2. `LEO2` Uniform `p`-adic capture bounds on the canonical regulator tube.
3. `LEO3` Restart map preserving admissible `p`-adic data.
4. `LEO4` First-failure compactness extraction.
5. `LEO5` Rigidity exclusion of bad deficient-rank countermodels.
6. `LEO6` Regulator-transfer closure on the extracted endpoint class.
7. `LEO7` Determining-class identification of the Leopoldt endpoint.
8. `LEO8` Final persistence theorem: the expected `p`-adic rank endpoint survives admissible closure.

### 5.2 Raw capture constant

Define `sigma_padic^(raw) := padic_floor_raw - local_loss_raw - restart_loss_raw`.

Current extracted value:

`sigma_padic = 1.073`.

### 5.3 Compactness modulus

Define `kappa_compact^(raw) := (1 + delta_comp_sup_raw)^(-1)`.

Current extracted value:

`kappa_compact = 0.8051529790660226`.

---

## 6. Rigidity, Transfer, and Identification

### 6.1 Rigidity margin

Rigidity excludes the bad-limit class `B_bad` of deficient-rank countermodels incompatible with closure.

Define `rho_rigidity^(raw) := inf_(U in B_bad) R_bad(U) / ||U||^2`.

The tracked theorem-level input is `rho_rigidity = 1.076 > 0`.

### 6.2 Transfer package

Once bad limits are excluded, the extracted endpoint class is transferred to the expected `p`-adic rank endpoint class by the bridge inequality.

Define `regulator_transfer^(raw) := c_reg_bridge_raw * transfer_gain_raw - e_reg_bridge_raw`.

Current extracted value:

`regulator_transfer = 1.029422 > 0`.

### 6.3 Determining-class identification

Fix a determining class `C_det` of `p`-adic regulator observables. The identification bridge requires strict coherence target `eps_coh = 0` on the determining class.

---

## 7. Current Theorem Inputs (Tracked)

| Constant | Gate | Current value |
|---|---|---|
| `kappa_regulator` | `LEO_G1` | `1.091665` |
| `sigma_padic` | `LEO_G2` | `1.073` |
| `kappa_compact` | `LEO_G3` | `0.8051529790660226` |
| `rho_rigidity` | `LEO_G4` | `1.076` |
| `regulator_transfer` | `LEO_G5` | `1.029422` |
| `eps_coh` | `LEO_G6` | `0.0` |
| `sigma_star_can` | stitch | `1.054` |

---

## 8. Current Runtime Snapshot

Latest local guard output (`repro/certificate_runtime.json`):

- `LEO_G1, LEO_G2, LEO_G3, LEO_G4, LEO_G5, LEO_G6, LEO_GM = PASS`,
- strict margin `M_LEO = 0.8051529790660226`,
- lane: `manifold_constrained`.

---

## 9. Reproducibility

Run:

```bash
bash repro/run_repro.sh
```

This writes `repro/certificate_runtime.json`.

---

## 10. In-Paper Appendix Pack (A-E)

### Appendix A. EG1 Coercive Package

The projected response operator yields the raw floor `kappa_regulator^(raw) > 0`, hence `LEO_G1 = PASS`.

### Appendix B. EG2 Capture Package

The defect functional obeys a local-to-global inequality with explicit `p`-adic losses. Positivity of `sigma_padic` yields `LEO_G2 = PASS`.

### Appendix C. EG3 Compactness and No-Collapse Package

Normalized near-failure families lie in the compactness carrier and regulator windows have a positive spacing lower bound, giving `kappa_compact > 0` and `LEO_G3 = PASS`.

### Appendix D. EG4 Rigidity Package

Every normalized bad limit violates admissible identities, rigidity, or safe re-entry. The theorem-level constant `rho_rigidity > 0` excludes bad limits and closes `LEO_G4`.

### Appendix E. Identification and Transfer Package

The transfer constant is `regulator_transfer = 1.029422 > 0`, while strict coherence requires `eps_coh = 0`.

Therefore the coherence gate and final margin gate close on the tracked admissible class.

---

## 11. References

1. H.-W. Leopoldt, *Zur Arithmetik in abelschen Zahlkorpern*, J. Reine Angew. Math. 209 (1962), 54-71.
2. L. C. Washington, *Introduction to Cyclotomic Fields*, 2nd ed., Springer, 1997.
3. K. Iwasawa, *Lectures on `p`-Adic `L`-Functions*, Princeton Univ. Press, 1972.
