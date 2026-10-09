# Bead: bob-cli-5s — Bob Refs: a quick-open panel in Bob Mac Capture that opens reference PDFs in Highlights

[Bead Pages](../README.md) / bob-cli-5s

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.5z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5z.md) · **Assignee:** `bob-cli-5s.land`
**Created:** 2026-10-08 19:32:40 EDT
**Plan:** [202610/bob\_refs\_panel.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/bob_refs_panel.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_refs_panel.md

<!-- sase:links:end -->

## Description

One keystroke (⌃⇧⌘R anywhere, or the Open… key while Highlights is frontmost) shows a prewarmed glass panel listing every PDF-backed reference note from `bob ref list`, with kind and reading state on every row, the working set first when the query is empty, tiered relevance when it is not, rows that never move under the cursor, and a kind-adaptive inspector. Return opens the original PDF in Highlights and changes nothing in the vault.

## Notes

[2026-10-09T11:55:30Z · bob-cli-5s.land] LAND TRIAGE (bob-cli-5s.land): PROPOSED FOLLOW-UP outcomes. (1) refs-panel thin-client decisions record (5s.1 #2, 5s.2 #1, 5s.3 #2, 5s.4 #1, 5s.5 #1, 5s.6 #1, 5s.7 #1, 5s.8 #1, 5s.9 #1): filed as memory task bob-cli-5u (ready; Bryan accepts or cancels; refs_decision_memory=no kept the epic from editing memory). (2) 9 return_links filter_* lib failures (5s.1 #1, 5s.9 #2): reproduced on b6ba7c3 with pandoc 3.1.3 (tests pin \hyperref[id], pandoc 3.1.3 emits \protect\hyperlink{id}); not epic-caused (bob-cli-5j code); filed as ci task bob-cli-5t, related to bob-cli-4u. (3) fakeBob live-preview waitUntil flakes in CapturePanelModelTests (5s.2 #2/#4, 5s.6 #2): semantic duplicate of bob-cli-4k (twin StartPending test, same wait class); +1 recorded there. (4) 5s.4 #2 'run Swift build/tests/CI': declined, superseded by 5s.4 #4 and green CI on every later phase (2016864 run 37919892089). (5) 5s.6 #3 ImageRenderer fixture limits: declined as a task, guidance only and already applied by 5s.8; the child closeout plan keeps the workarounds. (6) 5s.7 #2 master CI red on inspector compile errors: declined, resolved by d1689b3/f5f6178 and green runs 37918351904/37919892089. (7) 5s.8 #2 anchor the Cmd-K menu below the selected row: caused by the epic (spec section 10 requires 'popped up below the selected row; when the row frame is unknown, at the list's center'), so it is remaining epic work in the child plan, not a task.

[2026-10-09T11:59:12Z · bob-cli-5s.land] LAND AUDIT (bob-cli-5s.land, before child plan): Read all 9 closed phases and notes, the plan, and every epic commit (bob-cli 4c9cdbe, a4c69ff, b6ba7c3; bob-mac-capture 65ab7ee..2016864). macOS CI green at 2016864 (run 37919892089); no --epic-symbol entries. Drift: no non-epic commits landed in bob-cli or bob-mac-capture since the epic started, so nothing to integrate. Remaining epic-caused work, confirmed in source: (1) CRITICAL: RefsSearchBar onTextChange drops the typed string, so model.query stays empty and search does not work; (2) the open-error re-show calls show() -> prepareForPresentation(), wiping query and pendingOpen, so Try Again and Open in Default App do nothing, and it bypasses BobPanelCoordinator; (3) the wake observer is on NotificationCenter.default instead of NSWorkspace's center; (4) Today is not refreshed on every open; the -g pass runs inside refs-list, so a git failure discards the snapshot; (5) AppDelegate @Published sinks re-read the old value, so the ⌃⇧⌘R toggle is inverted; (6) section 5.5 unavailable rows are dropped instead of dimmed (README claims dimmed); (7) 2-char word prefixes never reach T1; ranker uses UTC days; Ready sorts by last-opened, not added desc; git dates not marked approximate; (8) the 3 s intrinsics timeout cannot fire; the Cmd-K menu is anchored at the mouse, not the selected row; content well, Reduce Transparency base, and per-show scale-in are missing; inspector honesty violations ('Unknown date', 'Added Added', '0 open'); (9) dead symbols, refs-piece debug renders, README gaps; (10) bob-cli: a4c69ff committed stray .build/ Swift cache files, blocked key order, missing several-trackers test, docs/ref.md client/additive notes. Planned as child epic sase_plan_bob_refs_land_fixes.md (phases cli-blocked-polish, refs-core-fixes, refs-model-fixes, refs-ui-fixes).

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-5s.1](bob-cli-5s.1.md) | bob-cli exposes Blocked on ref rows | ✓ closed | small | 2026-10-08 | 1 | 1 |
| [bob-cli-5s.2](bob-cli-5s.2.md) | Hotkey registry and CI render artifacts in Bob Mac Capture | ✓ closed | small | 2026-10-08 | 1 | 0 |
| [bob-cli-5s.3](bob-cli-5s.3.md) | RefsCore target — decoding, item model, fetcher, and stores | ✓ closed | medium | 2026-10-08 | 1 | 0 |
| [bob-cli-5s.4](bob-cli-5s.4.md) | RefsCore ranking — browse sections, search tiers, stability, explanations | ✓ closed | medium | 2026-10-08 | 1 | 1 |
| [bob-cli-5s.5](bob-cli-5s.5.md) | Refs library service and panel model | ✓ closed | medium | 2026-10-08 | 1 | 0 |
| [bob-cli-5s.6](bob-cli-5s.6.md) | Refs panel window, list, basic inspector, and keyboard | ✓ closed | medium | 2026-10-08 | 1 | 0 |
| [bob-cli-5s.7](bob-cli-5s.7.md) | Hotkeys, Highlights takeover, menu, settings, and coexistence with Capture | ✓ closed | medium | 2026-10-08 | 1 | 0 |
| [bob-cli-5s.8](bob-cli-5s.8.md) | Kind-adaptive inspector and actions menu | ✓ closed | medium | 2026-10-08 | 1 | 0 |
| [bob-cli-5s.9](bob-cli-5s.9.md) | README coherence, optional memory record, final CI, and Bryan's checklist | ✓ closed | small | 2026-10-08 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-5s: Bob Refs: a quick-open panel in Bob Mac Capture that opens reference PDFs in Highlights [in_progress]"]
    n1["bob-cli-5s.1: bob-cli exposes Blocked on ref rows [closed]"]
    n2["bob-cli-5s.10: Bob Refs landing fixes: make search, error recovery, refresh, ranking, and the inspector match the bob_refs_panel spec [in_progress]"]
    n3["bob-cli-5s.10.1: bob-cli blocked-field polish and stray .build cleanup [closed]"]
    n4["bob-cli-5s.10.2: RefsCore ranking, captions, dates, and refs-rank fixes [closed]"]
    n5["bob-cli-5s.10.3: Search binding, open-error re-show, unavailable rows, refresh triggers, and live settings [in_progress]"]
    n6["bob-cli-5s.10.4: Panel visuals, inspector honesty, ⌘K anchor, cleanup, README, and final CI [in_progress]"]
    n7["bob-cli-5s.2: Hotkey registry and CI render artifacts in Bob Mac Capture [closed]"]
    n8["bob-cli-5s.3: RefsCore target — decoding, item model, fetcher, and stores [closed]"]
    n9["bob-cli-5s.4: RefsCore ranking — browse sections, search tiers, stability, explanations [closed]"]
    n10["bob-cli-5s.5: Refs library service and panel model [closed]"]
    n11["bob-cli-5s.6: Refs panel window, list, basic inspector, and keyboard [closed]"]
    n12["bob-cli-5s.7: Hotkeys, Highlights takeover, menu, settings, and coexistence with Capture [closed]"]
    n13["bob-cli-5s.8: Kind-adaptive inspector and actions menu [closed]"]
    n14["bob-cli-5s.9: README coherence, optional memory record, final CI, and Bryan's checklist [closed]"]
    n0 --> n1
    n0 --> n2
    n2 --> n3
    n2 --> n4
    n2 --> n5
    n2 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n0 --> n14
    n1 -.-> n8
    n1 -.-> n14
    n3 -.-> n6
    n4 -.-> n5
    n5 -.-> n6
    n7 -.-> n11
    n7 -.-> n12
    n8 -.-> n9
    n9 -.-> n10
    n10 -.-> n11
    n11 -.-> n12
    n11 -.-> n13
    n12 -.-> n14
    n13 -.-> n14
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5s.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.1/README.md) | [bob-cli-5s.1](bob-cli-5s.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-5s.10.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.10.1/README.md) | [bob-cli-5s.10.1](bob-cli-5s.10.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-5s.10.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.10.2/README.md) | [bob-cli-5s.10.2](bob-cli-5s.10.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-5s.10.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.10.3/README.md) | [bob-cli-5s.10.3](bob-cli-5s.10.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-5s.10.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.10.land/README.md) | [bob-cli-5s.10](bob-cli-5s.10.md) | 0 |
| [bbugyi200.apollo.bob-cli-5s.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.2.md) | [bob-cli-5s.2](bob-cli-5s.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-5s.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.3.md) | [bob-cli-5s.3](bob-cli-5s.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-5s.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.4/README.md) | [bob-cli-5s.4](bob-cli-5s.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-5s.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.5.md) | [bob-cli-5s.5](bob-cli-5s.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-5s.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.6/README.md) | [bob-cli-5s.6](bob-cli-5s.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-5s.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.7/README.md) | [bob-cli-5s.7](bob-cli-5s.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-5s.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.8/README.md) | [bob-cli-5s.8](bob-cli-5s.8.md) | 0 |
| [bbugyi200.apollo.bob-cli-5s.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.9/README.md) | [bob-cli-5s.9](bob-cli-5s.9.md) | 1 |
| [bbugyi200.apollo.bob-cli-5s.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.land.md) | [bob-cli-5s](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4c9cdbe`](https://github.com/bobs-org/bob-cli/commit/4c9cdbe583770f6fa487be18af6615f259e3bf01) | feat(refs): expose Blocked as always-present boolean on ref rows | [bob-cli-5s.1](bob-cli-5s.1.md) | 2026-10-08 20:18:06 EDT |
| bob-cli | [`a4c69ff`](https://github.com/bobs-org/bob-cli/commit/a4c69ff8964d85d4340682af9e4a11d8253eb049) | chore(build): record Swift build cache from RefsCore verification | [bob-cli-5s.4](bob-cli-5s.4.md) | 2026-10-09 01:19:19 EDT |
| bob-cli | [`b6ba7c3`](https://github.com/bobs-org/bob-cli/commit/b6ba7c3387675e9723e416acbbc0c08543137ca0) | docs(readme): document blocked display-only overlay field | [bob-cli-5s.9](bob-cli-5s.9.md) | 2026-10-09 07:25:33 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5s.2][1] | Need epic scope for phase work | 1 |
| read-by | [agent:bob-cli-5s.3][2] | epic context for phase worker | 1 |
| read-by | [agent:bob-cli-5s.4][3] | Need epic scope for phase work | 2 |
| read-by | [agent:bob-cli-5s.7][4] | find inspector phase bead id for follow-up citation | 1 |
| read-by | [agent:bob-cli-5s.8][5] | Need epic status and prior phase progress for inspector work | 1 |
| read-by | [agent:bob-cli-5s.9][6] | epic scope for closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-5s.3.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.7/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.8/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5s.9/README.md

<!-- sase:referenced-by:end -->
