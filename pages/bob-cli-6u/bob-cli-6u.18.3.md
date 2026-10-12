# Bead: bob-cli-6u.18.3 — Capture link-guard, & on ^prj, and output-compatibility fixes

[Bead Pages](../README.md) / [bob-cli-6u.18](bob-cli-6u.18.md) / bob-cli-6u.18.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.land.md) · **Assignee:** `bob-cli-6u.18.3` · **Size:** medium
**Created:** 2026-10-12 18:07:06 EDT · **Closed:** 2026-10-12 18:59:41 EDT
**Plan:** [202610/prj\_line\_blocking\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_landing_fixes.md)

## Description

cli-capture: restore pull-forward for residents of unblocked projects, stop claiming links in existing capture JSON fields, resident cycle edges and id-less residents on & to ^prj, never raise Blocked seeds, struck links, `+` residents, keep-link consumption, and no whole-vault read for non-Blocked link targets.

## Notes

[2026-10-12T22:59:08Z · bob-cli-6u.18.3] PROPOSED FOLLOW-UP: Fix the two percent-listen CLI tests — clean-base `cargo test --test cli percent_listen` reproduces the same failures at tests/cli/capture/ref.rs:942 and :991; already tracked by CI bead bob-cli-6m.

[2026-10-12T22:59:41Z · bob-cli-6u.18.3] Verified cargo fmt --check, focused capture regressions, and full just check. The only check failures are the two capture percent-listen tests, reproduced identically on clean base at tests/cli/capture/ref.rs:942 and :991 and already tracked by bob-cli-6m. epic-symbols reported no entries.

## Dependencies

- **Blocks:** [bob-cli-6u.18.6](bob-cli-6u.18.6.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.3/README.md) | [bob-cli-6u.18.3](bob-cli-6u.18.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`53af9cb`](https://github.com/bobs-org/bob-cli/commit/53af9cbba2a5b99a8a0e18e9262170b72ebeac84) | fix(capture): honor project blocking in link gestures | [bob-cli-6u.18.3](bob-cli-6u.18.3.md) | 2026-10-12 19:00:34 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6u.18.3][1] | Check whether prior phase notes record remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.3/README.md

<!-- sase:referenced-by:end -->
