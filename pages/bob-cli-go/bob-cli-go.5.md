# Bead: bob-cli-go.5 — \`bob task merge\` and \`bob task move -t\`

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.5` · **Size:** medium
**Created:** 2026-11-03 16:11:30 EST · **Closed:** 2026-11-04 01:29:56 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

merge-cli: ship `bob task merge` (-i, -D, -s, -p) and the many-source `bob task move -t` mode on the shared shell, with teaching refusals, beautiful human output, JSON records, catalog and completion wiring, and generated reference docs.

## Notes

[2026-11-04T06:29:31Z · bob-cli-go.5] PROPOSED FOLLOW-UP: Merge re-points a dependent that lacks its own canonical [id::] but does not mint one, so live bob task reconcile drops the BLOCKS mirror entry it just wrote; MG fixtures always carry [id::] on dependents so MG17 never sees this shape. Reproduced on a hand-written vault with no merge involved; second reconcile converges with exit 0.

[2026-11-04T06:29:41Z · bob-cli-go.5] PROPOSED FOLLOW-UP: just docs-gen bob-docs gen step fails on sase/memory/glossary/task-merge.md having no front matter; pre-existing on the clean tree (this phase touched no memory files) and owned by the closeout phase that applies the accepted glossary strands.

[2026-11-04T06:29:56Z · bob-cli-go.5] merge-cli done: bob task merge (-i/-D/-s/-p, teaching refusals, human+JSON, unchanged-no-commit) and bob task move -t (typed-order staged moves, move_to_task/move_same_note, error.code) on the shared shell, wired into runner/completion/catalog/help with regenerated goldens and contract-note cleanup. Verified: cargo fmt clean, full clippy gate clean, cargo test --workspace all green (incl. 15 new task_merge CLI tests), live scratch-vault §2 example yields the After blocks with dependent re-point + mirror + LINKED FROM, reconcile exits 0 and converges. Two PROPOSED FOLLOW-UP notes recorded (BLOCKS mirror vs [id::]-less dependents; pre-existing bob-docs gen memory-strand failure).

## Dependencies

- **Blocks:** [bob-cli-go.10](bob-cli-go.10.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-go.3](bob-cli-go.3.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-go.4](bob-cli-go.4.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.9](bob-cli-go.9.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.5/README.md) | [bob-cli-go.5](bob-cli-go.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`497db44`](https://github.com/bobs-org/bob-cli/commit/497db446c52c4827bcd1d4955497a224b601e618) | feat(task-merge): ship bob task merge and bob task move -t | [bob-cli-go.5](bob-cli-go.5.md) | 2026-11-04 01:31:32 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.5][1] | Need full notes and fields | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.5/README.md

<!-- sase:referenced-by:end -->
