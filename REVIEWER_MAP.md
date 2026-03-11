# Reviewer Map

    ## Claim Scope

    - Canonical-lane claim: inside the `manifold_constrained` lane, if the theorem chain in this repository holds and the guard certificate passes, the repository-level closure claim is satisfied.
    - Standard target claim: carried by the in-repo bridge theorems tying the lane to the target statement.

    ## Theorem Dependency Chain

    1. `EG1`: coercive response and active control floor.
    2. `EG2`: capture and admissible continuation.
    3. `EG3`: compactness and no-collapse spacing.
    4. `EG4`: rigidity and transfer.
    5. Identification bridge: strict coherence on the determining class.
    6. Scalar closure: `LEO_G1, LEO_G2, LEO_G3, LEO_G4, LEO_G5, LEO_G6, LEO_GM` all `PASS`.

    Primary files:

    - `paper/LEOPOLDT_CONJECTURE_PREPRINT.md`
    - `notes/EG1_public.md`
    - `notes/EG2_public.md`
    - `notes/EG3_public.md`
    - `notes/EG4_public.md`
    - `notes/IDENTIFICATION_BRIDGE.md`

    ## Closure Gates

    | Gate | Constant | Description |
    |------|----------|-------------|
    | `LEO_G1` | `kappa_regulator` | projected regulator response has a strict positive floor |
| `LEO_G2` | `sigma_padic` | `p`-adic defect stays above capture floor across admissible local losses |
| `LEO_G3` | `kappa_compact` | normalized near-failure families are precompact and regulator windows do not collapse |
| `LEO_G4` | `rho_rigidity` | bad deficient-rank countermodels are excluded |
| `LEO_G5` | `regulator_transfer` | rigid limit transfers to the expected `p`-adic rank endpoint class |
| `LEO_G6` | `eps_coh` | strict coherence / identification closure |
| `LEO_GM` | derived | final strict margin |

    ## Falsification Conditions

    - `repro/certificate_runtime.json` has any non-`PASS` gate.
    - `lane.active_lane != "manifold_constrained"`.
    - `all_pass != true`.
    - Any manifest hash mismatch under `repro/repro_manifest.json`.
    - A verified counterexample to any EG theorem statement used in the paper.
