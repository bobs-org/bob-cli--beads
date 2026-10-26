# Bead: bob-cli-ce.10 — Move Snapshot to Highlights onto the runner and refresh ledger caches

[Bead Pages](../README.md) / [bob-cli-ce](README.md) / bob-cli-ce.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5c.linker.w0.md) · **Assignee:** `bob-cli-ce.10` · **Size:** small
**Created:** 2026-10-26 10:35:53 EDT · **Closed:** 2026-10-26 13:12:32 EDT
**Plan:** [202610/bob\_colon\_command\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_colon_command_mode.md)

## Description

integrations: bob-project-tasks' Snapshot note to Highlights runs through api.commandMode when it is available, and bob-ledger-tools refreshes the caches a finished run invalidates.

## Notes

[2026-10-26T17:02:19Z · bob-cli-ce.10] --list

[2026-10-26T17:12:23Z · bob-cli-ce.10] PROPOSED FOLLOW-UP: docs-check lint fails on clean base — BOB_TEST_FIXTURE_PDF read at bob-cli src/native/highlights_ref/source_store.rs:185 is undocumented in docs/reference/configuration.md (verified on pristine 6f2f193 with no local modifications)

[2026-10-26T17:12:32Z · bob-cli-ce.10] Snapshot routes through api.commandMode v1 (ref create [+ -C], entryId ref-create, trigger api) with byte-for-byte legacy fallback; ledger-tools subscribes to bob-command-mode:run-finished and refreshes themes/relations/stats/references/tasks caches, ignoring unknown tags. Verified: focused suites 13/13, full npm test 3775/3775, build --check + validate + docs inventory green, scoped sync deployed both plugins. docs-check lint failure is pre-existing on clean base (recorded as follow-up).

## Dependencies

- **Blocks:** [bob-cli-ce.11](bob-cli-ce.11.md) ✓ · ⧖ 2026-10-26
- **Depends on:** [bob-cli-ce.7](bob-cli-ce.7.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ce.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.10/README.md) | [bob-cli-ce.10](bob-cli-ce.10.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@e3b2763`](https://github.com/bobs-org/bob-plugins/commit/e3b276313de3a5f58887444a2771b5ca13ecde4f) | feat(plugins): route snapshot through command-mode runner and refresh caches on run-finished | [bob-cli-ce.10](bob-cli-ce.10.md) | 2026-10-26 13:13:39 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ce.10][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.10/README.md

<!-- sase:referenced-by:end -->
