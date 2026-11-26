# Bead: bob-cli-q5.3.1.2 — Apply capture snooze operations atomically

[Bead Pages](../README.md) / [bob-cli-q5.3.1](bob-cli-q5.3.1.md) / bob-cli-q5.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.3.md) · **Assignee:** `bob-cli-q5.3.1.2` · **Size:** medium
**Created:** 2026-11-25 19:34:28 EST · **Closed:** 2026-11-26 04:14:15 EST
**Plan:** [202611/capture\_snooze\_token.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_snooze_token.md)

## Description

mutation: connect snooze add/drop to capture snapshots for existing and new tasks, preserve row notes when linking now, implement retime and drop, and verify refusals and whole-batch atomicity.

## Notes

[2026-11-26T08:45:04Z · bob-cli-q5.3.1.2] PROPOSED FOLLOW-UP: Numeric-route snooze-drop preview disagrees with execution — capture-parse -f json -- "@20261125:here!" returns mode=task and body="@20261125:here" while capture correctly drops the active row by basename; the editor masks the bang then falls through the existing alphabetic-route candidate guard. Existing parser code is unchanged by this mutation phase.

[2026-11-26T08:47:56Z · bob-cli-q5.3.1.2] PROPOSED FOLLOW-UP: Clarify or fix relative snooze rounding — the shared core parser rounds the duration, not the resulting wall clock: at 12:03, +45m resolves to 12:48 and +1h to 13:03. docs/snooze.md says relative targets round upward to a five-minute boundary. Capture intentionally reuses the unchanged core parser; the mutation regression pins its actual result rather than adding divergent capture-only rounding.

[2026-11-26T09:01:10Z · bob-cli-q5.3.1.2] Mutation interface handoff for completion/docs: capture now executes existing/new z:<when>, retime, strict @route:id! drop, and ordinary link-now row cleanup through staged core planners. Result schema stays 1 / grammar 33. The optional item.snooze object has action=add|retime|drop|link_now, canonical route including .md, block_id, vault-relative daily_file; add/retime also carry time (HHMM), wake_at (RFC3339), and row (one-based final settled coordinate, omitted if a later item removes it). Drop/link_now omit time/wake_at/row. Unrelated captures omit snooze. Existing add/drop use kind=snooze; new tasks and ordinary link-now retain their ordinary kind. Human add/retime preview says snoozed until HH:MM and has no fictional Pomodoro block. All existing task/link construction and core time semantics are reused. No memory or documentation files edited by this phase.

[2026-11-26T09:03:31Z · bob-cli-q5.3.1.2] PROPOSED FOLLOW-UP: Repair pre-existing full-check failures — full check ToolRun d9f6d1470d4fa55a51b0d07d48d1089f passed formatting/lint and 13,162 tests but failed 43 lib + 55 CLI tests. With all phase changes stashed and git status clean on base 1c23bce7, ToolRun 549282d9b014e9ca187b04e3ed57d52c reran all 98 exact failing names: all 98 failed identically after normalizing only thread/panic coordinates, generated temporary directory instance IDs, and the RUST_BACKTRACE hint. Most failures are legacy drawer/layout/completion fixtures; others cover note-pull/project-note previews, task status placement, and the wispr_summary PDF kicker. bob-cli-q9 already tracks the identical wispr_summary failure. The closed bob-cli-h5 covered an older note-pull fixture issue, not these newly reproduced differences. No new task bead created; land agent should triage these base failures. All phase changes were restored after comparison.

[2026-11-26T09:13:59Z · bob-cli-q5.3.1.2] Completed mutation implementation. Existing and new task snoozes, retime/drop, same-note edits, canonical identity deduplication, retained nested notes, running-first/next-up link-now cleanup without receipts, core time/refusal semantics, staged dependency eligibility, minted-ID collisions, final row coordinates, and atomic guarded writes are covered. Final ToolRun d91dbe34a32be4444af3d68d7c6a59e4 passes cargo fmt, the full just lint gate, and cargo test --lib --test cli snooze (62 unit + 48 CLI tests). The read-drift test exercises retime and link-now against task, daily-note, prerequisite, and vault-membership changes. Full check and all 98 clean-base failure reproductions are recorded in note #4; these unrelated failures do not keep this phase open. Numeric drop-preview parity and relative-time documentation follow-ups remain in notes #1/#2 for land triage; completion/docs has the additive result contract in note #3. No memory changes, version changes, or ancestor closure performed.

[2026-11-26T09:14:15Z · bob-cli-q5.3.1.2] Implemented atomic capture snooze add/retime/drop and note-preserving link-now. Final formatting and full lint pass; 62 unit and 48 CLI snooze tests pass. Full-check 98 failures reproduce identically on clean base 1c23bce7 and are recorded for land triage. No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-q5.3.1.1](bob-cli-q5.3.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-q5.3.1.3](bob-cli-q5.3.1.3.md) ◐ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.2/README.md) | [bob-cli-q5.3.1.2](bob-cli-q5.3.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ae78dbb`](https://github.com/bobs-org/bob-cli/commit/ae78dbb2dbcd61ce5b8cc9a0dd4db904d93ea745) | feat(capture): apply snooze operations atomically | [bob-cli-q5.3.1.2](bob-cli-q5.3.1.2.md) | 2026-11-26 04:15:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.3.1.2][1] | Recheck acceptance criteria and record clean-base verification before closing | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q5.3.1.2/README.md

<!-- sase:referenced-by:end -->
