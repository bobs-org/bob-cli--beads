# Bead: bob-cli-ce.3 — Color, progress, and exit receipts for non-TTY runs

[Bead Pages](../README.md) / [bob-cli-ce](README.md) / bob-cli-ce.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5c.linker.w0.md) · **Assignee:** `bob-cli-ce.3` · **Size:** small
**Created:** 2026-10-26 10:35:52 EDT · **Closed:** 2026-10-26 11:33:15 EDT
**Plan:** [202610/bob\_colon\_command\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_colon_command_mode.md)

## Description

run-env: bob honors CLICOLOR_FORCE, BOB_PROGRESS, and BOB_RUN_RECEIPT without a TTY, advertises them as catalog `features`, and documents them in the configuration reference.

## Notes

[2026-10-26T15:33:15Z · bob-cli-ce.3] CLICOLOR_FORCE colors piped help, NO_COLOR wins, CLICOLOR_FORCE=0 stays plain; BOB_PROGRESS=1 prints a line-oriented fetching line on piped stderr; BOB_RUN_RECEIPT writes schema-1 receipts for exit 0/2/1 and warns without changing exit on an unwritable path; catalog features are clicolor-force, progress-env, run-receipt; just docs-check passed; clippy rustc gate passed; epic-symbols had no leftovers.

## Dependencies

- **Depends on:** [bob-cli-ce.2](bob-cli-ce.2.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-ce.5](bob-cli-ce.5.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ce.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.3/README.md) | [bob-cli-ce.3](bob-cli-ce.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b5ba95c`](https://github.com/bobs-org/bob-cli/commit/b5ba95c96ec51418ad312e5e1b4e1fa71bb2753c) | feat(cli): honor color, progress, and exit receipts without a TTY | [bob-cli-ce.3](bob-cli-ce.3.md) | 2026-10-26 11:35:54 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ce.3][1] | Need remaining notes, design details, and earlier agent remainder | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.3/README.md

<!-- sase:referenced-by:end -->
