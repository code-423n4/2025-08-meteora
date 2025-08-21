# Meteora - Dynamic Bonding Curve audit details

**Award pool details**
- Total Prize Pool: 104,500 in USDC
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

## Automated Findings / Publicly Known Issues

[⭐️ BYTES - can you run 4naly3er, or should we omit?]

The 4naly3er report can be found [here](https://github.com/code-423n4/YYYY-MM-contest-candidate/blob/main/4naly3er-report.md).

_Note for C4 wardens: Anything included in this `Automated Findings / Publicly Known Issues` section is considered a publicly known issue and is ineligible for awards._

## Links

- **Previous audits:** [⭐️ BYTES TODO]
- **Documentation:** 
  - [Overview of Meteora's Tech Stack](https://docs.meteora.ag/overview/home)
  - [Developer Documentation](https://docs.meteora.ag/developer-guide/home)
- **Website:** [meteora.ag](https://app.meteora.ag/)
- **X/Twitter:** [@MeteoraAG](https://x.com/MeteoraAG)

---

# Scope

### Files in Scope: (81 files)

- [fee_rate_limiter.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/base_fee/fee_rate_limiter.rs)
- [fee_scheduler.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/base_fee/fee_scheduler.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/base_fee/mod.rs)
- [const_pda.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/const_pda.rs)
- [constants.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/constants.rs)
- [curve.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/curve.rs)
- [error.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/error.rs)
- [event.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/event.rs)
- [auth.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/auth.rs)
- [ix_claim_protocol_fee.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/ix_claim_protocol_fee.rs)
- [ix_close_claim_protocol_fee_operator.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/ix_close_claim_protocol_fee_operator.rs)
- [ix_create_claim_protocol_fee_operator.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/ix_create_claim_protocol_fee_operator.rs)
- [ix_withdraw_protocol_surplus.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/ix_withdraw_protocol_surplus.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/admin/mod.rs)
- [ix_claim_creator_trading_fee.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/creator/ix_claim_creator_trading_fee.rs)
- [ix_create_virtual_pool_metadata.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/creator/ix_create_virtual_pool_metadata.rs)
- [ix_transfer_pool_creator.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/creator/ix_transfer_pool_creator.rs)
- [ix_withdraw_creator_surplus.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/creator/ix_withdraw_creator_surplus.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/creator/mod.rs)
- [ix_initialize_virtual_pool_with_spl_token.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/initialize_pool/ix_initialize_virtual_pool_with_spl_token.rs)
- [ix_initialize_virtual_pool_with_token2022.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/initialize_pool/ix_initialize_virtual_pool_with_token2022.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/initialize_pool/mod.rs)
- [process_create_token_metadata.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/initialize_pool/process_create_token_metadata.rs)
- [create_locker.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/create_locker.rs)
- [damm_v2_metadata_state.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/damm_v2_metadata_state.rs)
- [damm_v2_utils.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/damm_v2_utils.rs)
- [migrate_damm_v2_initialize_pool.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/migrate_damm_v2_initialize_pool.rs)
- [migration_damm_v2_create_metadata.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/migration_damm_v2_create_metadata.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/dynamic_amm_v2/mod.rs)
- [ix_withdraw_migration_fee.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/ix_withdraw_migration_fee.rs)
- [meteora_damm_claim_lp_token.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/meteora_damm_claim_lp_token.rs)
- [meteora_damm_lock_lp_token.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/meteora_damm_lock_lp_token.rs)
- [meteora_damm_metadata_state.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/meteora_damm_metadata_state.rs)
- [migrate_meteora_damm_initialize_pool.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/migrate_meteora_damm_initialize_pool.rs)
- [migration_meteora_damm_create_metadata.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/migration_meteora_damm_create_metadata.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/meteora_damm/mod.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/mod.rs)
- [withdraw_leftover.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/migration/withdraw_leftover.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/mod.rs)
- [ix_claim_partner_trading_fee.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/partner/ix_claim_partner_trading_fee.rs)
- [ix_create_config.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/partner/ix_create_config.rs)
- [ix_create_partner_metadata.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/partner/ix_create_partner_metadata.rs)
- [ix_withdraw_partner_surplus.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/partner/ix_withdraw_partner_surplus.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/partner/mod.rs)
- [ix_swap.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/swap/ix_swap.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/swap/mod.rs)
- [swap_exact_in.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/swap/swap_exact_in.rs)
- [swap_exact_out.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/swap/swap_exact_out.rs)
- [swap_partial_fill.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/instructions/swap/swap_partial_fill.rs)
- [lib.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/lib.rs)
- [macros.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/macros.rs)
- [fee_math.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/math/fee_math.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/math/mod.rs)
- [safe_math.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/math/safe_math.rs)
- [u128x128_math.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/math/u128x128_math.rs)
- [utils_math.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/math/utils_math.rs)
- [fee_parameters.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/params/fee_parameters.rs)
- [liquidity_distribution.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/params/liquidity_distribution.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/params/mod.rs)
- [swap.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/params/swap.rs)
- [claim_fee_operator.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/claim_fee_operator.rs)
- [config.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/config.rs)
- [fee.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/fee.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/mod.rs)
- [partner_metadata.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/partner_metadata.rs)
- [virtual_pool.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/virtual_pool.rs)
- [virtual_pool_metadata.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/state/virtual_pool_metadata.rs)
- [activation_handler.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/utils/activation_handler.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/utils/mod.rs)
- [token.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/utils/token.rs)

### Files out of Scope: (10 files)

- [lib.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/lib.rs)
- [quote_exact_in.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/quote_exact_in.rs)
- [quote_exact_out.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/quote_exact_out.rs)
- [quote_partial_fill.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/quote_partial_fill.rs)
- [tests/mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/mod.rs)
- [tests/test_quote_exact_out.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_quote_exact_out.rs)
- [tests/test_quote_partial_fill.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_quote_partial_fill.rs)
- [/damm-v2/src/lib.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/libs/damm-v2/src/lib.rs)
- [/dynamic-amm/src/lib.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/libs/dynamic-amm/src/lib.rs)
- [/locker/src/lib.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/libs/locker/src/lib.rs)
- [mod.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/mod.rs)
- [price_math.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/price_math.rs)
- [test_create_config.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_create_config.rs)
- [test_dynamic_fee_params.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_dynamic_fee_params.rs)
- [test_inverse_fee.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_inverse_fee.rs)
- [test_math_utils.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_math_utils.rs)
- [test_migration_fee_status.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_migration_fee_status.rs)
- [test_rate_limiter.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_rate_limiter.rs)
- [test_swap.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_swap.rs)
- [test_total_supply.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_total_supply.rs)
- [test_volitility_accumulate.rs](https://github.com/MeteoraAg/dynamic-bonding-curve/blob/30dd2a1fc5c90949e2038f61c19dc03fee513d98/programs/dynamic-bonding-curve/src/tests/test_volitility_accumulate.rs)

# Additional context

## Areas of concern (where to focus for bugs)

Main areas to focus on:
- Funds are safe (reserve fund, fees of partner/creator/protocol, surplus amount, amount left)
- Identify any blockers for the migration process (i.e. after the bonding curve reaches the migration quote threshold, it should be migrated)

## Main invariants

Main contract: 
- https://github.com/MeteoraAg/dynamic-bonding-curve

Third-party contracts:
- Damm v2: https://github.com/MeteoraAg/damm-v2
- Locker: https://github.com/jup-ag/jup-lock
- Damm v1/Dynamic vault: Closed source (https://docs.meteora.ag/overview/products/damm-v1/what-is-damm-v1)

## All trusted roles in the protocol

[⭐️ BYTES TODO - see table template below]

| Role                                | Description                       |
| --------------------------------------- | ---------------------------- |
| Owner                          | Has superpowers                |
| Administrator                             | Can change fees                       |


## Running tests

[⭐️ BYTES TODO]

✅ SCOUTS: Please format the response above 👆 using the template below👇

```bash
git clone https://github.com/code-423n4/2023-08-arbitrum
git submodule update --init --recursive
cd governance
foundryup
make install
make build
make sc-election-test
```
To run code coverage
```bash
make coverage
```

✅ SCOUTS: Add a screenshot of your terminal showing the test coverage - [⭐️ BYTES TODO]

## Sample PoC

[⭐️ BYTES TODO]

## Miscellaneous
Employees of Meteora and employees' family members are ineligible to participate in this audit.

Code4rena's rules cannot be overridden by the contents of this README. In case of doubt, please check with C4 staff.
