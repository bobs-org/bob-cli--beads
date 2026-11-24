# Bead: bob-cli-pl.6.1.1 — Return the resulting settings contract from property previews and writes

[Bead Pages](../README.md) / [bob-cli-pl.6.1](bob-cli-pl.6.1.md) / bob-cli-pl.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.md) · **Assignee:** `bob-cli-pl.6.1.1` · **Size:** small
**Created:** 2026-11-24 15:49:21 EST · **Closed:** 2026-11-24 16:44:17 EST
**Plan:** [202611/area\_project\_settings.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_settings.md)

## Description

preview-contract: expose the candidate contract in successful update JSON, document the additive field, and test clear/apply/undo sources without changing validation or writes.

## Notes

[2026-11-24T21:10:16Z · bob-cli-pl.6.1.1] Successful update JSON returns view.report.contract on area/project/bank notes. Preview, apply, empty-ops, and restore share the additive field; ordinary notes omit it. Native and CLI tests cover clear-to-ghost color/residence, inherited/config labels, apply parity, inverse restore, bank hybrid, and dry-run byte preservation. epic-symbols: none. Host close is bound to just check.

[2026-11-24T21:44:17Z · bob-cli-pl.6.1.1--1] Successful update JSON returns view.report.contract on area/project/bank notes. Preview/apply/empty-ops/restore share the additive field; ordinary notes omit it. cargo fmt --check plus 14 lib and 8 CLI contract tests passed, including update_json_returns_candidate_contract_after_clear_apply_and_undo. Prior full just check also passed (exit 0). epic-symbols: none.

## Dependencies

- **Blocks:** [bob-cli-pl.6.1.2](bob-cli-pl.6.1.2.md) ◐ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.1.1.md) | [bob-cli-pl.6.1.1](bob-cli-pl.6.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`447ef1a`](https://github.com/bobs-org/bob-cli/commit/447ef1a5815924ca08329aee256598eaa9f999f9) | feat(props): return settings contract from successful property updates | [bob-cli-pl.6.1.1](bob-cli-pl.6.1.1.md) | 2026-11-24 16:46:13 EST |
