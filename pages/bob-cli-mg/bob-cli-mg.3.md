# Bead: bob-cli-mg.3 — Bank Charts header balance readout in bob-ledger-tools

[Bead Pages](../README.md) / [bob-cli-mg](README.md) / bob-cli-mg.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.50.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.50.linker.w0.md) · **Assignee:** `bob-cli-mg.3` · **Size:** medium
**Created:** 2026-11-16 15:40:33 EST · **Closed:** 2026-11-16 18:58:45 EST
**Plan:** [202611/wf\_checking\_period\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/wf_checking_period_close.md)

## Description

readout: decode `balances[]` and paint the hero's resting BALANCE readout in the Bank Period Charts header, including the header-only quiet-period state, tooltip, aria, and activation. Update both repos' docs, review preview screenshots, and sync the plugins.

## Notes

[2026-11-16T23:58:45Z · bob-cli-mg.3] Readout done and verified; plugin deploy pending on WS-14. New 241nca-plugin-bank-period-balance.js (normalize, model, DOM builder) registered between 241nc/241nd; decode attaches balances[] (absent stays absent, malformed->null with one warn, never fails report); charts model carries balance with older-bob digest parity, balance-state header-only root, waiting-line append; header/paint/hosts/styles per plan. Tests: new test-ledger-tools-bank-period-balance.cjs (11 tests: matrix goldens, decode, parity, paint) — 83/83 bank tests pass; full npm test has 15 pre-existing env failures identical on clean base (setup-card, walkMode, perf, etc). Preview matrix renders without layout errors; reviewed 720-light + 360-dark PNGs for all 7 balance cases. Docs updated in both repos (plugin page trimmed to 6000-word cap; just docs-check + npm docs:check pass). Ran just install so installed bob emits balances[] (W46 as_of Fri Nov 13, matches ground truth). bob plugins sync BLOCKED: vault stamp is WS-14 uncommitted build (866bb77, live sibling agent); clean-sync recipe followed (fetch+ff+sync) but deployed bytes match no commit, and -F is forbidden. Retry after WS-14 lands: bob plugins sync --repo <this-checkout> --no-pull -p bob-ledger-tools. No memory edits (vocabulary belongs to mg.4).

## Dependencies

- **Depends on:** [bob-cli-mg.2](bob-cli-mg.2.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mg.4](bob-cli-mg.4.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mg.3/README.md) | [bob-cli-mg.3](bob-cli-mg.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3f47869`](https://github.com/bobs-org/bob-cli/commit/3f4786912cb40ca87e7ae231f085b05a65652a13) | docs(bank): document bank period balance readout | [bob-cli-mg.3](bob-cli-mg.3.md) | 2026-11-16 19:07:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mg.3][1] | Need phase scope and design | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mg.3/README.md

<!-- sase:referenced-by:end -->
