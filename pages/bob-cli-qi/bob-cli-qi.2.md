# Bead: bob-cli-qi.2 — Remove the bank area contract from bob and guard the no-tasks hub

[Bead Pages](../README.md) / [bob-cli-qi](README.md) / bob-cli-qi.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1gn](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1gn.md) · **Assignee:** `bob-cli-qi.2` · **Size:** medium
**Created:** 2026-11-26 10:06:12 EST · **Closed:** 2026-11-26 10:51:32 EST
**Plan:** [202611/bank\_hub\_demotion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_hub_demotion.md)

## Description

cli-hub: drop NoteKind::Bank from the props settings contract (a ! commit), refuse @bank task captures with a preview diagnostic, and add the bank_hub_task and bank_hub_area_type findings to bob bank check. Also fix the starter text and the note-catalog order, invert the hybrid tests, untype the hub fixtures, and correct the bob-cli docs.

## Notes

[2026-11-26T15:51:18Z · bob-cli-qi.2] PROPOSED FOLLOW-UP: capture::transfer::transfer_merge_refusals_are_atomic_and_coded fails identically on clean master (drawer_near_duplicate case succeeds when it should refuse); pre-existing, unrelated to bank hub work -r Recording pre-existing failure found during cli-hub verification

[2026-11-26T15:51:32Z · bob-cli-qi.2] cli-hub done: props contract dropped for Bank (settings.rs for_kind Area-only, read.rs/cli.rs docs, contract/tests + props_contract CLI inverted to no-contract/card-owned/prop_setting_disabled, roles fixture untyped); @bank refused via BANK_HOLDS_NO_TASKS_CODE + bank_holds_no_tasks_error + is_bank_hub_route in all 4 plan.rs paths and capture-parse preview with @cash rewrite (3 new bank_hub CLI tests); bank check gains bank_hub_area_type + bank_hub_task warnings (unit + CLI tests, docs table); starter text untyped; catalog checks bank before area + regression test; hub fixtures untyped across bank/walks/props suites; areas bank->garden renames; docs bank/props/vault-format/json-outputs/capture updated. Verified: cargo fmt --check ok, cargo clippy gate ok, docs-gen + docs-check pass, targeted suites green (lib props/bank/catalog/areas 68+322+56; cli bank/props/bank_hub/walks/areas 84). Mac Capture read-only check: only album_holds_no_tasks is special-cased, bank code renders generically. Pre-existing transfer_merge_refusals failure recorded as follow-up.

## Dependencies

- **Blocks:** [bob-cli-qi.4](bob-cli-qi.4.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-qi.5](bob-cli-qi.5.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-qi.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qi.2/README.md) | [bob-cli-qi.2](bob-cli-qi.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`478d523`](https://github.com/bobs-org/bob-cli/commit/478d5233100d45ba27d1bf29530eb790a36a8837) | feat(bank,props,capture): enforce Area-only props and bank-holds-no-tasks | [bob-cli-qi.2](bob-cli-qi.2.md) | 2026-11-26 10:52:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qi.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-qi.2/README.md

<!-- sase:referenced-by:end -->
