# Bead: bob-cli-hd.2 — Shared agreement rule, close settle, and Rust ledger applier

[Bead Pages](../README.md) / [bob-cli-hd](README.md) / bob-cli-hd.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5q.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5q.linker.w0.md) · **Assignee:** `bob-cli-hd.2` · **Size:** medium
**Created:** 2026-11-05 10:26:34 EST · **Closed:** 2026-11-05 11:06:58 EST
**Plan:** [202611/pomodoro\_names\_follow\_task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/pomodoro_names_follow_task_types.md)

## Description

agree-rule: add the pure `agree_entry` and `settle_closed` planners, the MEET guard in `relocate`, new shared vector sections, and one Rust applier that agrees chosen entries in a day's text through a pluggable task-type lookup.

## Notes

[2026-11-05T16:06:51Z · bob-cli-hd.2] PROPOSED FOLLOW-UP: docs-check tutorial TUTORIAL_FENCE 12 `=#focus` retired fails identically on clean base (verified via stash); likely tracks capture grammar retirement, needs task bead triage

[2026-11-05T16:06:58Z · bob-cli-hd.2] agree-rule lands: pure agree_entry/settle_closed in pomodoro_themes/agree.rs with 19 agree_entry + 10 settle vectors (incl idempotence), MEET guard in routing::relocate with 4 new relocate vectors, reusable agree_apply applier with TaskTypeLookup/default HomeResolver as-if-open typing + 5 applier tests (idempotence, CRLF, selector), docs/task-types.md agreement rule + vectors updated. Verified: cargo test --lib 5039 passed, cargo clippy clean, cargo fmt clean; just docs-check fails identically on base (recorded as follow-up).

## Dependencies

- **Blocks:** [bob-cli-hd.3](bob-cli-hd.3.md) ◐ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hd.4](bob-cli-hd.4.md) ◐ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hd.5](bob-cli-hd.5.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hd.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hd.2/README.md) | [bob-cli-hd.2](bob-cli-hd.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1f2b28b`](https://github.com/bobs-org/bob-cli/commit/1f2b28b03b514a4d72ed313c146a78ef51bd271e) | feat(task-types): shared agreement rule, close settle, and Rust ledger applier | [bob-cli-hd.2](bob-cli-hd.2.md) | 2026-11-05 11:08:25 EST |
