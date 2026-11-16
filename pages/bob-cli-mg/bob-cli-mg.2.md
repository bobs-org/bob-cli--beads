# Bead: bob-cli-mg.2 — balances\[\] in bob bank report, human line, and docs

[Bead Pages](../README.md) / [bob-cli-mg](README.md) / bob-cli-mg.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.50.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.50.linker.w0.md) · **Assignee:** `bob-cli-mg.2` · **Size:** small
**Created:** 2026-11-16 15:40:33 EST · **Closed:** 2026-11-16 17:36:17 EST
**Plan:** [202611/wf\_checking\_period\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/wf_checking_period_close.md)

## Description

report: wire the resolver into `bob bank report` for every period selector as an additive `balances[]` array and a human Balance line, then document the Closing balances contract and verify read-only against the live vault.

## Notes

[2026-11-16T22:36:17Z · bob-cli-mg.2] report: balances[] wired into bob bank report for every period selector (config order, cash omitted, [] when config missing, schema_version stays 1) plus human Balance line after Out/In/Net; docs Closing balances section and JSON bullets added; unit report-balances test and cli settle-across-imports e2e added. Verified: just fmt/lint/docs-check pass, 308 lib + 19 cli bank tests pass. Live vault read-only check matches plan ground truth with no discrepancy: W46 as_of 2026-11-13, W43-W45 and Q2-Q3 settled, Q4 so_far.

## Dependencies

- **Depends on:** [bob-cli-mg.1](bob-cli-mg.1.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mg.3](bob-cli-mg.3.md) ◐ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mg.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mg.2/README.md) | [bob-cli-mg.2](bob-cli-mg.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7b26a70`](https://github.com/bobs-org/bob-cli/commit/7b26a707d955c87a48609b92d52cac9f7012b276) | feat(bank): report period closing balances in bank report | [bob-cli-mg.2](bob-cli-mg.2.md) | 2026-11-16 17:37:43 EST |
