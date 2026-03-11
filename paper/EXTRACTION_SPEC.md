# Constant Extraction Spec (LEO)

    This file defines the theorem-constant extraction contract for this repository.

    ## Objective

    1. extract raw constants from explicit component inputs and formulas,
    2. normalize by declared references,
    3. promote into `artifacts/constants_registry.json` and `artifacts/stitch_constants.json`.

    ## Inputs
    - `artifacts/constants_extraction_inputs.json`

    ## Outputs
    - `artifacts/constants_extracted.json`
    - `artifacts/constants_registry.json`
    - `artifacts/stitch_constants.json`
    - `artifacts/promotion_report.json`

    ## Formula Set
    - `kappa_regulator_raw = c_reg_raw * regulator_density_raw - e_reg_raw`
- `sigma_padic_raw = padic_floor_raw - local_loss_raw - restart_loss_raw`
- `kappa_compact_raw = 1.0 / (1.0 + delta_comp_sup_raw)`
- `rho_rigidity_raw = rho_rigidity_raw`
- `regulator_transfer_raw = c_reg_bridge_raw * transfer_gain_raw - e_reg_bridge_raw`
- `eps_coh_raw = eps_coh_raw`
- `sigma_star_can_raw = sigma_star_can_raw`

    ## Validations
    - positivity required for: `kappa_regulator`, `sigma_padic`, `kappa_compact`, `rho_rigidity`, `regulator_transfer`, `sigma_star_can`
    - nonnegative required for: `eps_coh`
    - strict-zero required for: `eps_coh` in strict mode

    ## Execution
    `repro/run_repro.sh` runs:
    1. `scripts/extract_constants.py`
    2. `scripts/promote_constants.py`
    3. `scripts/leo_closure_guard.py`
