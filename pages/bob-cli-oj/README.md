# Bead: bob-cli-oj — \[N / \]N group jumps for days, periods, records, and any note

[Bead Pages](../README.md) / bob-cli-oj

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.land`
**Created:** 2026-11-21 07:41:34 EST · **Closed:** 2026-11-21 21:12:51 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bracket_n_group_jumps.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-p5][2] | Group-arms footer epic whose phases and lander recorded this e2e failure and proved it predates the epic |
| related | [bead:bob-cli-p6][3] | Epic that added walk_by and deferred this adoption at its apollo host gate |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-p5/README.md
[3]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-p6/README.md

<!-- sase:links:end -->

## Description

`[N` / `]N` (and `[{` / `]}` after any `n` walk) open the first note of the previous / next group on every canonical daily, week, and quarter note, on records of albums that set `walk_by`, and on any note whose nav line carries `«` / `»` links. `[n` / `]n` walk a grouped album one group at a time. The property card's docked rail and the links walker footer show the same group stops, and a stop whose note does not exist yet looks clearly, calmly different from one that will never be created.

## Notes

[2026-11-21T15:22:38Z · bob-cli-oj.3.1.land] DISCOVERED ISSUE: Triaged proposal from bob-cli-oj.3.1.4 note #1. plugin-apis.md is 8165/8000 words at bob-plugins 4e0ff78. This is a develop-tier warning (lint.py), not a second fatal docs-check error. Independent count/history shows 7996 before 168b665, 8131 after your calendar-groups phase commit 168b665 (oj.2), then 8165 after 6debb63 (oe.8.3). The existing headroom task bob-cli-ob covers the broader remediation; the oj.2 increment is causally yours and should be considered in outer landing. This is outside the grouped-walk child epic.

[2026-11-21T20:27:18Z · bryanbugyi34@gmail.com] The new bar that we added does not look great. Namely, the '<<' and '>>' don't look great and are not intuitive and the bottom bar is way to cluttered. See the 🔒 20261121\_152522.png screenshot for an example of what this looks like now. The epic lander agent should try to improve the situation before landing the epic.

[2026-11-21T22:10:03Z · bob-cli-oj.5.1.land] FOR THE bob-cli-oj LAND AGENT (from bob-cli-oj.5.1.land): Bryan's note #2 (the «/» arms looked bad and the bottom bar was cluttered) is addressed in Ledger Tools 1.157.0. It is the landing stitch for bob-cli-oj.5.1, committed by the host finalizer on top of bob-plugins ae305a3, and deployed with bob plugins sync.
Decisions taken (auto, final): layout = slim (the group row stays its own slim second row), glyph = skip (Lucide skip-back / skip-forward inline SVG), footer = yes.
Surfaces changed:
1. Property-card group row on day, week, and quarter cards and the grouped record walk rail. Arms show the skip mark and the group name only, with no «/» and no visible landing; the tooltip and accessible name carry the landing. The centre is just the tick track (title and hidden label carry `Day 6 of 7 in week W47` or `Section 2 of 4: … · 2 of 3`). A one-member group shows no centre or track, which is the screenshot case. Creatable and ghost arms use dashed or dotted underlines, not boxes; rail items and chips keep their boxes.
2. Status-bar links walker footer: the same mark (shared kit builder), no «/» in arm text, no `1/1` context, and `]n enters X` moves to the tooltip while the next group arm already names X.
Authored «/»/<< >> nav-line grammar and the conflict message are unchanged; Navigation Hotkeys is untouched.
bob-cli-oj.5.1 and phase bob-cli-oj.5 are closed (evidence in their close notes).
Left for you:
- the decisions-web follow-up (bob-cli-oj.5 note #1)
- bob-cli-oj.6 note #3, the walker-footer e2e geometryStable failure. I reproduced it identically on clean origin/master fc806cf: .bob-bracket-mode x = 819/956/1085/968 for s/w/n/b, width and height stable. So it predates this landing; no task was filed, to avoid duplicating that proposal.

[2026-11-22T00:16:09Z · bob-cli-o6.land] DISCOVERED ISSUE (routed by the bob-cli-o6 land agent): task bob-cli-ot (intention-card e2e yaml-done-returns timeout; yaml-invalid-stays-recoverable refusal notice missing) is caused by this epic's phase bob-cli-oj.6 commit 7b44b29 'paint group arms and hints in the links walker footer'. Attribution is decisive, not inferred: with the same debug bob and harness, the full intention-card e2e passes 82/82 at 9a15d52 (= 7b44b29~1) and yaml-done-returns fails at 7b44b29 (artifacts file:explicit:8290d9715c1214421e92b848 and file:explicit:a9a0d0dd3ca2361e423565a4, attached to bob-cli-ot with code pointers). The related-link suspicion on bob-cli-o6 ('Done-control return path may have regressed in o6.5') is cleared: all o6 commits are in the passing tree. Per task-bead rules this epic-caused issue is bob-cli-oj land-agent work before close; bob-cli-ot stays as the tracking task.

[2026-11-22T02:12:51Z · bob-cli-oj.land] LANDED by bob-cli-oj.land.

STEP 1 VERIFY. Read all 8 phases (oj.1-oj.8, including child epics oj.3.1 and oj.5.1) and every note. Checked them against the plan and the source:
- nav: `[N`/`]N`, `[{`/`]}` on family n, link-only «/» and <</>> grammar, and walkMode v7. Vault vimrc maps `bob_prev/next_group_link`.
- ledger: api.navGroups v1 calendar and record stops, existing/creatable/ghost states, and the periodNotes pre-adoption refusal. The group row is on day, week, and quarter cards and the record rail, plus the walks-by pill and footer group arms.
- bob-cli: walk_by, group-major ring_slots, at most 5 walk-line rewrites, groups/heads JSON with record_walk_groups_v1, `bob albums update` walk_by set/unset, and «/» stripping.
- glossary strands record-note and walker-footer (016cb008).
DECISIONS held: daily_create=yes, walk_more_albums=no (movies/podcasts untouched), memory_glossary applied, memory_decision_group_stops=no (no decisions edit).
Bryan's note #2 (cluttered «/» arms) was fixed in 1.157.0 (oj.5.1.land: skip marks, track-only centre). I confirmed it in today's screenshots.
Real-Obsidian group-jump e2e reran on the final tree with real debug bob (c05deef2): status passed, 40 cases.

STEP 1 EPIC-CAUSED FIXES (this landing):
(a) bob-cli-ot, from oj.6 7b44b29. The wider footer group arms made Obsidian's floating status bar cover the YAML-excursion Done bar, an unstyled full-width bar at the pane bottom. The e2e's hit test showed DIV.status-bar-item over Done's centre. Fix in ledger-tools 1.157.1: Done mounts under the view header as a compact mod-cta button at the top left, clear of the status bar and of top-right notices. The e2e now asserts Done is uncovered before clicking, and a unit test covers the mount position. intention-card e2e 80/82 -> 82/82; record-card 180/180; album UI 129/130, whose one failure (bob-cli-nq) is pre-existing and identical on the base. Deployed with bob plugins sync -p bob-ledger-tools. bob-cli-ot closed with evidence.
(b) oj.8 glossary drift: bob-cli docs/reference/glossary.md was never regenerated after the strand edits, so docs-check failed on generated drift. Regenerated it; generated-drift and lint now pass.

STEP 2 INTEGRATE. Reviewed every non-epic commit since 07:40 in bob-cli (on reqs, om prose links, oo bank, os ref, o6 docs, tidy, rename-drawer) and in bob-plugins (o6 title block, om [[ completion, on req guards, oe.8 successors, oo bank, 70e23b7 digits, fc754fa schema expanded). Nothing duplicates or conflicts with group jumps. 17eae49c only moved the albums-sync paragraph, and the walk_by docs are intact. The req guards act on task lines, not note navigation.

GATES: bob-plugins build:check and docs inventory pass. npm test 8533/8540: 3 wall-clock failures (bob-cli-io frees-marks, bob-cli-km event-link-times, bob-cli-m1 dependency stage), each passing alone. bob-cli just check passes. just docs-check: generated drift, lint, build, URLs, and links pass. The only failure is tools/docs test_contracts (55!=54), already tracked as a DISCOVERED ISSUE on active epic bob-cli-on and reproducible on base. The plugin-apis.md 8308/8000 is a warning only. Vault ledger-tools 1.157.1 is deployed from this checkout; it is an uncommitted build until the landing commit, which holds the same bytes. epic-symbols: none.

FOLLOW-UP OUTCOMES:
- decisions-web group-stops record (oj.1, .2, .3, .4, .5, .6, .7, .8): DECLINED. The plan answered memory_decision_group_stops=no, and filing it would override that decision. The rule lives in the plan's design contract and the docs.
- vault-format.md 6016/6000 (oj.1, .2, .4, .6): DECLINED as resolved by cb9f8fad (o6.6.1.5); docs lint passes.
- plugin-apis.md over budget (oj.4, epic note #1): +1 on bob-cli-ob. The file was 8173 words before oj; oj.2 added about 135, and trimming only that share still leaves it over cap.
- foreign ledger-tools sync refusals (oj.1 #3, oj.2 #4): DECLINED as resolved; oj.7 and this landing deployed ledger-tools cleanly.
- cycler v6 checklist test (oj.2 #2, oe.8): DECLINED as resolved; it no longer fails in npm test.
- Ledger timing flakes (oj.1--1 #9): +1 on bob-cli-io and bob-cli-km; also +1 on bob-cli-m1.
- walker-footer geometryStable (oj.6 #3, oj.7 #3, 5.1.land): NEW bob-cli-p5 (ci, medium). It fails identically at pre-epic 9a15d52, so the epic did not cause it.
- apollo walk_by adoption (oj.7 #1): NEW bob-cli-p6 (feature, small). apollo still times out on SSH banner exchange via apollo and apollo-do today, so the host gate stays recorded and subscriptions/eat are not adopted. zettel is already adopted.
- album schema-field-jump-ctrl-j: +1 on bob-cli-nq (pre-existing).
- test_contracts 55!=54 (oj.7): DECLINED; already routed to active epic bob-cli-on, and not caused by oj.
- task-status-cycler stuck behind the abandoned 726f9a5 stamp (epic-caused, oj.1's lost commit; vault 1.52.0 equals landed 6e0d764, master is 1.55.0): +1 on bob-cli-or, which is the guard bug. Staged a Bryan-approval gate that rechecks the stamp and bytes, then force-deploys origin/master. Coordination note added on bob-cli-on.10.1. block-id-prompt was already redeployed by bob-cli_11.

## Attachments

- 🔒 20261121\_152522.png · image/png · 2858×1728 · 983.287 KiB (private attachment)

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-oj.1](bob-cli-oj.1.md) | Group-link grammar, one resolver, and the \[N / \]N commands | ✓ closed | medium | 2026-11-21 | 1 | 2 |
| [bob-cli-oj.2](bob-cli-oj.2.md) | Calendar group provider, legacy step fill-in, and the pre-adoption guard | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-oj.3](bob-cli-oj.3.md) | Album \`walk\_by\` and group-major record walk lines in bob | ✓ closed | large | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.4](bob-cli-oj.4.md) | Grouped record walk model and the record group provider | ✓ closed | medium | 2026-11-21 | 1 | 2 |
| [bob-cli-oj.5](bob-cli-oj.5.md) | The group row at the bottom of property cards | ✓ closed | large | 2026-11-21 | 1 | 0 |
| [bob-cli-oj.6](bob-cli-oj.6.md) | Group arms and hints in the links walker footer | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-oj.7](bob-cli-oj.7.md) | Album adoption, real-Obsidian proof, and final deploy | ✓ closed | medium | 2026-11-21 | 1 | 1 |
| [bob-cli-oj.8](bob-cli-oj.8.md) | Accepted memory updates | ✓ closed | small | 2026-11-21 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-oj: [N / ]N group jumps for days, periods, records, and any note [closed]"]
    n1["bob-cli-oj.1: Group-link grammar, one resolver, and the [N / ]N commands [closed]"]
    n2["bob-cli-oj.2: Calendar group provider, legacy step fill-in, and the pre-adoption guard [closed]"]
    n3["bob-cli-oj.3: Album `walk_by` and group-major record walk lines in bob [closed]"]
    n4["bob-cli-oj.3.1: Album walk_by and guarded grouped record walks [closed]"]
    n5["bob-cli-oj.3.1.1: Parse walk_by and publish one grouped walk model [closed]"]
    n6["bob-cli-oj.3.1.2: Apply grouped record moves in one guarded transaction [closed]"]
    n7["bob-cli-oj.3.1.3: Add reversible walk_by updates to the album writer [closed]"]
    n8["bob-cli-oj.3.1.4: Document and verify the complete grouped walk contract [closed]"]
    n9["bob-cli-oj.4: Grouped record walk model and the record group provider [closed]"]
    n10["bob-cli-oj.5: The group row at the bottom of property cards [closed]"]
    n11["bob-cli-oj.5.1: The group row at the bottom of property cards [closed]"]
    n12["bob-cli-oj.5.1.1: Kit group-row builder, rail missing-target states, and their CSS [closed]"]
    n13["bob-cli-oj.5.1.2: Day, week, and quarter cards adopt the group row and the derived step row [closed]"]
    n14["bob-cli-oj.5.1.3: Grouped record walk rail and the album card's \"walks by\" pill [closed]"]
    n15["bob-cli-oj.5.1.4: Preview matrix, real-Obsidian e2e runs, and final deploy for the group rail [closed]"]
    n16["bob-cli-oj.6: Group arms and hints in the links walker footer [closed]"]
    n17["bob-cli-oj.7: Album adoption, real-Obsidian proof, and final deploy [closed]"]
    n18["bob-cli-oj.8: Accepted memory updates [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n3 --> n4
    n4 --> n5
    n4 --> n6
    n4 --> n7
    n4 --> n8
    n0 --> n9
    n0 --> n10
    n10 --> n11
    n11 --> n12
    n11 --> n13
    n11 --> n14
    n11 --> n15
    n0 --> n16
    n0 --> n17
    n0 --> n18
    n1 -.-> n10
    n1 -.-> n16
    n2 -.-> n9
    n2 -.-> n10
    n2 -.-> n16
    n3 -.-> n9
    n5 -.-> n6
    n6 -.-> n7
    n7 -.-> n8
    n9 -.-> n10
    n9 -.-> n16
    n10 -.-> n17
    n12 -.-> n13
    n12 -.-> n14
    n13 -.-> n15
    n14 -.-> n15
    n16 -.-> n17
    n17 -.-> n18
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.1.md) | [bob-cli-oj.1](bob-cli-oj.1.md) | 2 |
| [bbugyi200.athena.bob-cli-oj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.2/README.md) | [bob-cli-oj.2](bob-cli-oj.2.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.md) | [bob-cli-oj.3](bob-cli-oj.3.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.1/README.md) | [bob-cli-oj.3.1.1](bob-cli-oj.3.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.1.2.md) | [bob-cli-oj.3.1.2](bob-cli-oj.3.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.3/README.md) | [bob-cli-oj.3.1.3](bob-cli-oj.3.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.3.1.4/README.md) | [bob-cli-oj.3.1.4](bob-cli-oj.3.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.3.1.land.md) | [bob-cli-oj.3.1](bob-cli-oj.3.1.md) | 2 |
| [bbugyi200.athena.bob-cli-oj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.4.md) | [bob-cli-oj.4](bob-cli-oj.4.md) | 2 |
| [bbugyi200.athena.bob-cli-oj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.md) | [bob-cli-oj.5](bob-cli-oj.5.md) | 0 |
| [bbugyi200.athena.bob-cli-oj.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md) | [bob-cli-oj.5.1.1](bob-cli-oj.5.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md) | [bob-cli-oj.5.1.2](bob-cli-oj.5.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md) | [bob-cli-oj.5.1.3](bob-cli-oj.5.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.4/README.md) | [bob-cli-oj.5.1.4](bob-cli-oj.5.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.5.1.land.md) | [bob-cli-oj.5.1](bob-cli-oj.5.1.md) | 2 |
| [bbugyi200.athena.bob-cli-oj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md) | [bob-cli-oj.6](bob-cli-oj.6.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md) | [bob-cli-oj.7](bob-cli-oj.7.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.8.md) | [bob-cli-oj.8](bob-cli-oj.8.md) | 1 |
| [bbugyi200.athena.bob-cli-oj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.land/README.md) | [bob-cli-oj](README.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@168b665`](https://github.com/bobs-org/bob-plugins/commit/168b665d35c36ec1f28309c6abca21219f161c39) | feat(ledger-tools): add api.navGroups v1 calendar group stops | [bob-cli-oj.2](bob-cli-oj.2.md) | 2026-11-21 08:06:42 EST |
| bob-cli | [`e11f2a0`](https://github.com/bobs-org/bob-cli/commit/e11f2a0c5e9fa1cb0aefe01a4ccb1ca1785e0af1) | feat(albums): group record walks by declared walk\_by | [bob-cli-oj.3.1.1](bob-cli-oj.3.1.1.md) | 2026-11-21 08:25:36 EST |
| bob-cli | [`ce0dcc5`](https://github.com/bobs-org/bob-cli/commit/ce0dcc54cec50104991b4ad943de0566e7eba2b6) | feat(records): apply grouped walk updates | [bob-cli-oj.3.1.2](bob-cli-oj.3.1.2.md) | 2026-11-21 08:58:17 EST |
| bob-plugins | [`bob-plugins@51cf930`](https://github.com/bobs-org/bob-plugins/commit/51cf930da624ffaa5f0c950464ad55db1556e77a) | feat(navigation): restore group-link commands and guarded repeats | [bob-cli-oj.1](bob-cli-oj.1.md) | 2026-11-21 09:33:34 EST |
| bob-plugins | [`bob-plugins@983076e`](https://github.com/bobs-org/bob-plugins/commit/983076e6882c744f36e6fa513e9c2853bd160c36) | feat(navigation): land group-link resolver and guarded group jumps | [bob-cli-oj.1](bob-cli-oj.1.md) | 2026-11-21 09:42:42 EST |
| bob-cli | [`66866ea`](https://github.com/bobs-org/bob-cli/commit/66866ea114d6b8eded72d27d66169722d50c6920) | feat(albums): add reversible walk\_by updates to the album writer | [bob-cli-oj.3.1.3](bob-cli-oj.3.1.3.md) | 2026-11-21 09:48:58 EST |
| bob-cli | [`020ad4e`](https://github.com/bobs-org/bob-cli/commit/020ad4e6207f81fd9c633db21c48e1b8efdf3bba) | docs(albums): document grouped record walks | [bob-cli-oj.3.1.4](bob-cli-oj.3.1.4.md) | 2026-11-21 10:15:34 EST |
| bob-cli | [`7ac4fee`](https://github.com/bobs-org/bob-cli/commit/7ac4feeb043503a050e253dfe499da32c9ac1e04) | fix(albums): restore walk\_by at original slot and bind emitted selection | [bob-cli-oj.3.1](bob-cli-oj.3.1.md) | 2026-11-21 11:15:03 EST |
| bob-cli--plans | [`bob-cli--plans@761b2b8`](https://github.com/bobs-org/bob-cli--plans/commit/761b2b8b536aef795ef576ab2a98fb7f7256a9b3) | chore(plans): mark album\_walk\_by epic and landing repairs done | [bob-cli-oj.3.1](bob-cli-oj.3.1.md) | 2026-11-21 11:15:49 EST |
| bob-plugins | [`bob-plugins@d8dc11e`](https://github.com/bobs-org/bob-plugins/commit/d8dc11eafae367bf05b464be86ed4d1a10cfe05b) | feat(ledger-tools): add grouped record navigation | [bob-cli-oj.4](bob-cli-oj.4.md) | 2026-11-21 11:42:38 EST |
| bob-plugins | [`bob-plugins@bd8f2d4`](https://github.com/bobs-org/bob-plugins/commit/bd8f2d46219b794996e8563e3410bbc6e7e58e3c) | docs(plugins): refresh ledger tools inventory for 1.149.2 | [bob-cli-oj.4](bob-cli-oj.4.md) | 2026-11-21 11:56:43 EST |
| bob-plugins | [`bob-plugins@7b44b29`](https://github.com/bobs-org/bob-plugins/commit/7b44b29dc2b29584c2a7dcf0453309bc0a4f8821) | feat(ledger-tools): paint group arms and hints in the links walker footer | [bob-cli-oj.6](bob-cli-oj.6.md) | 2026-11-21 12:39:49 EST |
| bob-plugins | [`bob-plugins@c4953d3`](https://github.com/bobs-org/bob-plugins/commit/c4953d3d47b82dd5d615e9990d9471b3c4c49773) | feat(ledger-tools): add the property-card group row and missing-target states | [bob-cli-oj.5.1.1](bob-cli-oj.5.1.1.md) | 2026-11-21 12:48:44 EST |
| bob-plugins | [`bob-plugins@63e2f64`](https://github.com/bobs-org/bob-plugins/commit/63e2f6418a4f6135b59884ed888b67ccd9c14d68) | feat(ledger-tools): day, week, and quarter cards adopt the group row | [bob-cli-oj.5.1.2](bob-cli-oj.5.1.2.md) | 2026-11-21 13:15:37 EST |
| bob-plugins | [`bob-plugins@2aa877c`](https://github.com/bobs-org/bob-plugins/commit/2aa877ce6064c4679077fadd77c58f530ea8bdd3) | feat(ledger-tools): add the grouped record walk rail and the album walks-by pill | [bob-cli-oj.5.1.3](bob-cli-oj.5.1.3.md) | 2026-11-21 13:24:17 EST |
| bob-plugins | [`bob-plugins@cb70f82`](https://github.com/bobs-org/bob-plugins/commit/cb70f8291aeffa9d8724ea08b51a30ab07671381) | feat(ledger-tools): prove the group rail with a real-builder preview matrix and fix what it found | [bob-cli-oj.5.1.4](bob-cli-oj.5.1.4.md) | 2026-11-21 14:54:59 EST |
| bob-plugins | [`bob-plugins@24ed171`](https://github.com/bobs-org/bob-plugins/commit/24ed1719709183364382e64a48153c01224fea1d) | feat(ledger-tools): declutter the group row and footer group arms with skip marks | [bob-cli-oj.5.1](bob-cli-oj.5.1.md) | 2026-11-21 17:11:32 EST |
| bob-cli--plans | [`bob-cli--plans@b8a4c00`](https://github.com/bobs-org/bob-cli--plans/commit/b8a4c00646dae5071489f1a2214c3f31a0edf796) | chore(plans): mark group\_rail done after landing bob-cli-oj.5.1 | [bob-cli-oj.5.1](bob-cli-oj.5.1.md) | 2026-11-21 17:12:20 EST |
| bob-plugins | [`bob-plugins@235c7db`](https://github.com/bobs-org/bob-plugins/commit/235c7db27ea06bea003db3822d908e08ce2f2c04) | test(nav): add the real-Obsidian \[N / \]N group-jump walkthrough | [bob-cli-oj.7](bob-cli-oj.7.md) | 2026-11-21 18:51:25 EST |
| bob-cli | [`016cb00`](https://github.com/bobs-org/bob-cli/commit/016cb00845d6e85c9149744eed25208fffac3b1a) | docs(glossary): record grouped walks and group stops in record-note and walker-footer | [bob-cli-oj.8](bob-cli-oj.8.md) | 2026-11-21 20:10:48 EST |
| bob-cli | [`f3cf08c`](https://github.com/bobs-org/bob-cli/commit/f3cf08c40139dda1ff9fa9d239cc2374099c7a50) | docs(glossary): regenerate the reference glossary for the grouped-walk strands | [bob-cli-oj](README.md) | 2026-11-21 21:14:08 EST |
| bob-plugins | [`bob-plugins@ebdce52`](https://github.com/bobs-org/bob-plugins/commit/ebdce52a535cca37b15fd6fe66e8414e0df61c09) | fix(ledger-tools): mount the YAML Done control under the pane header | [bob-cli-oj](README.md) | 2026-11-21 21:14:39 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.land][1] | Attribute the bob-cli-ot yaml-done-returns regression to oj.6 commit 7b44b29; need the epic status to route the discovered-issue note | 1 |
| read-by | [agent:bob-cli-oj.2][2] | Need parent epic DECISIONS, notes, and overall scope | 1 |
| read-by | [agent:bob-cli-oj.6][3] | Need sibling phase statuses so I do not redo landed work or collide with group-rail | 1 |
| read-by | [agent:bob-cli-oj.7][4] | Need landed phase notes, versions, and follow-ups before adoption and e2e proof | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-o6.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md

<!-- sase:referenced-by:end -->
