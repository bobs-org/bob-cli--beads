# Bead: bob-cli-78.3 — Close paths honour the tag proxy and pull in parents

[Bead Pages](../README.md) / [bob-cli-78](README.md) / bob-cli-78.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.71](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.71.md) · **Assignee:** `bob-cli-78.3` · **Size:** medium
**Created:** 2026-10-13 03:14:28 EDT · **Closed:** 2026-10-13 05:43:36 EDT
**Plan:** [202610/subproject\_cascade.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/subproject_cascade.md)

## Description

cli-close: make capture ! and =x closes read a tagged ^prj as an inherited reason (PDC4/PDC5), implement pull-in step 3 and trigger (c) with their rows, and add the close-path subtree recovery only under close_recovers_subprojects.

## Notes

[2026-10-13T09:43:07Z · bob-cli-78.3] cli-close verification: PDC4/PDC5 tag proxy, pull-in step 3 (PP32/PP36), trigger (c) (PP29-31,PP33-35) wired into ! and =x with prefilter-gated parent load (no catalog walk for ordinary closes). Unit: 10 new tests (pdc4, pdc5, pdc6-no, pp29-33 incl. prefilter); CLI: 6 new tests (! JSON+dry-run+human, PP34 sync dry-run, PP35 net pass, PDC4/PDC5 rows, =x trigger-c). Gate: fmt clean, clippy exit 0 (no new-code warnings), 2509 lib + 1439 cli pass; only failures are the 2 known bob-cli-6m percent-listen tests, verified identical on clean base. Perf (debug, /tmp/bob-perf vault copy 6281 md, dry-run median-of-3): non-prj closes within noise vs base (! plain 194-245 vs 202, ! proj 209-252 vs 198, =x plain 196-211 vs 199, =x proj 204-226 vs 216, ! noid 135-139 vs ~143, =x noid 23 vs 26); trigger-c adds honest new cost only on ^prj-with-parent closes (=x subprj 26->~150ms debug, ! subprj 144->144-179ms). close_recovers_subprojects=no honored: descendants keep tags until reconcile (pdc6-no test). No doc changes (contract already describes this); no memory edits (rollout owns them).

[2026-10-13T09:43:16Z · bob-cli-78.3] PROPOSED FOLLOW-UP: just check leaves only the 2 known bob-cli-6m percent-listen failures (capture::ref percent_listen_reference_runs_existing_worker_and_installs_audio, failed_percent_listen_worker_keeps_listen_retry_guidance); verified byte-identical failure on the clean base tree during bob-cli-78.3

[2026-10-13T09:43:21Z · bob-cli-78.3] PROPOSED FOLLOW-UP: update glossary project-task to say sub-projects inherit ancestor blocking (skipped per memory_glossary=no; rollout owns the call)

[2026-10-13T09:43:36Z · bob-cli-78.3] Verified: 10 new unit tests (PDC4/PDC5/PDC6-no, PP29-33+prefilter) and 6 new CLI tests (!/=x trigger-c, dry-run parity, PP34 sync, PP35 net pass) pass; fmt clean, clippy exit 0, 2509 lib + 1439 cli green with only the 2 known bob-cli-6m failures (identical on base); perf on vault copy shows non-prj closes within noise and trigger-c cost confined to ^prj-with-parent closes; no epic-symbols remain

## Dependencies

- **Depends on:** [bob-cli-78.2](bob-cli-78.2.md) ✓ · ⧖ 2026-10-13
- **Blocks:** [bob-cli-78.8](bob-cli-78.8.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-78.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-78.3/README.md) | [bob-cli-78.3](bob-cli-78.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6eceb00`](https://github.com/bobs-org/bob-cli/commit/6eceb00b76e1b4b93647451b3febdae07723d8dc) | feat(task-complete): honor project close cascade with tag proxy and pull-in | [bob-cli-78.3](bob-cli-78.3.md) | 2026-10-13 05:54:32 EDT |
