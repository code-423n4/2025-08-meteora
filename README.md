# Meteora - Dynamic Bonding Curve audit details

**Award pool details**
- Total Prize Pool: $104,500 in USDC
  - HM awards: up to $96,000 in USDC
    - If no valid Highs are found, the HM pool is $19,200 in USDC
    - If no valid Highs or Mediums are found, the HM pool is $0
  - QA awards: $4,000 in USDC
  - Judge awards: $4,000 in USDC
  - Scout awards: $500 in USDC
- [Read our guidelines for more details](https://docs.code4rena.com/competitions)
- Starts August 22, 2025 20:00 UTC
- Ends September 12, 2025 20:00 UTC 

**❗ Important notes for wardens** 
1. A coded, runnable PoC is required for all High/Medium submissions to this audit. 
    - This repo includes a basic template to run the test suite.
    - PoCs must use the test suite provided in this repo.
    - Your submission will be marked as Insufficient if the POC is not runnable and working with the provided test suite.
    - Exception: PoC is optional (though recommended) for wardens with signal ≥ 0.68.
1. This audit includes **deployed code,** and [the "live criticals" exception](https://docs.code4rena.com/awarding/incentive-model-and-awards#the-live-criticals-exception) therefore applies. 
1. Judging phase risk adjustments (upgrades/downgrades):
    - High- or Medium-risk submissions downgraded by the judge to Low-risk (QA) will be ineligible for awards.
    - Upgrading a Low-risk finding from a QA report to a Medium- or High-risk finding is not supported.
    - As such, wardens are encouraged to select the appropriate risk level carefully during the submission phase.

## Publicly Known Issues

_Note for C4 wardens: Anything included in this `Automated Findings / Publicly Known Issues` section is considered a publicly known issue and is ineligible for awards._

## Links

- **Previous audits:** : https://docs.meteora.ag/resources/audits/dbc
- **Documentation:** 
  - [Overview of Meteora's Tech Stack](https://docs.meteora.ag/overview/home)
  - [Developer Documentation](https://docs.meteora.ag/developer-guide/home)
- **Website:** [meteora.ag](https://app.meteora.ag/)
- **X/Twitter:** [@MeteoraAG](https://x.com/MeteoraAG)

---

# Scope

## Files in Scope: (81 files)

- [`base_fee/fee_rate_limiter.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/base_fee/fee_rate_limiter.rs)
- [`base_fee/fee_scheduler.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/base_fee/fee_scheduler.rs)
- [`base_fee/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/base_fee/mod.rs)
- [`const_pda.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/const_pda.rs)
- [`constants.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/constants.rs)
- [`curve.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/curve.rs)
- [`error.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/error.rs)
- [`event.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/event.rs)
- [`admin/auth.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/auth.rs)
- [`admin/ix_claim_protocol_fee.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/ix_claim_protocol_fee.rs)
- [`admin/ix_close_claim_protocol_fee_operator.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/ix_close_claim_protocol_fee_operator.rs)
- [`admin/ix_create_claim_protocol_fee_operator.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/ix_create_claim_protocol_fee_operator.rs)
- [`admin/ix_withdraw_protocol_surplus.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/ix_withdraw_protocol_surplus.rs)
- [`admin/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/mod.rs)
- [`creator/ix_claim_creator_trading_fee.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/creator/ix_claim_creator_trading_fee.rs)
- [`creator/ix_create_virtual_pool_metadata.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/creator/ix_create_virtual_pool_metadata.rs)
- [`creator/ix_transfer_pool_creator.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/creator/ix_transfer_pool_creator.rs)
- [`creator/ix_withdraw_creator_surplus.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/creator/ix_withdraw_creator_surplus.rs)
- [`creator/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/creator/mod.rs)
- [`initialize_pool/ix_initialize_virtual_pool_with_spl_token.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/initialize_pool/ix_initialize_virtual_pool_with_spl_token.rs)
- [`initialize_pool/ix_initialize_virtual_pool_with_token2022.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/initialize_pool/ix_initialize_virtual_pool_with_token2022.rs)
- [`initialize_pool/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/initialize_pool/mod.rs)
- [`initialize_pool/process_create_token_metadata.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/initialize_pool/process_create_token_metadata.rs)
- [`migration/create_locker.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/create_locker.rs)
- [`migration/dynamic_amm_v2/damm_v2_metadata_state.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/damm_v2_metadata_state.rs)
- [`migration/dynamic_amm_v2/damm_v2_utils.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/damm_v2_utils.rs)
- [`migration/dynamic_amm_v2/migrate_damm_v2_initialize_pool.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/migrate_damm_v2_initialize_pool.rs)
- [`migration/dynamic_amm_v2/migration_damm_v2_create_metadata.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/migration_damm_v2_create_metadata.rs)
- [`migration/dynamic_amm_v2/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/mod.rs)
- [`migration/ix_withdraw_migration_fee.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/ix_withdraw_migration_fee.rs)
- [`migration/meteora_damm/meteora_damm_claim_lp_token.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/meteora_damm_claim_lp_token.rs)
- [`migration/meteora_damm/meteora_damm_lock_lp_token.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/meteora_damm_lock_lp_token.rs)
- [`migration/meteora_damm/meteora_damm_metadata_state.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/meteora_damm_metadata_state.rs)
- [`migration/meteora_damm/migrate_meteora_damm_initialize_pool.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/migrate_meteora_damm_initialize_pool.rs)
- [`migration/meteora_damm/migration_meteora_damm_create_metadata.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/migration_meteora_damm_create_metadata.rs)
- [`migration/meteora_damm/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/mod.rs)
- [`migration/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/mod.rs)
- [`migration/withdraw_leftover.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/withdraw_leftover.rs)
- [`instructions/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/mod.rs)
- [`partner/ix_claim_partner_trading_fee.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/partner/ix_claim_partner_trading_fee.rs)
- [`partner/ix_create_config.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/partner/ix_create_config.rs)
- [`partner/ix_create_partner_metadata.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/partner/ix_create_partner_metadata.rs)
- [`partner/ix_withdraw_partner_surplus.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/partner/ix_withdraw_partner_surplus.rs)
- [`partner/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/partner/mod.rs)
- [`swap/ix_swap.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/swap/ix_swap.rs)
- [`swap/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/swap/mod.rs)
- [`swap/swap_exact_in.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/swap/swap_exact_in.rs)
- [`swap/swap_exact_out.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/swap/swap_exact_out.rs)
- [`swap/swap_partial_fill.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/swap/swap_partial_fill.rs)
- [`lib.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/lib.rs)
- [`macros.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/macros.rs)
- [`math/fee_math.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/math/fee_math.rs)
- [`math/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/math/mod.rs)
- [`math/safe_math.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/math/safe_math.rs)
- [`math/u128x128_math.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/math/u128x128_math.rs)
- [`math/utils_math.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/math/utils_math.rs)
- [`params/fee_parameters.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/params/fee_parameters.rs)
- [`params/liquidity_distribution.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/params/liquidity_distribution.rs)
- [`params/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/params/mod.rs)
- [`params/swap.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/params/swap.rs)
- [`state/claim_fee_operator.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/claim_fee_operator.rs)
- [`state/config.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/config.rs)
- [`state/fee.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/fee.rs)
- [`state/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/mod.rs)
- [`state/partner_metadata.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/partner_metadata.rs)
- [`state/virtual_pool.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/virtual_pool.rs)
- [`state/virtual_pool_metadata.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/virtual_pool_metadata.rs)
- [`utils/activation_handler.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/utils/activation_handler.rs)
- [`utils/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/utils/mod.rs)
- [`utils/token.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/utils/token.rs)

## Files out of Scope: (13 files)

- [`dynamic-bonding-curve-sdk/src/lib.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/dynamic-bonding-curve-sdk/src/lib.rs)
- [`dynamic-bonding-curve-sdk/src/quote_exact_in.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/dynamic-bonding-curve-sdk/src/quote_exact_in.rs)
- [`dynamic-bonding-curve-sdk/src/quote_exact_out.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/dynamic-bonding-curve-sdk/src/quote_exact_out.rs)
- [`dynamic-bonding-curve-sdk/src/quote_partial_fill.r`s](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/dynamic-bonding-curve-sdk/src/quote_partial_fill.rs)
- [`tests/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/mod.rs)
- [`tests/test_quote_exact_out.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/dynamic-bonding-curve-sdk/src/tests/test_quote_exact_out.rs)
- [`tests/test_quote_partial_fill.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/dynamic-bonding-curve-sdk/src/tests/test_quote_partial_fill.rs)
- [`dynamic-bonding-curve-sdk/src/tests/mod.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/dynamic-bonding-curve-sdk/src/tests/mod.rs)
- [`dynamic-bonding-curve-sdk/src/tests/test_quote_exact_out.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/dynamic-bonding-curve-sdk/src/tests/test_quote_exact_out.rs)
- [`dynamic-bonding-curve-sdk/src/tests/test_quote_partial_fill.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/dynamic-bonding-curve-sdk/src/tests/test_quote_partial_fill.rs)
- [`libs/damm-v2/src/lib.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/libs/damm-v2/src/lib.rs)
- [`libs/dynamic-amm/src/lib.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/libs/dynamic-amm/src/lib.rs)
- [`libs/locker/src/lib.rs`](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/libs/locker/src/lib.rs)


# Additional context

## Areas of concern (where to focus for bugs)

Main areas to focus on:
- Funds are safe (reserve fund, fees of partner/creator/protocol, surplus amount, amount left)
- Identify any blockers for the migration process (i.e. after the bonding curve reaches the migration quote threshold, it should be migrated)

## Main invariants

Main contract: 
- https://github.com/MeteoraAg/dynamic-bonding-curve/tree/30dd2a1fc5c90949e2038f61c19dc03fee513d98

Third-party contracts:
- Damm v2: https://github.com/MeteoraAg/damm-v2
- Locker: https://github.com/jup-ag/jup-lock
- Damm v1/Dynamic vault: Closed source (https://docs.meteora.ag/overview/products/damm-v1/what-is-damm-v1)

## Running tests

pnpm install
pnpm test

## Sample PoC

Utilize the existing test suite here as your base for POC's:
- https://github.com/MeteoraAg/dynamic-bonding-curve/tree/30dd2a1fc5c90949e2038f61c19dc03fee513d98/tests
- https://github.com/MeteoraAg/dynamic-bonding-curve/tree/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests

## Miscellaneous
Employees of Meteora and employees' family members are ineligible to participate in this audit.

Code4rena's rules cannot be overridden by the contents of this README. In case of doubt, please check with C4 staff.
