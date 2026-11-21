# Bead: bob-cli-oo.4 — Space keymap, in-card note stage, stay-on-row commit, command, and docs

[Bead Pages](../README.md) / [bob-cli-oo](README.md) / bob-cli-oo.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5q.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5q.linker.w0.md) · **Assignee:** `bob-cli-oo.4` · **Size:** medium
**Created:** 2026-11-21 12:07:08 EST · **Closed:** 2026-11-21 16:01:52 EST
**Plan:** [202611/bank\_row\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_row_notes.md)

## Description

note-stage: reassign Space to the note stage and `-` to no-category, build the in-card stage and bankNoteCommit that never advances, add `Bank: note this row`, update e2e, plugin and bob-cli docs, and apply memory only per the decisions.

## Notes

[2026-11-21T21:01:20Z · bob-cli-oo.4] PROPOSED FOLLOW-UP: Docs word caps still fail lint on the clean base — bob-docs lint (just docs-check, npm run docs:check) exits 1 for docs/reference/plugins/bob-ledger-tools.md (6042 on base, 6033 after this phase, cap 6000; tracked by bob-cli-il) and docs/reference/plugins/bob-navigation-hotkeys.md (6307, untouched here). bob-docs build --strict and links pass. This phase kept its ledger-tools rewrite net-negative and left other features prose alone.

[2026-11-21T21:01:27Z · bob-cli-oo.4] PROPOSED FOLLOW-UP: Note-stage change chips show generic patterns — bankNoteNormalize (246a) reports changes as fixed strings ("[[target|alias]] → alias", "!! → ‼"), so the stage chips cannot show the concrete text the design example uses ("[[max]] → max"). Make the normalizer report the matched text per change and update test-ledger-tools-bank-note-write.cjs and the chip assertions in test-ledger-tools-bank-note-stage.cjs.

[2026-11-21T21:01:34Z · bob-cli-oo.4] PROPOSED FOLLOW-UP: Perf budget flakes under host load — npm test failed only "200-link / 2000-task build stays within the 25 ms budget" (test-ledger-tools-event-link-times.cjs) and "perf — one build over a 200-link ledger stays under 25 ms" (test-ledger-tools-frees-marks.cjs) at load average ~124; both pass in isolation (17 ms, 29 ms→pass on rerun). Same pair phase bob-cli-oo.3 saw; unrelated to bank code.

[2026-11-21T21:01:52Z · bob-cli-oo.4] Verified: bob-plugins (on fc754fa5) — Space opens an in-card note stage (new 248n fragment), '-' files/removes/acknowledges with no category, Delete aliases it in set mode, restricted Enter acknowledges only after the report settles (explicit modal.loading); bankNoteCommit writes one whole-line edit isolated via CM6 isolateHistory, saves with a reported outcome, keeps the cursor, re-captures the context, re-anchors the walk, counts session.notes (summary appends '· N notes'), never ticks/advances/jumps or flips didInteract; 'Bank: note this row' (bank-note-row) opens set mode directly in the stage, skips the report, refuses off-row and structured notes. New scripts/test-ledger-tools-bank-note-stage.cjs 21/21; bank card/model/UI/note-write/subscription/actions suites green; npm test 8410/8417 with only 2 host-load perf flakes (pass isolated); build:check current; all fragments <1000 lines; e2e updated (walk-dash, walk-note, walk-note-then-accept, note-preserving walk-undo) and its --self-test passes, but the real Obsidian run could not execute here (no obsidian or xvfb-run installed). Manifest 1.156.0; bob plugins sync deployed after the landed-build recipe for fc754fa5 (no -F). Docs: bob-ledger-tools.md keys + regenerated command table (page 6042->6033 words), bob-cli guide step 2 + If-it-goes-wrong, docs/bank.md Ownership; regenerated docs/reference/glossary.md (stale since oo.3's strand edit). bob-cli just check passes; just docs-check/npm run docs:check fail only on the two pre-existing over-budget pages (see follow-up); bob-docs build --strict and links pass. Memory: glossary:bank-row sentence was already added by oo.3 (dfe20ca3), nothing further; keymap decision record not written (reviewer said no). No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-oo.3](bob-cli-oo.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oo.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oo.4/README.md) | [bob-cli-oo.4](bob-cli-oo.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fc27bf1`](https://github.com/bobs-org/bob-cli/commit/fc27bf1ad8694d35bf5ce3729d7a2b3adb5f9d1e) | docs(bank): document the Category card note stage and regenerate the glossary | [bob-cli-oo.4](bob-cli-oo.4.md) | 2026-11-21 16:03:16 EST |
