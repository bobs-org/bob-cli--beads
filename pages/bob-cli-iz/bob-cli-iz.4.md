# Bead: bob-cli-iz.4 — Add the --force day reset to bob gcal sync

[Bead Pages](../README.md) / [bob-cli-iz](README.md) / bob-cli-iz.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1aa](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1aa.md) · **Assignee:** `bob-cli-iz.4` · **Size:** medium
**Created:** 2026-11-09 07:12:09 EST · **Closed:** 2026-11-09 09:46:10 EST
**Plan:** [202611/gcal\_sync\_race\_force\_and\_skip\_reasons.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_sync_race_force_and_skip_reasons.md)

## Description

force_reset: bob-cli. New force flag, `gcal.reset` journal record and fold, a planner reset that restores missing rows with their old block ids and re-applies Google over present rows, beautiful reset output, docs, and tests. See plan section "Phase force_reset".

## Notes

[2026-11-09T14:46:10Z · bob-cli-iz.4] Implemented the -F/--force day reset, gcal.reset fold, planner restoration/reapplication, reset reports, docs, and authorized decision memory. Verified: cargo fmt -- --check; cargo test --lib native::gcal (214 passed); Gcal integration suites (188 passed); just docs-check; cargo clippy --all-targets (passed with existing workspace warnings). epic-symbols was empty.

## Dependencies

- **Depends on:** [bob-cli-iz.2](bob-cli-iz.2.md) ✓ · ⧖ 2026-11-09
- **Depends on:** [bob-cli-iz.3](bob-cli-iz.3.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-iz.5](bob-cli-iz.5.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-iz.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-iz.4/README.md) | [bob-cli-iz.4](bob-cli-iz.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`97f0b8f`](https://github.com/bobs-org/bob-cli/commit/97f0b8f19b75c90e81e875c87462ae65850956db) | feat(gcal): add forced day reset | [bob-cli-iz.4](bob-cli-iz.4.md) | 2026-11-09 09:47:37 EST |
