# Bead: bob-cli-gl.5.1.3 — Finish move output, help, and conformance verification

[Bead Pages](../README.md) / [bob-cli-gl.5.1](bob-cli-gl.5.1.md) / bob-cli-gl.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-gl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.md) · **Assignee:** `bob-cli-gl.5.1.3` · **Size:** medium
**Created:** 2026-11-03 16:14:54 EST · **Closed:** 2026-11-03 20:22:51 EST
**Plan:** [202611/capture\_move\_execution.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_execution.md)

## Description

move_presentation: Add human move output and the no-move discoverability hint, regenerate capture help, close remaining MV coverage gaps, and record warm dry-run performance. Supply verification evidence to the child epic land agent for bob-cli-gl.5.

## Notes

[2026-11-04T01:11:38Z · bob-cli-gl.5.1.3--1] PROPOSED FOLLOW-UP: Repair the docs generator failure already tracked by bob-cli-gm.1.1.4. Both `just docs-gen` (after its CLI reference test passed) and `just docs-check` fail at generated docs on `sase/memory/glossary/task-merge.md: memory strand has no front matter`; `git diff --quiet HEAD -- sase/memory/glossary/task-merge.md` confirmed the strand is unchanged.

[2026-11-04T01:11:47Z · bob-cli-gl.5.1.3--1] Warm dry-run timing: disposable synthetic fixture, 50 Markdown notes (40 parent task roots plus 288 unrelated roots; 11,233 bytes), debug/test-profile bob 0.4.0; draft creates a project, authors one task, moves `^p001`, and move-links `:p002`; one unmeasured warmup (99.62 ms), then 7 samples: 67.56, 72.08, 78.52, 77.59, 72.64, 58.48, 76.66 ms (median 72.64 ms, min 58.48 ms, max 78.52 ms).

[2026-11-04T01:22:41Z · bob-cli-gl.5.1.3--1] PROPOSED FOLLOW-UP: `just check` fails in clippy at `src/native/task_merge/mod.rs:14` (`unused import: payload::prepare_task_merge`). Confirmed the identical `just lint` failure in a temporary clean worktree at HEAD 14a57732; this phase diff does not touch task_merge. The related preparation API phase bob-cli-go.4.1.1 is closed and the task-merge integration phase bob-cli-go.4.1.3 is in progress; no bead specifically tracks this lint. Recheck after integration and consume, remove, or locally allow the re-export as appropriate.

[2026-11-04T01:22:51Z · bob-cli-gl.5.1.3--1] Verified focused project-note move tests (4 passed), docs reference regeneration, formatted tree, eligibility/human output coverage, and warm dry-run timing (72.64 ms median). Recorded clean-base clippy failure and docs-generator front-matter failure as proposed follow-ups; clean HEAD reproduces the former, and epic-symbols has no leftovers.

## Dependencies

- **Depends on:** [bob-cli-gl.5.1.2](bob-cli-gl.5.1.2.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.3.md) | [bob-cli-gl.5.1.3](bob-cli-gl.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ddb0a73`](https://github.com/bobs-org/bob-cli/commit/ddb0a73f1ead67088b89f07ba81946efb08d5a11) | feat(capture): show project-note moves and eligibility hints | [bob-cli-gl.5.1.3](bob-cli-gl.5.1.3.md) | 2026-11-03 20:24:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.5.1.3--1][1] | Verify the docs follow-up and warm dry-run evidence are recorded before closing | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.3.md

<!-- sase:referenced-by:end -->
