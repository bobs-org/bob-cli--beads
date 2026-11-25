# Bead: bob-cli-q5.1.1.3 — Public snooze CLI and guarded write shell

[Bead Pages](../README.md) / [bob-cli-q5.1.1](bob-cli-q5.1.1.md) / bob-cli-q5.1.1.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.md) · **Assignee:** `bob-cli-q5.1.1.3` · **Size:** medium
**Created:** 2026-11-25 10:36:16 EST
**Plan:** [202611/snooze\_wake\_engine.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/snooze_wake_engine.md)

## Description

guarded-cli: register bob snooze list/add/drop/wake and the read-only bare default, JSON and human output, completion and command-catalog entries. Add the bounded vault-lock/replan/preimage shell, multi-file add transaction, writer-host pin, dry-run behavior, and day rollover checks. Verify races, refusals, forecasts, and repeated wakes. Generate CLI references.

## Notes

[2026-11-25T19:51:40Z · bob-cli-q5.1.1.3] PROPOSED FOLLOW-UP: Reduce the pre-existing documentation word-budget overages (docs/develop/plugins/plugin-apis.md: 9276/8000, docs/reference/capture-syntax.md: 6011/6000, docs/reference/plugins/bob-navigation-hotkeys.md: 6068/6000); `just docs-check` reproduced the same failures on clean base e6eb52a1.

## Dependencies

- **Depends on:** [bob-cli-q5.1.1.2](bob-cli-q5.1.1.2.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.1.1.4](bob-cli-q5.1.1.4.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.1.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.1.1.3.md) | [bob-cli-q5.1.1.3](bob-cli-q5.1.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`68dee6e`](https://github.com/bobs-org/bob-cli/commit/68dee6e1f280f235971d55ee915ce46e82902b29) | feat(snooze): add public CLI and guarded write shell | [bob-cli-q5.1.1.3](bob-cli-q5.1.1.3.md) | 2026-11-25 16:17:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.7.1.land--2][1] | Identify existing docs-budget follow-up references for clean-base docs-check failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ph.7.1.land.md

<!-- sase:referenced-by:end -->
