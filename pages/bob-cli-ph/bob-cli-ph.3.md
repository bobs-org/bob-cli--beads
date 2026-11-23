# Bead: bob-cli-ph.3 — Every host reads bold drawers before any writer flips

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.3` · **Size:** small
**Created:** 2026-11-22 17:36:48 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

reader-rollout: a host-currency script plus a gated check that bob on athena, apollo, and the Mac and the vault's deployed plugins all read bold drawers.

## Notes

[2026-11-23T23:49:39Z · bob-cli-ph.3] Reader-rollout implementation: added executable scripts/dev/bob-host-currency and wired it into just check-scripts. Final just check-scripts passed (exit 0). The gate checked drawer-contract commits 37b2080e and c25d92fd plus bob-task-drawer-dual-read-v1 in task-status-cycler, block-id-prompt, bob-ledger-tools, and bob-navigation-hotkeys. All four markers were present on athena, apollo, and mac; all hosts reported bob 0.6.0, but no v* release tag contains both commits, so the reader gate remains held for the release train.

## Dependencies

- **Depends on:** [bob-cli-ph.1](bob-cli-ph.1.md) ✓ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.2](bob-cli-ph.2.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.4](bob-cli-ph.4.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.3.md) | [bob-cli-ph.3](bob-cli-ph.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fd99ebb`](https://github.com/bobs-org/bob-cli/commit/fd99ebb85dcf0555cc48570397c419f4dd8f3167) | chore: add Bob host reader currency gate | [bob-cli-ph.3](bob-cli-ph.3.md) | 2026-11-23 18:51:04 EST |
