# Bead: bob-cli-7d.1 — bob-cli task\_goto grammar, candidates, docs, and digest vectors

[Bead Pages](../README.md) / [bob-cli-7d](README.md) / bob-cli-7d.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4b.linker.w0.md) · **Assignee:** `bob-cli-7d.1` · **Size:** medium
**Created:** 2026-10-13 09:50:29 EDT · **Closed:** 2026-10-13 10:12:31 EDT
**Plan:** [202610/slash\_task\_goto.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/slash_task_goto.md)

## Description

cli-goto: add the whole-draft `/query` claim (parse need `task_goto`, capture refusal, `task_goto` completion with `note_path`/`target` candidates over the `:` catalog), help, docs/capture.md, CLI tests, and the shared line-digest vector fixture.

## Notes

[2026-10-13T14:12:22Z · bob-cli-7d.1] PROPOSED FOLLOW-UP: capture::r#ref listen-worker tests fail identically on clean base (failed_percent_listen_worker_keeps_listen_retry_guidance, percent_listen_reference_runs_existing_worker_and_installs_audio) — pre-existing, unrelated to task_goto

[2026-10-13T14:12:31Z · bob-cli-7d.1] cli-goto done: task_goto claim/refusal/completion, TaskGoto candidates with note_path+target, help+docs, line_digest vectors (10/10 pass), 3 unit + 10 CLI tests green, just check green except 2 pre-existing ref listen-worker failures reproduced on clean base; live vault probe: parse incomplete/task_goto, complete task_goto with 36 rows in §4 key order, dry-run T3 refusal

## Dependencies

- **Blocks:** [bob-cli-7d.3](bob-cli-7d.3.md) ◐ · ⧖ 2026-10-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7d.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7d.1/README.md) | [bob-cli-7d.1](bob-cli-7d.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f2f2fd0`](https://github.com/bobs-org/bob-cli/commit/f2f2fd037f3cec857374af1c34fe37e137ef3052) | feat(capture): whole-draft /query Go To grammar, candidates, docs, and digest vectors | [bob-cli-7d.1](bob-cli-7d.1.md) | 2026-10-13 10:13:42 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7d.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7d.1/README.md

<!-- sase:referenced-by:end -->
