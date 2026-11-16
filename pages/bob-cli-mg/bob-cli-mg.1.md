# Bead: bob-cli-mg.1 — Historical balance resolver and check findings

[Bead Pages](../README.md) / [bob-cli-mg](README.md) / bob-cli-mg.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.50.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.50.linker.w0.md) · **Assignee:** `bob-cli-mg.1` · **Size:** medium
**Created:** 2026-11-16 15:40:33 EST · **Closed:** 2026-11-16 16:33:02 EST
**Plan:** [202611/wf\_checking\_period\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/wf_checking_period_close.md)

## Description

resolver: add the pure bank/balance.rs resolver (coverage spans, final days, batch attribution, anchor segments, cross-checks, and period resolution) plus the two new `bob bank check` balance findings and their docs rows, with the invariant test suite.

## Notes

[2026-11-16T21:33:02Z · bob-cli-mg.1] Added src/native/bank/balance.rs (coverage spans, Final days, batch attribution, anchors, B(d), cross-checks, period resolution) and wired bank_balance_anchor_mismatch plus bank_balance_csv_overlap into bob bank check with docs/bank.md rows. Shared import_local_date with status.rs. 16 resolver tests cover the invariant suite and the phase case matrix. Gates: just fmt, just lint, just test, just docs-check.

## Dependencies

- **Blocks:** [bob-cli-mg.2](bob-cli-mg.2.md) ◐ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mg.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mg.1/README.md) | [bob-cli-mg.1](bob-cli-mg.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e49dbd4`](https://github.com/bobs-org/bob-cli/commit/e49dbd465daac7888ff45eb00e2f4e00c1beed6e) | feat(bank): add historical posted-balance resolver and check findings | [bob-cli-mg.1](bob-cli-mg.1.md) | 2026-11-16 16:34:25 EST |
