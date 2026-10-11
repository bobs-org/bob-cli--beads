# Bead: bob-cli-6l.5.1.4 — Verify the real renderer in light and dark

[Bead Pages](../README.md) / [bob-cli-6l.5.1](bob-cli-6l.5.1.md) / bob-cli-6l.5.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6l.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.5.md) · **Assignee:** `bob-cli-6l.5.1.4` · **Size:** medium
**Created:** 2026-10-11 14:15:46 EDT · **Closed:** 2026-10-11 16:20:23 EDT
**Plan:** [202610/stats\_charts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/stats_charts.md)

## Description

rendered_verification: add a fixture-driven browser preview, inspect light/dark and narrow/wide screenshots, fix visual and interaction defects, run integration checks, and deploy the completed plugin.

## Notes

[2026-10-11T20:10:21Z · bob-cli-6l.5.1.4--1] Verification: bob-ledger-tools 1.47.0; preview used Chrome/151.0.7922.34, fixture stats-browser-preview-canonical-1/schema 1, bob-cli 0.1.0 at ab314c061da8, BOB_NOW=2026-10-11 12:00:00, canonical SHA-256 1d88359eb84e71d514d749106091b7573319e901ea7fda4514c1bc902364327d, renderer main.js SHA-256 96b0b74e48be2d11cf316ad7ceb6664f945089575109d43a53d6b494cd225c23. Four screenshots were visually inspected; 9 charts/9 context panels, table, definition, and tooltip rendered at 360/1000 px in both themes without page overflow; all 14 browser interaction checks passed, including pointer/keyboard/focus/open/grouped-day/resize, reduced motion, and forced colors. Artifacts: file:explicit:d43bb7378c605a2e0347762e (360 light), file:explicit:0f212e5aa948daabad875383 (360 dark), file:explicit:74113e3c03000eeea3adebc7 (1000 light), file:explicit:34c79cdfd7216caeac586b8e (1000 dark), file:explicit:43fb3347b5c0ebfef240a8f7 (checked matrix report). npm run build passed; npm run validate passed 6/6 manifests; all 56 source fragments are <=995 lines; bob plugins sync --repo used this opened checkout and copied manifest 1.47.0 to /home/bryan/bob. npm test failed only on existing suite failures; a clean-base stash run reproduced test-task-status-cycler-successor-wiring failures (the tests expect 2026-10-09 while the current clock yields 2026-10-11). The dataviz skill was unavailable, so its validator was not run. just check is being run via the SASE monitor continuation.

[2026-10-11T20:10:26Z · bob-cli-6l.5.1.4--1] PROPOSED FOLLOW-UP: Track the pre-existing date-sensitive successor-wiring npm test failures: node --test scripts/test-task-status-cycler-successor-wiring.cjs fails on clean base when completion stamps use 2026-10-11 but expectations are pinned to 2026-10-09. Reproduced with our linked checkout changes stashed; prior Stats phase notes bob-cli-6l.5.1.2 and bob-cli-6l.5.1.3 record the broader clean-base suite failures. Search found no existing task bead for this successor-wiring failure; no new bead was created.

[2026-10-11T20:20:05Z · bob-cli-6l.5.1.4--2] PROPOSED FOLLOW-UP: The pre-existing percent-listen CLI failures remain out of scope for this Stats phase and are tracked by bob-cli-6m. They reproduce on the clean base as well as this phase tree: cargo test --locked --test cli exits 101 with 1364 passed and the same two tests failing in tests/cli/capture/ref.rs.

[2026-10-11T20:20:10Z · bob-cli-6l.5.1.4--2] Verification: monitored just check ansgw0r0y9m9 exited 101 after cargo fmt --check and clippy --all-targets --all-features passed; the CLI target had 1364 passed and the two bob-cli-6m failures. Clean-base reproduction used cargo test --locked --test cli with docs/stats.md stashed and produced the same two failures (exit 101, 25.49s); docs/stats.md was restored.

[2026-10-11T20:20:23Z · bob-cli-6l.5.1.4--2] Completed and verified Stats browser preview/deployment for bob-ledger-tools 1.47.0: Chrome 151.0.7922.34, schema-1 canonical fixture, four 360/1000 light/dark screenshots visually inspected, 14 browser interaction checks passed, npm build passed, npm validate 6/6, all 56 source fragments <=995 lines, and bob plugins sync confirmed the opened checkout. Artifacts: file:explicit:d43bb7378c605a2e0347762e, file:explicit:0f212e5aa948daabad875383, file:explicit:74113e3c03000eeea3adebc7, file:explicit:34c79cdfd7216caeac586b8e, file:explicit:43fb3347b5c0ebfef240a8f7. npm test retains clean-base date-sensitive failures; just check retains the two pre-existing percent-listen failures, reproduced on clean base and tracked by bob-cli-6m. epic-symbols reported none.

## Dependencies

- **Depends on:** [bob-cli-6l.5.1.3](bob-cli-6l.5.1.3.md) ✓ · ⧖ 2026-10-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6l.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6l.5.1.4.md) | [bob-cli-6l.5.1.4](bob-cli-6l.5.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`efc5593`](https://github.com/bobs-org/bob-cli/commit/efc55932f7b055437d270d5fea37f7186ce5fd73) | docs(stats): document charts and preview workflow | [bob-cli-6l.5.1.4](bob-cli-6l.5.1.4.md) | 2026-10-11 16:21:19 EDT |
