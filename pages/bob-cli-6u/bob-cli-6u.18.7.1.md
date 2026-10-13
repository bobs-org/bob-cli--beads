# Bead: bob-cli-6u.18.7.1 — Reconcile internal-id, warning, and projects-sync hoist fixes

[Bead Pages](../README.md) / [bob-cli-6u.18.7](bob-cli-6u.18.7.md) / bob-cli-6u.18.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.land.md) · **Assignee:** `bob-cli-6u.18.7.1` · **Size:** medium
**Created:** 2026-10-12 20:32:25 EDT · **Closed:** 2026-10-12 21:17:03 EDT
**Plan:** [202610/prj\_line\_blocking\_land\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_land_audit_fixes.md)

## Description

cli-reconcile-projects: filter same-note ids from inherited resident edges, warn only for field-named internal targets, scope the internal-id filter to recognised projects and to [id::] values, stop the frontmatter scheduled bypass of the hoist gate, revert ^prj matching to exact, CRLF and test-strength fixes, and the stale direct-^prj-link docs.

## Notes

[2026-10-13T01:16:44Z · bob-cli-6u.18.7.1--2] PROPOSED FOLLOW-UP: Fix the two percent-listen CLI failures tracked by bob-cli-6m — bob ref jobs run exits successfully without invoking the fake listen runner; clean-base b09612e reproduces both exact failures.

[2026-10-13T01:16:55Z · bob-cli-6u.18.7.1--2] Implemented the assigned fixes: filter inherited project edges by same-note [id::] values; warn only for field-named internal targets and once per row/id; limit internal-id filtering to recognized exact ^prj tasks; gate frontmatter scheduled propagation on an open ^prj; preserve line endings when inserting at end of a note; add regression coverage and update project/dependency/status-hook docs. Verification: just check exited 101 with 1410 CLI tests and 2449 library tests passing; its only failures were the two percent-listen tests. cargo test --test cli percent_listen on clean base b09612e reproduced both exact failures, tracked by bob-cli-6m and recorded above. Reconcile dry-run exited 1 with missing daily note /home/bryan/bob/2026/20261013.md and empty applied_files/deferred_files; it reported no planned edits. Projects sync dry-run exited 0: 85 projects, 0 status updates, 0 ^prj edits, 0 task schedule updates, 0 warnings. epic-symbols reported no entries.

[2026-10-13T01:17:03Z · bob-cli-6u.18.7.1--2] Verified the phase changes and regression coverage. just check has only the two known percent-listen failures, reproduced identically on clean base b09612e and tracked by bob-cli-6m. Reconcile dry-run reported the missing daily note with no applied or deferred files; projects sync dry-run reported 85 projects and no edits, schedule updates, or warnings. No epic symbols remain.

## Dependencies

- **Blocks:** [bob-cli-6u.18.7.5](bob-cli-6u.18.7.5.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.1.md) | [bob-cli-6u.18.7.1](bob-cli-6u.18.7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d2836e0`](https://github.com/bobs-org/bob-cli/commit/d2836e0ed1a24be033ffb29772a6d4053390283f) | fix(projects): correct ^prj reconcile and sync behavior | [bob-cli-6u.18.7.1](bob-cli-6u.18.7.1.md) | 2026-10-12 21:18:03 EDT |
