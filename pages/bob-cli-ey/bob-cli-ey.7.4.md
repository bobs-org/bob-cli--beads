# Bead: bob-cli-ey.7.4 — Bob Mac Capture real drawer fixtures and migrated task-type generator

[Bead Pages](../README.md) / [bob-cli-ey.7](bob-cli-ey.7.md) / bob-cli-ey.7.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.land.md) · **Assignee:** `bob-cli-ey.7.4` · **Size:** medium
**Created:** 2026-11-01 03:50:53 EST · **Closed:** 2026-11-01 08:08:21 EST
**Plan:** [202611/finish\_capture\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_capture_drawers.md)

## Description

mac-drawer-fixtures: regenerate the drawer fixtures from a bob that contains drawer-writes and drawer-menu, and retire the synthetic drawer-contract overlays and the parent_section fallback. Move generate-task-type-fixtures.sh off the retired attached #type forms, regenerate the task-type fixtures at grammar 3, update fake-bob and tests, and verify on macOS CI.

## Notes

[2026-11-01T13:08:09Z · bob-cli-ey.7.4--c] Verification evidence: grammar-3 Bob build and both fixture generators passed; second generation was idempotent (fixture hash 5cd78060e6906a54a0a0ab5323abed4f13b57028fba9d5e3bc107bac2514f16b). just check passed (monitor xjw784a4x337), and athena just portable-check passed (monitor 5fe3vs3a604g). macOS CI: run 41303480015 failed with seven bob-cli-f3 baseline tests plus three phase regressions; run 41305060555 failed with the seven baseline tests plus CaptureDrawerMenuPresentationTests.testEmptyQueryOpensWithOnThisTaskAndRecentGroupsAndNothingSelected; run 41308048455 failed only with the seven bob-cli-f3 baseline tests already documented by bob-cli-ey.7.3. Final checks passed (monitor 6xdahse9zmsh): retirement grep no matches, bash -n passed for both fixture generators and fake-bob, git diff --check passed. Initial grammar-3 fixture generation completed successfully.

[2026-11-01T13:08:21Z · bob-cli-ey.7.4--c] Completed grammar-3 fixture migration; fixture generation is idempotent. just check and athena portable-check passed. macOS CI run 41308048455 has only the seven bob-cli-f3 baseline failures documented in phase 7.3; earlier runs 41303480015 and 41305060555 and their extra failures are recorded in the bead notes. Retirement grep, bash syntax checks, and git diff --check passed; epic-symbol audit is clear.

## Dependencies

- **Depends on:** [bob-cli-ey.7.1](bob-cli-ey.7.1.md) ✓ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-ey.7.2](bob-cli-ey.7.2.md) ✓ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-ey.7.3](bob-cli-ey.7.3.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.7.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.7.4.md) | [bob-cli-ey.7.4](bob-cli-ey.7.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@361e929`](https://github.com/bobs-org/bob-mac-capture/commit/361e9293446796f79c9d01ae19e41d9b5b015c33) | feat(capture): migrate Mac Capture fixtures to grammar 3 | [bob-cli-ey.7.4](bob-cli-ey.7.4.md) | 2026-11-01 08:09:54 EST |
