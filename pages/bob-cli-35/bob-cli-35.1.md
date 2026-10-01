# Bead: bob-cli-35.1 — Shared target, marker, and install helpers

[Bead Pages](../README.md) / [bob-cli-35](README.md) / bob-cli-35.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3s.md) · **Assignee:** `bob-cli-35.1` · **Size:** small
**Created:** 2026-10-01 02:07:05 EDT · **Closed:** 2026-10-01 02:21:09 EDT
**Plan:** [202610/web\_url\_highlights\_clip.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/web_url_highlights_clip.md)

## Description

stamp-core: factor create's target planning, collision guards, marker composition, and stamp-plus-atomic-install into a shared module; add optional provenance marker keys; make `captured` a standard synced field.

## Notes

[2026-10-01T06:20:52Z · bob-cli-35.1] PROPOSED FOLLOW-UP: Fix pre-existing clippy deny clippy::overly_complex_bool_expr in tests/cli/capture/pomodoro_name.rs:808 (fails identically on clean base; unrelated to stamp-core)

[2026-10-01T06:21:09Z · bob-cli-35.1] stamp-core done: new highlights_ref/stamp.rs (TargetWorkflow/TargetPlan, plan_default_target/plan_exact_output, compose_marker with source_url/author/published/captured extras, stamp_and_install with PdfInfo Title/Author); create.rs refactored with identical behavior; captured added to COMMON_USER_FIELDS + docs. Verified: cargo fmt clean, cargo test full suite exit 0 (unit planner/marker/stamp tests, fake-pandoc create-path CLI test, scan provenance round-trip + rescan no-op). cargo clippy has one pre-existing unrelated deny in capture/pomodoro_name.rs:808, reproduced on clean base, filed as follow-up.

## Dependencies

- **Blocks:** [bob-cli-35.4](bob-cli-35.4.md) ✓ · ⧖ 2026-10-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-35.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-35.1/README.md) | [bob-cli-35.1](bob-cli-35.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fd12809`](https://github.com/bobs-org/bob-cli/commit/fd128098dc311aeb02b03f0911829157e384459a) | feat(highlights-ref): add shared stamp-core module with marker extras and atomic install | [bob-cli-35.1](bob-cli-35.1.md) | 2026-10-01 02:23:38 EDT |
