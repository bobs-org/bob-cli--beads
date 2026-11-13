# Bead: bob-cli-l5.3 — The bob gcal ack command

[Bead Pages](../README.md) / [bob-cli-l5](README.md) / bob-cli-l5.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c2.md) · **Assignee:** `bob-cli-l5.3` · **Size:** large
**Created:** 2026-11-12 16:39:08 EST · **Closed:** 2026-11-13 03:31:25 EST
**Plan:** [202611/gcal\_external\_event\_ack.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_external_event_ack.md)

## Description

cli: build the interactive one-key review queue (termios raw mode), the note branch through the shared note writer, one-shot/list/clear/dry-run/JSON forms, exit codes, the note.rs sibling-list fix, doctor acks section, stale-seen notices, and shell completion.

## Notes

[2026-11-13T08:34:36Z · bob-cli-l5.3.1.land] CLI phase closeout: the completed child epic covers the full bob gcal ack CLI, including queue suppression and selector mode validation, 80-column PTY presentation with terminal restoration, waiting and skipped-series refolding, journal read-error propagation, and exact-key orphan receipt clear. All four child phases are closed. Focused ack/TTY suites passed 39+7; auth, CLI, list, note, notes, and sync integration suites passed; the gcal lib set has 279 passed and one known sync_args_read_last_n_days_aliases_and_default_to_none failure assigned to bob-cli-l2 and reproduced on clean base 1863b39b. Formatting and clippy pass; no post-start origin drift; no epic symbols remain. The green just check run required a temporary test-expectation edit for that unrelated failure, reverted per the approved repair plan, so the final tree retains the known limitation. just symvision is unavailable in the Justfile.

## Dependencies

- **Depends on:** [bob-cli-l5.1](bob-cli-l5.1.md) ✓ · ⧖ 2026-11-12
- **Depends on:** [bob-cli-l5.2](bob-cli-l5.2.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-l5.4](bob-cli-l5.4.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-l5.5](bob-cli-l5.5.md) ◐ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-l5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-l5.3.md) | [bob-cli-l5.3](bob-cli-l5.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-l5.3.1.1][1] | Need the assigned CLI scope and final epic decisions | 1 |
| read-by | [agent:bob-cli-l5.3.1.2][2] | Need the assigned CLI scope and final epic decisions | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.3.1.2/README.md

<!-- sase:referenced-by:end -->
