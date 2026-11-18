# Bead: bob-cli-mx.1 — Freshness scan parses the vault once

[Bead Pages](../README.md) / [bob-cli-mx](README.md) / bob-cli-mx.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.es.md) · **Assignee:** `bob-cli-mx.1` · **Size:** small
**Created:** 2026-11-17 17:59:52 EST · **Closed:** 2026-11-17 19:15:27 EST
**Plan:** [202611/mac\_walk\_attention\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_walk_attention_marks.md)

## Description

scan-once: share one Tasks settings read and one TaskIndex across the freshness scan's READY/PENDING/NEXT/OPEN queries and its all-task pass, with byte-identical outputs and recorded before/after timings.

## Notes

[2026-11-18T00:14:53Z · bob-cli-mx.1--1] PROPOSED FOLLOW-UP: Repair the records tidy command registry and help contract — clean-base just check failures reproduce in catalog::tests::public_leaves_are_entries_or_excluded, completion::kinds::tests::every_value_arg_has_a_decision, runner::tests::every_native_command_is_on_exactly_one_canonical_path, and help_options::records_help_lists_subcommands_and_options_alphabetically.

[2026-11-18T00:15:27Z · bob-cli-mx.1--1] Implemented and focused shared-index test passed; release timing improved from 3.63s to 1.24s. just check fails only on four records tidy registry/help tests, each reproduced on the clean base tree and recorded as a proposed follow-up; no epic symbols remain.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mx.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mx.1.md) | [bob-cli-mx.1](bob-cli-mx.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3c796c7`](https://github.com/bobs-org/bob-cli/commit/3c796c7c2d70b728b2a17e16174ba5083c62bd28) | perf(freshness): reuse task index during scans | [bob-cli-mx.1](bob-cli-mx.1.md) | 2026-11-17 19:17:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mx.1--1][1] | Need current phase scope and completion status after failed gate | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-mx.1.md

<!-- sase:referenced-by:end -->
