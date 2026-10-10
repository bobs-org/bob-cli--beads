# Bead: bob-cli-5y.11 — bob ref migrate-tasks

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.11` · **Size:** large
**Created:** 2026-10-09 12:29:34 EDT · **Closed:** 2026-10-09 19:53:48 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

migrate-tasks: add the dry-run-first, reversible command that moves open v1 ref tasks into parent notes and rewrites every link and dependency ID that pointed at them.

## Notes

[2026-10-09T23:53:38Z · bob-cli-5y.11] PROPOSED FOLLOW-UP: decisions strand ref-tasks-live-with-their-parent — memory_ref_parent_decision=no left the strand unwritten; residence is the parent and ^ref-<slug> is only an address.

[2026-10-09T23:53:41Z · bob-cli-5y.11] PROPOSED FOLLOW-UP: glossary strands reference-task, reference-note, and area-note — memory_glossary_ref_terms=no left the v2 reading-task wording unwritten.

[2026-10-09T23:53:48Z · bob-cli-5y.11] just check clean (fmt, clippy, full tests) and 10 migrate-tasks CLI tests cover marks, deps, wrappers, ambiguous, closed, unmapped, tsv, adoption, noop, json

## Dependencies

- **Blocks:** [bob-cli-5y.13](bob-cli-5y.13.md) ✓ · ⧖ 2026-10-09
- **Depends on:** [bob-cli-5y.7](bob-cli-5y.7.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5y.11.md) | [bob-cli-5y.11](bob-cli-5y.11.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8905153`](https://github.com/bobs-org/bob-cli/commit/89051533fbf1820e8aa89c6355cac883d6621ded) | feat(ref): add bob ref migrate-tasks dry-run-first migration | [bob-cli-5y.11](bob-cli-5y.11.md) | 2026-10-09 19:55:18 EDT |
