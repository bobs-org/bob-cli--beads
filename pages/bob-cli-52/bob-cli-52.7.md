# Bead: bob-cli-52.7 — bob capture queues bare links for the reading queue

[Bead Pages](../README.md) / [bob-cli-52](README.md) / bob-cli-52.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.3w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.3w.linker.w1.md) · **Assignee:** `bob-cli-52.7` · **Size:** medium
**Created:** 2026-10-07 08:11:17 EDT · **Closed:** 2026-10-07 10:44:11 EDT
**Plan:** [202610/url\_capture\_ref\_routing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/url_capture_ref_routing.md)

## Description

capture: turn routing on in `capture` and `capture-parse`. Plan reference items with the offline verdict (including clipping and duplicate links), emit the additive JSON and the human wording, enqueue job files as rolled-back staged side effects, kick the worker after commit, add `-R/--no-ref`, and write the docs.

## Notes

[2026-10-07T14:43:56Z · bob-cli-52.7] PROPOSED FOLLOW-UP: lib failures missing_note_warning_successes, completion kinds decision, listen_filter card fail identically on clean base (see bob-cli-4j/4u/40 known failures)

[2026-10-07T14:44:01Z · bob-cli-52.7] PROPOSED FOLLOW-UP: cli test ingest_characterizes_url_failure_modes fails identically on clean base (uv resolves outside PATH on this host); needs hermetic-PATH fix

[2026-10-07T14:44:11Z · bob-cli-52.7] Routing on: lone bare URL queues (kind ref, placement queued, additive ref object with verdict/job/fallback); dry equals real apart from dry_run+job; verdicts in_library/in_intake/legacy/not_found/unknown/clipping/duplicate; -R on capture+parse; config error warns and stays task; jobs enqueue-then-commit with rollback and kick; human wording per table. Verified: cargo fmt clean, clippy no new warnings, 513 capture + full cli suite green except pre-existing ingest_characterizes failure (identical on base), lib green except 3 pre-existing base-identical failures; dry-run timing 14ms single / 10ms five-URL (debug). Fixed jobs twin test with -R.

## Dependencies

- **Depends on:** [bob-cli-52.4](bob-cli-52.4.md) ✓ · ⧖ 2026-10-07
- **Depends on:** [bob-cli-52.5](bob-cli-52.5.md) ✓ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.8](bob-cli-52.8.md) ◐ · ⧖ 2026-10-07
- **Blocks:** [bob-cli-52.9](bob-cli-52.9.md) ◐ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-52.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-52.7/README.md) | [bob-cli-52.7](bob-cli-52.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c9b361b`](https://github.com/bobs-org/bob-cli/commit/c9b361b205cc8fc529187ab1418b20009f5ce671) | feat(capture): queue bare links for the reading queue | [bob-cli-52.7](bob-cli-52.7.md) | 2026-10-07 10:46:15 EDT |
