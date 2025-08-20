# Sponsorname audit details
- Total Prize Pool: XXX XXX USDC (Notion: Total award pool)
  - HM awards: up to XXX XXX USDC (Notion: HM (main) pool)
    - If no valid Highs or Mediums are found, the HM pool is $0 
  - QA awards: XXX XXX USDC (Notion: QA pool)
  - Judge awards: XXX XXX USDC (Notion: Judge Fee)
- [Read our guidelines for more details](https://docs.code4rena.com/competitions)
- Starts XXX XXX XX 20:00 UTC (ex. `Starts March 22, 2023 20:00 UTC`)
- Ends XXX XXX XX 20:00 UTC (ex. `Ends March 30, 2023 20:00 UTC`)

**❗ Important notes for wardens** 
## 🐺 C4 staff: delete the PoC requirement section if not applicable - i.e. for non-Solidity/EVM audits.
1. A coded, runnable PoC is required for all High/Medium submissions to this audit. 
  - This repo includes a basic template to run the test suite.
  - PoCs must use the test suite provided in this repo.
  - Your submission will be marked as Insufficient if the POC is not runnable and working with the provided test suite.
  - Exception: PoC is optional (though recommended) for wardens with signal ≥ 0.68.
1. Judging phase risk adjustments (upgrades/downgrades):
  - High- or Medium-risk submissions downgraded by the judge to Low-risk (QA) will be ineligible for awards.
  - Upgrading a Low-risk finding from a QA report to a Medium- or High-risk finding is not supported.
  - As such, wardens are encouraged to select the appropriate risk level carefully during the submission phase.

## Automated Findings / Publicly Known Issues

The 4naly3er report can be found [here](https://github.com/code-423n4/YYYY-MM-contest-candidate/blob/main/4naly3er-report.md).

_Note for C4 wardens: Anything included in this `Automated Findings / Publicly Known Issues` section is considered a publicly known issue and is ineligible for awards._


### Files in Scope: (81 files)

- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/base_fee/fee_rate_limiter.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/base_fee/fee_scheduler.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/base_fee/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/const_pda.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/constants.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/curve.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/error.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/event.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/admin/auth.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/admin/ix_claim_protocol_fee.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/admin/ix_close_claim_protocol_fee_operator.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/admin/ix_create_claim_protocol_fee_operator.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/admin/ix_withdraw_protocol_surplus.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/admin/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/creator/ix_claim_creator_trading_fee.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/creator/ix_create_virtual_pool_metadata.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/creator/ix_transfer_pool_creator.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/creator/ix_withdraw_creator_surplus.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/creator/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/initialize_pool/ix_initialize_virtual_pool_with_spl_token.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/initialize_pool/ix_initialize_virtual_pool_with_token2022.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/initialize_pool/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/initialize_pool/process_create_token_metadata.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/create_locker.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/damm_v2_metadata_state.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/damm_v2_utils.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/migrate_damm_v2_initialize_pool.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/migration_damm_v2_create_metadata.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/ix_withdraw_migration_fee.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/meteora_damm_claim_lp_token.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/meteora_damm_lock_lp_token.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/meteora_damm_metadata_state.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/migrate_meteora_damm_initialize_pool.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/migration_meteora_damm_create_metadata.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/migration/withdraw_leftover.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/partner/ix_claim_partner_trading_fee.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/partner/ix_create_config.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/partner/ix_create_partner_metadata.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/partner/ix_withdraw_partner_surplus.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/partner/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/swap/ix_swap.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/swap/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/swap/swap_exact_in.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/swap/swap_exact_out.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/instructions/swap/swap_partial_fill.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/lib.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/macros.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/math/fee_math.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/math/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/math/safe_math.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/math/u128x128_math.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/math/utils_math.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/params/fee_parameters.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/params/liquidity_distribution.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/params/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/params/swap.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/state/claim_fee_operator.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/state/config.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/state/fee.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/state/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/state/partner_metadata.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/state/virtual_pool.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/state/virtual_pool_metadata.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/price_math.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/test_create_config.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/test_dynamic_fee_params.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/test_inverse_fee.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/test_math_utils.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/test_migration_fee_status.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/test_rate_limiter.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/test_swap.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/test_total_supply.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/tests/test_volitility_accumulate.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/utils/activation_handler.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/utils/mod.rs
- /app/dynamic-bonding-curve/programs/dynamic-bonding-curve/src/utils/token.rs

### Files out of Scope: (10 files)

- /app/dynamic-bonding-curve/dynamic-bonding-curve-sdk/src/lib.rs
- /app/dynamic-bonding-curve/dynamic-bonding-curve-sdk/src/quote_exact_in.rs
- /app/dynamic-bonding-curve/dynamic-bonding-curve-sdk/src/quote_exact_out.rs
- /app/dynamic-bonding-curve/dynamic-bonding-curve-sdk/src/quote_partial_fill.rs
- /app/dynamic-bonding-curve/dynamic-bonding-curve-sdk/src/tests/mod.rs
- /app/dynamic-bonding-curve/dynamic-bonding-curve-sdk/src/tests/test_quote_exact_out.rs
- /app/dynamic-bonding-curve/dynamic-bonding-curve-sdk/src/tests/test_quote_partial_fill.rs
- /app/dynamic-bonding-curve/libs/damm-v2/src/lib.rs
- /app/dynamic-bonding-curve/libs/dynamic-amm/src/lib.rs
- /app/dynamic-bonding-curve/libs/locker/src/lib.rs



