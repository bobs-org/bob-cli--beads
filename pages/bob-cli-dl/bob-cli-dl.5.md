# Bead: bob-cli-dl.5 — Obsidian relation writer folds Task Card Cancel into the source write

[Bead Pages](../README.md) / [bob-cli-dl](README.md) / bob-cli-dl.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2r.linker.w0.md) · **Assignee:** `bob-cli-dl.5` · **Size:** large
**Created:** 2026-10-28 08:15:27 EDT · **Closed:** 2026-10-28 10:07:46 EDT
**Plan:** [202610/relation\_cancel\_labels.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_cancel_labels.md)

## Description

nav-cancel-writer: mirror the vectors, add a cached cancel-label config loader and one pure planRelationCancelEffects planner, and fold planTaskCancelBatch into applyRelationEdit before stageWrite (one write, one undo). Extract a shared post-cancel helper (prune and recovery, no notice), show one composed notice, advance the walk once for a landed source, and re-plan at commit. Deploy with bob plugins sync.

## Notes

[2026-10-28T14:07:30Z · bob-cli-dl.5] nav-cancel-writer landed in bob-plugins. Explicit Links-to / Linked-from add/relabel into a configured cancel label cancels the source via planTaskCancelBatch; LINKS, checkbox, cancellation date, and existing-log prepend share one source-note transaction. Today's Pomodoro prune and cycler recoverBlockedDependents run through runPostCancelEffects. Writer never settles the walk (picker onClose does).

Verification: npm run build, npm test (3877 pass), npm run validate, npm run docs:check, bob plugins sync --no-pull -p bob-navigation-hotkeys. Vectors match bob-cli 52bff0161befe3ce9656117547920caaf3129644 byte-for-byte. sase bead epic-symbols bob-cli-dl.5: none.

Preview/commit contract for bob-cli-dl.6:
- Preview: planRelationCancelEffects over stage snapshots, then summarizeRelationCancelEffects(plan, day).
- Commit: pass expectedCancelEffects into applyRelationEdit. Writer reloads cancel labels/date, re-plans live snapshots, compares via relationCancelEffectsEqual (identities, edge/label keys, verdicts, day — not object identity).
- Stale: {ok:false, stale:true, cancelEffects} writes nothing. applyRelationCancelStaleToPicker keeps the stage open, stores the refreshed summary, clears relationCancelConfirmNonce, and best-effort refreshes the consequence strip. First stale Return refreshes; a second Return with the new summary can commit.
- Ordinary callers omit expectedCancelEffects and plan from current state.
- Composed notice: buildRelationCancelComposeNotice (CL6 wording, prune/recovery chips, LINKED FROM follow-up).

[2026-10-28T14:07:46Z · bob-cli-dl.5] Closed after npm test (3877), validate, docs:check, and bob plugins sync. Preview/commit contract for .6 is on the phase note. epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-dl.1](bob-cli-dl.1.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dl.6](bob-cli-dl.6.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dl.5.md) | [bob-cli-dl.5](bob-cli-dl.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@768fac8`](https://github.com/bobs-org/bob-plugins/commit/768fac86d256f6e7abd5c38fdff9a65c7fc4ed23) | feat(nav): cancel sources when linking a configured cancel label | [bob-cli-dl.5](bob-cli-dl.5.md) | 2026-10-28 10:14:57 EDT |
