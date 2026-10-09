# Bead: bob-cli-5s.10 — Bob Refs landing fixes: make search, error recovery, refresh, ranking, and the inspector match the bob\_refs\_panel spec

[Bead Pages](../README.md) / [bob-cli-5s](README.md) / bob-cli-5s.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.bob-cli-5s.land` · **Assignee:** `bob-cli-5s.10.land`
**Created:** 2026-10-09 08:04:27 EDT · **Closed:** 2026-10-09 11:57:12 EDT
**Plan:** [202610/bob\_refs\_land\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_land_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/bob_refs_land_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_land_fixes.md

<!-- sase:links:end -->

## Description

Finish epic bob-cli-5s. Close every gap its land audit found between the shipped Bob Refs panel and plan:202610/bob_refs_panel.md: typed queries reach the model, an open error re-shows the panel with its state and working buttons, unavailable rows stay in place dimmed, refresh fires on wake and every open, ranking follows the spec tables in local days, the inspector tells the truth, the ⌘K menu anchors at the row, and bob-cli drops stray Swift build files and finishes the blocked-field contract.

## Notes

[2026-10-09T12:58:48Z · bryanbugyi34@gmail.com] I think we've broken bob-mac-capture's 'just install' command. See 🔒 bob\_mac\_capture\_install\_error.txt for context.

[2026-10-09T15:54:02Z · bob-cli-5s.10.land] FOLLOW-UP TRIAGE (bob-cli-5s.10.land), before the remaining-work tale.

(1) bob-cli-5s.10.1 note #1 — completion CLI tests flake run-to-run (bash/readline/protocol/vault subsets fail with disjoint sets on the base tree and on the phase tree; zero references to ref_library). Not caused by this epic. Same load-timing class already owned by in-progress epic bob-cli-3j (notes #4, #7, #8, #9, #10: unset 150 ms BOB_COMPLETE_DEADLINE_MS, wall-clock budgets, zpty sleeps). No task bead exists for it. Recorded as a DISCOVERED ISSUE on bob-cli-3j. No new task.

(2) bob-cli-5s.10.2 note #2 — base just check stays red on the return_links Pandoc failures. Duplicate of ready task bob-cli-5t (the same 9 filter_* tests; Pandoc 3.1.3 emits \protect\hyperlink{id} where the tests pin \hyperref[id]). Already filed by bob-cli-5s.land from phases 5s.1 and 5s.9. This phase named that task and reported no new failure. Declined as a new task. No +1: this landing did not re-run those tests.

(3) Epic note #1 — bob-mac-capture just install failed on multiline string interpolations in RefsCaption.swift. Caused by this epic (phase 10.2). Fixed by 9c46702, which hoists those calls out of the interpolations. Current RefsCaption.swift has no multiline \( interpolations. Later CI is green through d5fcac0 (run 37949647297). Not remaining work.

(4) bob-cli-5s.10.4 note #1 FLAKE NOTE — RefsLibraryTests.testRefreshIfStale failed 4-vs-3 argv twice on final SHA d5fcac0 and passed on the --failed rerun (run 37949647297). Caused by this epic. The git-date lane publishes the snapshot (lastSuccessAt) and then writes a later argv=ref list -g line. The test waits for Today and not for that lane, then compares argv counts across a 1 s quiet window. The wake test already settles the same lane by waiting until ref/blogs/small_opened.md has added (4dcd5f0). This is remaining epic work, planned as a tale. Not a separate task.

(5) panelPresenter stays assigned to show() and is never called (phase 10.3's note to 10.4). Declined. Open-error re-show goes through panelRepresenter and BobPanelCoordinator.representRefs, which is the spec path. The named dead-symbol list in refs-ui-fixes did not include panelPresenter.

Integration: no non-epic commits landed in bob-cli or bob-mac-capture after this epic's first commit. bob-cli HEAD is b566ba4 (phase 10.1). bob-mac-capture HEAD is d5fcac0, and every commit after parent-epic 2016864 belongs to this epic. Nothing to retarget onto the new Refs behavior.

[2026-10-09T15:57:12Z · bob-cli-5s.10.land] LAND bob-cli-5s.10. Verified all four closed phases against the plan and the epic commits (bob-cli b566ba4; bob-mac-capture 3a5fd4a..d5fcac0). Blocked sits after reading_state_source, .build is untracked, the two-tracker [?] fixture asserts blocked == false, and docs/ref.md records the client note and schema_version 1 additivity. Refs behavior matches the land audit: setQuery, represent-without-reset through BobPanelCoordinator, unavailable rows kept and dimmed, workspace wake, Today on every open, git lane after publish, calendar days, Ready added-desc, approximate git dates, weekday 2...6, frecencyHalfLifeDays, prepared-item cache, refs-rank --now, content well, Reduce Transparency, inspector honesty, 3 s intrinsics timeout, and row-anchored Cmd-K. highlights_open_key stays cmdO. No memory edits. Final CI https://github.com/bobs-org/bob-mac-capture/actions/runs/37949647297 is green on d5fcac0 after a --failed rerun. No non-epic commits landed in either repo after the epic started. Follow-ups, also in epic note #2: completion CLI flakes recorded on bob-cli-3j (not this epic); return_links declined as duplicate of bob-cli-5t; the just-install RefsCaption parse break was fixed by 9c46702; panelPresenter left unused and declined because represent is the spec path. Remaining race fixed here: testRefreshIfStale now waits for the git-date backfill of ref/blogs/small_opened.md before sampling argv counts, the same settle the wake test uses, so a late -g line cannot fail the quiet-window compare. No --epic-symbol entries.

## Attachments

- 🔒 bob\_mac\_capture\_install\_error.txt · text/plain · 8.21582 KiB (private attachment)

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5s.10.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-5s.10.land.md) | [bob-cli-5s.10](bob-cli-5s.10.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@a87859f`](https://github.com/bobs-org/bob-mac-capture/commit/a87859f251b10346b60051ff713291bd71cb8f78) | fix(refs): settle the git-date lane in testRefreshIfStale before the argv baseline | [bob-cli-5s.10](bob-cli-5s.10.md) | 2026-10-09 12:20:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.10.1][1] | epic decisions context | 1 |
| read-by | [agent:bob-cli-5s.10.2][2] | Need parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-5s.10.3][3] | epic decisions | 1 |
| read-by | [agent:bob-cli-5s.10.4][4] | Need epic decisions and plan scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5s.10.4/README.md

<!-- sase:referenced-by:end -->
