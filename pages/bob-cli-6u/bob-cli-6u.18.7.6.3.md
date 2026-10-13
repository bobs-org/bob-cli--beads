# Bead: bob-cli-6u.18.7.6.3 — Task-status-cycler cross-note project reasons, Alt+\[ and transcluded ^prj recovery

[Bead Pages](../README.md) / [bob-cli-6u.18.7.6](bob-cli-6u.18.7.6.md) / bob-cli-6u.18.7.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.18.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.18.7.land.md) · **Assignee:** `bob-cli-6u.18.7.6.3` · **Size:** medium
**Created:** 2026-10-12 22:09:27 EDT · **Closed:** 2026-10-12 22:27:15 EDT
**Plan:** [202610/prj\_line\_blocking\_final\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_final_audit_fixes.md)

## Description

cycler-fixes: resolve cross-note Depends-On ids when deciding whether a ^prj still blocks, recover residents when ^prj leaves Blocked for any status and when it is cycled through a transclusion, split the block-id resident test, tighten the notice-order test, and restore the cycler README row.

## Notes

[2026-10-13T02:26:55Z · bob-cli-6u.18.7.6.3] cycler-fixes complete. All five audit findings were real and are fixed in task-status-cycler 1.34.0 (block-id-prompt src unchanged, tests only).

1. Cross-note Depends-On ids are resolved against the vault (Tasks cache when Warm, else markdown scan via readSuccessorNoteText) before planning. Only an id that resolves to an open task is a remaining project or own-reason; a missing id never blocks (DC7). recoverProjectResidentsAfterPrjUnblock resolves first, then plans.
2. Cycling ^prj out of [?] to any non-Blocked status recovers tagged open residents, including Alt+[ to Cancelled when the note is no longer project(T).
3. A transcluded ^prj recovers residents in its source note through vault.process (no editor).
4. block-id-prompt: resident consumption is its own test; notice-order asserts /^Project blocked by dependency · / (not the Task blocked · project reason fallback).
5. README cycler row restored the tagged-residents sentence, dropped nav prune-live-links text, fixed the stray double space, and describes 1–3. Manifest 1.33.0 → 1.34.0.

Regression tests in test-task-status-cycler-blocked-schedule.cjs fail on the pre-fix fragments (reverted 088/160/180, rebuilt, 5 failures) and pass with the fix. Vectors: DC7 missing-id, PDB resident recovery, UB WRITE [unblocked::] via ledger-tools v12.

npm test: 2554 pass, 6 fail — the allowed bob-cli-6v (4 unblocked-glyph), bob-cli-6w (Keep counts once), bob-cli-3w (stage-ranker timing). npm run validate ok. Deployed task-status-cycler on this host (bob plugins sync -n -r opened bob-plugins -p task-status-cycler). No memory notes edited. No epic-symbols on this phase.

[2026-10-13T02:27:15Z · bob-cli-6u.18.7.6.3] Verified: cross-note Depends-On ids resolve before resident recovery (closed target recovers, open target keeps tags, resident own closed prereq recovers); Alt+[ to Cancelled and transcluded ^prj recover residents; five new tests fail on pre-fix cycler fragments; block-id-prompt resident case split and notice-order exact; cycler README/manifest 1.34.0; npm test 2554 pass with only allowed 6v/6w/3w failures; validate ok; deployed task-status-cycler on this host.

## Dependencies

- **Blocks:** [bob-cli-6u.18.7.6.4](bob-cli-6u.18.7.6.4.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.7.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.6.3/README.md) | [bob-cli-6u.18.7.6.3](bob-cli-6u.18.7.6.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`332e507`](https://github.com/bobs-org/bob-cli/commit/332e507b13576df7d0a7b521dae01776f703791d) | docs(task-dependencies): document cycler ^prj resident recovery | [bob-cli-6u.18.7.6.3](bob-cli-6u.18.7.6.3.md) | 2026-10-12 22:28:46 EDT |
| bob-plugins | [`bob-plugins@7303ff4`](https://github.com/bobs-org/bob-plugins/commit/7303ff464ed3b3d1d103d942e8448b603759f8d5) | fix(task-status-cycler): resolve cross-note ^prj reasons before recovery | [bob-cli-6u.18.7.6.3](bob-cli-6u.18.7.6.3.md) | 2026-10-12 22:30:17 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6u.18.7.6.3][1] | Need full notes, DECISIONS, and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.7.6.3/README.md

<!-- sase:referenced-by:end -->
