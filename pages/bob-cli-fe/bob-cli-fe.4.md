# Bead: bob-cli-fe.4 — The =\* merge syntax end to end (bob-cli)

[Bead Pages](../README.md) / [bob-cli-fe](README.md) / bob-cli-fe.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c4.md) · **Assignee:** `bob-cli-fe.4` · **Size:** medium
**Created:** 2026-11-01 16:00:43 EST · **Closed:** 2026-11-01 22:33:48 EST
**Plan:** [202611/merged\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merged_pomodoros.md)

## Description

capture-merge: repurpose =* as merge, keeping retired-close teaching for digit and marker forms; add execution, spans, completion, output, and docs.

## Notes

[2026-11-02T03:33:30Z · bob-cli-fe.4] PROPOSED FOLLOW-UP: keep_moving lazy-routing unit test flakes under parallel just check — native::task_complete::tests::keep_moving_tests::routing_is_lazy_and_narrow_with_shared_destination asserts FULL_ROOT_SCAN_COUNT==0 but sees 1 when the lib suite runs in parallel (process-global atomics in pomodoro_themes/scan.rs); passes isolated with --test-threads=1. Reproduces the keep-moving commit 39866275 pattern, not capture-merge.

[2026-11-02T03:33:31Z · bob-cli-fe.4] PROPOSED FOLLOW-UP: capture complete_themes CLI test flakes under parallel just check — capture::complete_themes::configured_shell_describes_never_used_and_unconfigured_create failed once looking for "your type · never used" and passed isolated. Treat as suite-order flake unless it reproduces on a serial run.

[2026-11-02T03:33:48Z · bob-cli-fe.4] Verified capture-merge: =* letter/#/quote is PomodoroMerge (R5 rename+move+dedupe, dests untimed planned); =*1/=*!2/=** stay retired close; dest-less =* needs pomodoro_merge_dest and teaches x*; ==* stays not-a-close. Language tests (9 merge + retired-close) and CLI tests (4 merge + 5 retired) pass. capture-parse spans/mode/need, capture-complete src/dest, JSON/human output, docs/capture.md + docs-gen capture-parse.md. just fmt and clippy clean. just check: lib+cli otherwise green; two parallel-only flakes recorded as PROPOSED FOLLOW-UP (keep_moving FULL_ROOT_SCAN_COUNT; complete_themes shell description). Grammar stays 5. No glossary edit (phase 10). No epic-symbols leftovers.

## Dependencies

- **Blocks:** [bob-cli-fe.10](bob-cli-fe.10.md) ◐ · ⧖ 2026-11-01
- **Depends on:** [bob-cli-fe.3](bob-cli-fe.3.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.9](bob-cli-fe.9.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fe.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.4/README.md) | [bob-cli-fe.4](bob-cli-fe.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bb92fb1`](https://github.com/bobs-org/bob-cli/commit/bb92fb1c07fadeb9117bb23f93f6e09fd60bf340) | feat(capture)!: add =\* merge syntax end to end | [bob-cli-fe.4](bob-cli-fe.4.md) | 2026-11-01 22:35:11 EST |
