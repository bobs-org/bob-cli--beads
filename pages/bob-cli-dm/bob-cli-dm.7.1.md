# Bead: bob-cli-dm.7.1 — Task Card theme editing and successor retargeting

[Bead Pages](../README.md) / [bob-cli-dm.7](bob-cli-dm.7.md) / bob-cli-dm.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-dm.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.7.md) · **Assignee:** `bob-cli-dm.7.1.land`
**Created:** 2026-10-28 22:50:54 EDT · **Closed:** 2026-10-29 01:06:45 EDT
**Plan:** [202610/task\_card\_successor\_themes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_card_successor_themes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/task_card_successor_themes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_card_successor_themes.md

<!-- sase:links:end -->

## Description

Task Cards explain and edit task themes, and deliberate successor retargets remember the correct task theme without changing ordinary placement or freshness behavior.

## Notes

[2026-10-29T04:28:40Z · bob-cli-dm.7.1.land] FOLLOW-UP TRIAGE before remaining-work tale: collected every proposal: dm.7.1.3 #1 and dm.7.1.4 #1 both report generated docs/reference/glossary.md drift. Used sase_new_task, searched CI and all task types, swept last-week tasks and active epics. Independently reproduced via bob-docs gen --check on clean bob-cli 8b4d1b89 / plugins 21f2a0e; plugin inventory is current. Cause is root-parent memory commit 8b4d1b89 (bob-cli-e2.2) without generated glossary output. Recorded one DISCOVERED ISSUE on active bob-cli-e2 (e2.4 owns remaining docs), identifying both proposing beads. Declined a separate task because the two proposals are one defect owned by that active epic. No other proposals. Epic-caused Task Card runtime defects remain dm.7.1 work and are going into the bounded remaining-work tale, not follow-up tasks.

[2026-10-29T04:30:20Z · bob-cli-dm.7.1.land] LAND AUDIT (remaining work, do not close yet): read this epic, all four children and all 6 child notes, the approved plan, parent dm.7 scope/DECISIONS, implementation commits 14b4fda/1c9e0e1/acd96d4/21f2a0e, and source projection/stage/modal/normalizers/successor planner/runtime writers. Read-only focused suites (theme edit, successor picker, successor theme write, successor wiring) pass 56 tests. Extended the existing modal-harness in memory on plugins 21f2a0e: typed Brand New -> [] visible rows; openItemAtIndex(1) -> 0 calls to applyTaskCardThemeChoice; refresh changes selected theme-fix -> __default; inherited WRITE -> BUILD still reaches writer with action clear/inherited BUILD. Root causes: 352 commit rejects the opening flag that the base picker intentionally sets; 410 has no dynamic theme query branch; 352 preserves a key only on commit; applyTaskCardThemeChoice plans from a fresh projection instead of the shown one, and linked persistence does not re-resolve inheritance after its async read. Further gaps: 315 reserves known inherited keys before adding their Today/Recent row, and unavailable/malformed caps fail open; 330 renders header theme as plain bracketed text without PT6 hue pill while 352 uses a place-style dot for theme choices. The promised successor preservation coverage uses helper replacements, lacks actual roll/Alt+P coverage, and needs runtime writer assertions. These are epic work, covered by a medium tale with this epic and parent phase closeout in its final step. Drift reviewed: only interleaved plugin commit 0fb4b92 adds root marks via the theme-render lifecycle; retain that integration and root bytes. Primary later commits 818b8755 and 8b4d1b89 add root attribution/glossary, plus ce9f9e78 relation rollout docs since epic creation; no duplicate theme writer introduced. DECISIONS honored: no memory edits, ledger pills/seed remain parent siblings. No epic-symbol entries. Primary/plugin trees were clean; manual desktop UI unverified; old nav provenance refusal must be rechecked by repair coder without force. Follow-up disposition is recorded separately above.

[2026-10-29T05:06:45Z · bob-cli-dm.7.1.land] Completed the approved Task Card theme lifecycle and guarded successor retarget work. Repaired base-picker single-flight commit handling, dynamic typed-name filtering, selection/query preservation across refresh, shown-context guards, linked full-note inheritance recomputation, fail-closed caps, known inherited choice visibility, truthful theme hue presentation, and the ledger-tools runtime registry lookup that had silently skipped successor theme persistence. Preserved interleaved root-mark lifecycle integration from plugin commit 0fb4b92 and verified bracket and supported parenthesized theme bytes through actual close, move, roll, and Alt+P writers. Re-read this epic and all four closed children with their notes; reran epic-symbols with no entries. Audited implementation commits 14b4fda, 1c9e0e1, acd96d4, 21f2a0e and retained 0fb4b92. Focused runtime integration suites passed 82/82; npm test passed 4203 tests; npm run validate passed; host just check via sase tool run check succeeded (Rust suite 3894 tests). npm run docs:check remains blocked only by generated docs/reference/glossary.md drift from bob-cli-e2.2 commit 8b4d1b89 on clean base; plugin inventory is current. Both duplicate proposals dm.7.1.3 #1 and dm.7.1.4 #1 were triaged as one discovered issue on active bob-cli-e2, with e2.4 owning the remaining docs; no duplicate task was created and no memory was edited. task-status-cycler sync succeeded. bob-navigation-hotkeys sync was refused by the provenance guard because another checkout deployed an uncommitted build at c59819c; did not force. Obsidian was not running, so manual desktop/undo checks remain unverified. just symvision is unavailable because no recipe exists in the Justfile.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.7.1.land.md) | [bob-cli-dm.7.1](bob-cli-dm.7.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@2e1e881`](https://github.com/bobs-org/bob-plugins/commit/2e1e881d6e03edf33f85b030cccd7016aebb85ae) | feat(navigation): harden Task Card theme editing and successor writes | [bob-cli-dm.7.1](bob-cli-dm.7.1.md) | 2026-10-29 01:09:11 EDT |
| bob-cli--plans | [`bob-cli--plans@3fa1625`](https://github.com/bobs-org/bob-cli--plans/commit/3fa16255a1e2995fc8eac38a51c7e4e9321cd51b) | docs(plans): mark completed Task Card theme plan done | [bob-cli-dm.7.1](bob-cli-dm.7.1.md) | 2026-10-29 01:10:08 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.7.1.1][1] | Need the parent epic decisions and any phase instructions | 1 |
| read-by | [agent:bob-cli-dm.7.1.3][2] | Need parent epic DECISIONS and phase list | 1 |
| read-by | [agent:bob-cli-dm.7.1.4][3] | Need parent epic scope and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.7.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.7.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.7.1.4/README.md

<!-- sase:referenced-by:end -->
