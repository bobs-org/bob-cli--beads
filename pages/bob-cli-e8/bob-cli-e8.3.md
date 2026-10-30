# Bead: bob-cli-e8.3 — Reconcile projects mentions onto LINKED FROM

[Bead Pages](../README.md) / [bob-cli-e8](README.md) / bob-cli-e8.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2v.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2v.linker.w0.md) · **Assignee:** `bob-cli-e8.3` · **Size:** medium
**Created:** 2026-10-29 17:20:21 EDT · **Closed:** 2026-10-29 21:42:36 EDT
**Plan:** [202610/inline\_task\_mentions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/inline_task_mentions.md)

## Description

cli-reconcile: fold mention pairs into reconcile_relation_lines with precedence, minting, uncertainty, widened prefilters, the dark linked_from_mentions switch, and additive JSON and human output.

## Notes

[2026-10-30T01:42:28Z · bob-cli-e8.3] PROPOSED FOLLOW-UP: native::capture_related::tests::archive_closed_window_respects_mtime fails on clean master — stale done/ note with [completion:: 2026-10-01] still matches as closed_duplicate (days_ago=19) despite 40-day mtime; window appears to follow completion date, not mtime.

[2026-10-30T01:42:36Z · bob-cli-e8.3] cli-reconcile: mention pairs fold into reconcile_relation_lines behind relations.linked_from_mentions (default false). MN1–MN14, MN17, MN21, MN23 via fixture harness plus dedicated tests; LR1–LR24 still pass. Vault-copy dry-run with mentions on: mention_edges=57 (research ~64), 54 mention LINKED FROM inserts, 4 mention mints, no non-LINKED-FROM/non-mint delta vs mentions-off. Debug dry-run 3-pair avg 13.8s off → 16.5s on (~+19%). just check fmt+clippy green; workspace tests fail only archive_closed_window_respects_mtime, which reproduces on clean master.

## Dependencies

- **Depends on:** [bob-cli-e8.2](bob-cli-e8.2.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e8.4](bob-cli-e8.4.md) ✓ · ⧖ 2026-10-29
- **Blocks:** [bob-cli-e8.9](bob-cli-e8.9.md) ◐ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.3/README.md) | [bob-cli-e8.3](bob-cli-e8.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b8bcc78`](https://github.com/bobs-org/bob-cli/commit/b8bcc78a6a5218d5075b6efeef892685fdb79fbf) | feat(task-relations): project text mentions onto LINKED FROM | [bob-cli-e8.3](bob-cli-e8.3.md) | 2026-10-29 21:44:01 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-e8.3][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e8.3/README.md

<!-- sase:referenced-by:end -->
