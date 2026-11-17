# Bead: bob-cli-mu.3 — Bank Setup card group jumps

[Bead Pages](../README.md) / [bob-cli-mu](README.md) / bob-cli-mu.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.57.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.57.linker.w0.md) · **Assignee:** `bob-cli-mu.3` · **Size:** small
**Created:** 2026-11-17 15:36:25 EST · **Closed:** 2026-11-17 16:49:10 EST
**Plan:** [202611/schema\_card\_field\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_card_field_jumps.md)

## Description

bank-groups: add Shift+J/K category-group jumps in the Categories tab using painted order, make hotkeys match lowercase only so Shift+K stops selecting Car, tint the current group label, add a footer hint, reuse the shared bump/reveal helpers, and add tests and docs.

## Notes

[2026-11-17T21:40:46Z · bob-cli-mu.3] PROPOSED FOLLOW-UP: Full-suite timing budgets flake under parallel load (event-link-times, frees-marks, keep-moving-marks-surface, off-clock-link-chips miss 25ms budgets by 5-150x in full npm test runs but pass 116/116 standalone and on the clean tree); consider --test-concurrency=1 for test:unit or looser perf budgets

[2026-11-17T21:48:50Z · bob-cli-mu.3] SYNC BLOCKED (reproduces on clean tree, not caused by this phase): `bob plugins sync -p bob-ledger-tools` refuses — vault holds orphaned uncommitted build from ws bob-cli_15 @ b0a9c89 (2026-11-17T18:48:30Z). That workspace is clean at 60b5602, no agent runs in ws 15, and its deploy-time delta is only the record-sheet feature already committed as 60b5602, so -F drops nothing unrecoverable. Vault bundle is v1.129.0-era (no field jumps, keycaps, record update, or group jumps); this phase deploys upstream e32deb6 (v1.130.0) + group jumps, a feature superset. Next: `bob plugins sync --repo $(pwd) --no-pull -p bob-ledger-tools -F` needs Bryan approval (never run unasked). Clean-tree sync at upstream HEAD refuses identically.

[2026-11-17T21:49:10Z · bob-cli-mu.3] Bank group jumps done on upstream e32deb6 base. Verified: new unit suite 5/5 (steps, clamps, parent-first K, HIDDEN last, hotkey tightening, uppercase inert, tab/gate/hint-mode inertness, projected-order arrows, label class, footer hint, no-write silence, reduced-motion bumps); focused suites 113/113 incl. mu.1 field-jump + mu.2-adjacent album suites; build + build:check + docs:inventory green; docs:check has only the pre-existing json-outputs.md budget error (identical on clean tree); full test:unit has 4-5 parallel-load timing flakes that pass 116/116 standalone (recorded as PROPOSED FOLLOW-UP). Real-key CDP probe added to bank setup e2e; --self-test green. NOT synced: vault sync refused by orphaned ws-15 uncommitted deploy (clean-tree repro, recorded SYNC BLOCKED note with -F rationale for Bryan/land agent).

## Dependencies

- **Depends on:** [bob-cli-mu.1](bob-cli-mu.1.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mu.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mu.3/README.md) | [bob-cli-mu.3](bob-cli-mu.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f80d0dd`](https://github.com/bobs-org/bob-plugins/commit/f80d0dd09ff23e5cb46f8ac4bb0fa09d81025c9a) | feat(bank-setup): walk category groups in painted order with Shift+J/K | [bob-cli-mu.3](bob-cli-mu.3.md) | 2026-11-17 16:51:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mu.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mu.3/README.md

<!-- sase:referenced-by:end -->
