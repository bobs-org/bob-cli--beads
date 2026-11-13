# Bead: bob-cli-l5.3.1.2 — Implement the ack queue and noninteractive command forms

[Bead Pages](../README.md) / [bob-cli-l5.3.1](bob-cli-l5.3.1.md) / bob-cli-l5.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-l5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-l5.3.md) · **Assignee:** `bob-cli-l5.3.1.2` · **Size:** medium
**Created:** 2026-11-12 20:43:26 EST · **Closed:** 2026-11-12 23:02:04 EST
**Plan:** [202611/gcal\_ack\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_ack_cli.md)

## Description

command: add ack arguments and dispatch, the forward batched queue, explicit event/series ack and clear, list/dry-run/JSON, shared stale detection, writer-host messaging, and shell completion. Cover membership, redaction, selection, persistence, and exit codes with fake gog.

## Notes

[2026-11-13T03:34:38Z · bob-cli-l5.3.1.2] PROPOSED FOLLOW-UP: Repair the existing docs-gen failure: bob-docs gen rejects sase/memory/glossary/event-ack.md because the strand has no front matter; this file is unchanged in this phase.

[2026-11-13T04:00:08Z · bob-cli-l5.3.1.2] PROPOSED FOLLOW-UP: `just all` also exposed existing clean-base failures: `native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none` is already tracked by bob-cli-l2, and `native::completion::kinds::tests::every_value_arg_has_a_decision` reports `gmail sync:confirm` with no matching Gmail completion bead found. This ack phase does not change those behaviors.

[2026-11-13T04:02:04Z · bob-cli-l5.3.1.2] Implemented the ack queue, explicit ack/clear and JSON preview/list modes, stale receipt detection, CLI completion/catalog registration, and generated CLI reference. Verified cargo check, fmt, clippy, 9 ack integration tests, 13 catalog tests, stale unit test, and neighboring gcal suites; the full workspace run still shows the two documented clean-base failures, with the gcal one tracked by bob-cli-l2. just docs-gen's CLI reference test passed; docs generation hit the recorded glossary front-matter issue.

## Dependencies

- **Depends on:** [bob-cli-l5.3.1.1](bob-cli-l5.3.1.1.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-l5.3.1.3](bob-cli-l5.3.1.3.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-l5.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.3.1.2/README.md) | [bob-cli-l5.3.1.2](bob-cli-l5.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1863b39`](https://github.com/bobs-org/bob-cli/commit/1863b39b0c6accf8d12f83f223b729c0191afdaf) | feat(gcal): add external event ack CLI | [bob-cli-l5.3.1.2](bob-cli-l5.3.1.2.md) | 2026-11-12 23:04:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.7][1] | Confirm the existing task that tracks the event-ack glossary front-matter docs generator failure before recording this phase's check result | 1 |
| read-by | [agent:bob-cli-l5.3.1.2][2] | Need the phase scope, design file, decisions, and any prior-work notes before implementation | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.7/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.3.1.2/README.md

<!-- sase:referenced-by:end -->
