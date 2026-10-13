# Bead: bob-cli-7b.4 — Decision record, supersession marks, and docs sweep

[Bead Pages](../README.md) / [bob-cli-7b](README.md) / bob-cli-7b.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7c.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7c.w0.md) · **Assignee:** `bob-cli-7b.4` · **Size:** small
**Created:** 2026-10-13 08:12:08 EDT · **Closed:** 2026-10-13 10:36:01 EDT
**Plan:** [202610/capture\_link\_drops\_blocking\_deps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_link_drops_blocking_deps.md)

## Description

publish: sweep the docs for stale consumption wording and, under memory_supersede, add the new decisions record, mark the two records it partly supersedes, and run `sase memory init`.

## Notes

[2026-10-13T14:27:48Z · bob-cli-7b.4] Install the new bob and Bob Mac Capture on the MacBook through the usual install path. No vault migration is needed. Manual check: type ^job:blocked on a task Blocked by one open prerequisite; preview should show the dropped-dependency chip and Return should drop then link.

[2026-10-13T14:35:39Z · bob-cli-7b.4] PROPOSED FOLLOW-UP: just check reproduces the two percent-listen CLI failures (capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio, capture::r#ref::failed_percent_listen_worker_keeps_listen_retry_guidance), already tracked by bob-cli-6m

[2026-10-13T14:36:01Z · bob-cli-7b.4] Published capture-link-drops-blocking-deps, marked projects-block-from-prj-line and task-deps-are-depends-on-links superseded-in-part, ran sase memory init, and swept README.md plus docs/capture.md and docs/task-dependencies.md §5. just check: fmt and clippy clean; 1465 CLI tests passed; the two percent-listen failures match bob-cli-6m on clean base. epic-symbols: none leftover. Mac README already covered the drop. Bryan still needs to install the new bob and Bob Mac Capture; no vault migration.

## Dependencies

- **Depends on:** [bob-cli-7b.2](bob-cli-7b.2.md) ✓ · ⧖ 2026-10-13
- **Depends on:** [bob-cli-7b.3](bob-cli-7b.3.md) ✓ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7b.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-7b.4/README.md) | [bob-cli-7b.4](bob-cli-7b.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c80cbde`](https://github.com/bobs-org/bob-cli/commit/c80cbdeaf4c2bdf53d74b903e6a108c8d7a1a72f) | docs(memory): record capture dropping own blocking deps | [bob-cli-7b.4](bob-cli-7b.4.md) | 2026-10-13 10:37:23 EDT |
