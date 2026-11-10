# Bead: bob-cli-iz.5 — Hold a replaced Events section and record the deletion policy

[Bead Pages](../README.md) / [bob-cli-iz](README.md) / bob-cli-iz.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1aa](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1aa.md) · **Assignee:** `bob-cli-iz.5` · **Size:** small
**Created:** 2026-11-09 07:12:09 EST · **Closed:** 2026-11-09 10:18:55 EST
**Plan:** [202611/gcal\_sync\_race\_force\_and\_skip\_reasons.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_sync_race_force_and_skip_reasons.md)

## Description

replaced_hold: bob-cli. When every row Bob wrote for the day and the Events stamp vanish together, do what the replaced_events decision says (default: hold with status `held`), update list/doctor/docs, and write the decision records. See plan section "Phase replaced_hold".

## Notes

[2026-11-09T15:18:55Z · bob-cli-iz.5] Implemented the replaced-Events held outcome, list/doctor reporting, forced recovery behavior, docs, and authorized decision records. Verified all gcal integration suites, cargo clippy --all-targets, cargo check --all-targets, and the replaced-section recovery test. just docs-check could not run because the mounted bob-mac-capture checkout resolves to the primary repo instead of its own Git worktree.

## Dependencies

- **Depends on:** [bob-cli-iz.4](bob-cli-iz.4.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-iz.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-iz.5/README.md) | [bob-cli-iz.5](bob-cli-iz.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9a0bb25`](https://github.com/bobs-org/bob-mac-capture/commit/9a0bb25c4b55b547a6d92c35c93017471e74feff) | feat(gcal)!: hold replaced Events sections | [bob-cli-iz.5](bob-cli-iz.5.md) | 2026-11-09 20:22:17 EST |
| bob-mac-capture | `bob-mac-capture@9a0bb25` | feat(gcal)!: hold replaced Events sections | [bob-cli-iz.5](bob-cli-iz.5.md) | 2026-11-09 20:22:17 EST |
