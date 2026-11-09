# Bead: bob-cli-j0.2 — Make block-ID renames one undo step and undo-coherent across notes

[Bead Pages](../README.md) / [bob-cli-j0](README.md) / bob-cli-j0.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.d4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.d4.md) · **Assignee:** `bob-cli-j0.2` · **Size:** medium
**Created:** 2026-11-09 07:43:10 EST · **Closed:** 2026-11-09 08:14:29 EST
**Plan:** [202611/lost\_task\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/lost_task_guards.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | [bead:bob-cli-j1][1] | Phase proposed the older generic multi-edit split-undo defect |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-j1/README.md

<!-- sase:links:end -->

## Description

rename_atomic: reproduce the split undo in real Obsidian, apply each note's rename edits as one editor transaction, write closed notes with a compare-and-swap, and follow an undone rename across notes.

## Notes

[2026-11-09T13:13:56Z · bob-cli-j0.2] Reproduced the split undo in real Obsidian 1.15 (athena, xvfb, scratch vault) with scripts/obsidian-block-id-rename-e2e.cjs against block-id-prompt 1.37.0: after the rename through the real modal, ONE vim `u` (and ONE editor.undo()) left bob.md ids ["new-id","old-id"] (task ^id reverted, same-note BLOCKS link still ^new-id) and daily/done notes on ^new-id: 3 dangling links, exactly the 2026-11-09 commit d6d6ba958 shape. That reproduction fully accounts for the observed state, so the stale-snapshot theory was not needed; I did not exhaustively audit the status-cycler/freshness/review-walk line writers beyond that.

[2026-11-09T13:14:03Z · bob-cli-j0.2] Landed in bob-plugins (block-id-prompt 1.38.0): new fragments 155-block-rename-writes.js (one editor.transaction per open note, vault.process compare-and-swap per closed note, closed-note rollback) and 157-block-rename-follow.js (session record, 30 min window, undo/redo follow into recorded notes, ambiguity refusal + sticky Notice per decision undo_follows_rename = yes). Rename plan now carries the destination ^id edit in the destination note edit list. Real-Obsidian e2e passes 29/29 cases twice on 1.38.0 (vim u, editor.undo with the other note open in a split, redo, ambiguous note); unit tests in scripts/test-block-id-prompt-rename-atomic.cjs; npm test 5777 pass, npm run validate and docs:check green.

[2026-11-09T13:14:11Z · bob-cli-j0.2] PROPOSED FOLLOW-UP: other multi-edit gestures in block-id-prompt still apply a planned edit list as sequential editor.replaceRange calls, which keeps the same split-undo shape (task line + same-note link or Pomodoro link as separate undo events): applyTargetTaskPlan (140 source/targetEditor loops), completeTaskSourceLink (140, non-"((" path), 120-plugin-pomodoro-links.js (~682, ~835), 129-plugin-task-wikilink-pomodoro.js (~538), submitDirectBlockAdd (110) — apply each as one editor.transaction like 155-block-rename-writes.js does.

[2026-11-09T13:14:18Z · bob-cli-j0.2] Deployed block-id-prompt 1.38.0 with bob plugins sync on apollo (~/bob) and on the Mac via ssh mac (main.js sha256 f0629939...89fd matches the repo build). Both stamps are source_head 77c34f1 with dirty=dirty because the commit lands after this turn (apollo synced from this workspace clone, the Mac from an rsync copy at /tmp/bob-plugins-j02); once the commit is on origin a bare bob plugins sync from each canonical checkout overwrites the stamp cleanly. Obsidian on the Mac must reload the plugin (or restart) to run 1.38.0.

[2026-11-09T13:14:29Z · bob-cli-j0.2] Verified: real-Obsidian e2e reproduced the split undo on 1.37.0 and passes 29/29 (twice) on 1.38.0 (vim u, editor.undo, split-open note, redo, ambiguous-note sticky Notice); unit tests for single-transaction writes, closed-note compare-and-swap + rollback, undo/redo follow and ambiguity refusal pass; npm test (5777 pass), npm run validate and docs:check green; 1.38.0 deployed to apollo and the Mac (hash matches repo). Commit pending in bob-plugins.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j0.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j0.2/README.md) | [bob-cli-j0.2](bob-cli-j0.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5e5e33b`](https://github.com/bobs-org/bob-plugins/commit/5e5e33b60f008c95fcd14b2ecbc2d71a9c30dfcd) | feat(block-id-prompt): make block-ID renames one undo step across notes | [bob-cli-j0.2](bob-cli-j0.2.md) | 2026-11-09 08:15:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j0.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j0.2/README.md

<!-- sase:referenced-by:end -->
