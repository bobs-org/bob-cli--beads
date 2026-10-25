# Bead: bob-cli-bj — Relation label vocabulary — a chooser that works, hidden and one-off labels, and one global rename

[Bead Pages](../README.md) / bob-cli-bj

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2e.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2e.linker.w0.md) · **Assignee:** `bob-cli-bj.land`
**Created:** 2026-10-24 13:34:45 EDT
**Plan:** [202610/relation\_label\_vocabulary.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/relation_label_vocabulary.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-bu][2] | Source epic; decision memory_glossary=no deferred this glossary change |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-bu/README.md

<!-- sase:links:end -->

## Description

The Bob Mac Capture relation card is a reliable, beautiful chooser: Ctrl+N/P move a visible highlight through existing relation labels, Tab accepts, and nothing collapses. Relation labels can be hidden from suggestions (Ctrl+D, with undo), shown again (Ctrl+H section) and unhidden, created hidden with `~note:id||label` (with a clear warning when that hides an existing label), and renamed everywhere — from the card, `bob relations rename`, and Obsidian — in one previewed, revertable commit.

## Notes

[2026-10-24T20:11:30Z · bob-cli-bc.land] DISCOVERED ISSUE (from bob-cli-bc.land, proposed by bob-cli-bc.8 note #1): bob-mac-capture Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:227 (testRelationCardFiltersAndRanksCatalogLocally, added by bj.1 commit 7dc96cf) calls CaptureCompletionCandidate(replacement:label:count:hidden:), but the memberwise init in Sources/CaptureCore/CaptureModels.swift declares hidden (added by bc.7 a49a08b, 18:11Z, before 7dc96cf at 18:25Z) ahead of count, so swift typecheck-tests fails with 'argument hidden must precede count'. bc.8 reproduced it on the clean base; it is still present at bob-mac-capture origin/master fbea724. Fix: pass hidden: true before count: 10 in that test (or reorder the init params if bj prefers), then run the BobMacCaptureTests typecheck on athena/mac. Routed here because bj.1 authored the test and bj.7 (Mac card hide/Hidden section) is actively editing the same hidden-label path; no task created.

[2026-10-24T22:20:44Z · bob-cli-bk.land] DISCOVERED ISSUE corroboration from bob-cli-bk.land: current bob-mac-capture 7bfa312 CI https://github.com/bobs-org/bob-mac-capture/actions/runs/40137474050 passes Lint Swift formatting and Build (including the inbox route UI) but Test cannot compile at Tests/BobMacCaptureTests/CaptureRelationPanelTests.swift:227: argument hidden must precede count. This is exactly the bj.1 7dc96cf error already recorded in epic note #1; bj.7 is active. No new task; unrelated to bk routing. Evidence obtained from the completed CI log, not a new local reproduction.

[2026-10-25T00:02:17Z · bob-cli-bj.land] LAND TRIAGE (bob-cli-bj.land): Read the epic, its plan, and every note on bj.1-bj.11. PROPOSED FOLLOW-UP outcomes: (1) glossary:task-relation sentence (bj.1 #1, bj.3 #2, bj.5 #1, bj.6 #1, bj.7 #1, bj.8 #1, bj.9 #1, bj.10 #1, bj.11 #1) plus the bj.2 #1 Relation label glossary entry -> consolidated into new ready memory task bob-cli-bu (small); no memory edited (memory_glossary=no). (2) bj.8 #2 stage-ranker 16 ms timing -> +1 on existing flake bob-cli-3w (land npm test passed 3648/3648 on bob-plugins 21e9923). (3) bj.3 #3 rename must invalidate relation-label snapshots -> DECLINED, already done: src/native/relation_labels/rename.rs calls invalidate_scan after the write (line 375) and on the commit path (line 842). (4) bj.4 #2, bj.5 #2/#3, bj.6 #2 pre-existing gate reds -> DECLINED, resolved upstream by bc.land 09b26957 (themes rename kinds, help phrase, XDG_CACHE_HOME isolation); land just check on bob-cli 8f50b304 exits 0. (5) bj.4 #1 migrate bob ref rename onto vault_rewrite and bj.1 #2 provision a reachable macOS host/toolchain -> DECLINED as tasks: both are feature-type proposals and task(feature) is not agent-creatable; raised for Bryan here instead (neither is caused by the epic). (6) Epic notes #1/#2 hidden-before-count test compile -> addressed by bj.7 556bb67 (CaptureRelationPanelTests passes hidden before count; CI 40139064007 compiled and ran XCTest). New non-epic Mac CI failures found while separating epic-caused reds in run 40139064007: RefsPanelModelTests.testHighlightsSaveScanUsesPanelPreparation:2312 (pre-dates the epic; also fails on a49a08b run 40119580785) -> new ready ci task bob-cli-bv; CaptureInboxRouteChoiceModelTests:32 argv (closed epic bk, argv builder untouched by bj) -> new ready ci task bob-cli-bw. Deployed bj.11's bob-ledger-tools fold fix to ~/bob with bob plugins sync (only drift; 19/19 unchanged after). Remaining EPIC-CAUSED work found (to be planned): Mac Build broken by bj.9 1001627 (CI 40141576987), never-compiled bj.9 XCTests, CaptureRelationPanelTests.testRelationCardFiltersAndRanksCatalogLocally and two CaptureSeparatorToggleTests Shift+Return timeouts (bj.1 behavior change), and an unbounded per-vault relation catalog cache under ~/.cache/bob-cli/relations (151+ files; lib tests leak into the real cache) that lacks the pruning bc.land added to the theme cache in 09b26957.

[2026-10-25T00:42:57Z · bob-cli-bj.12.land] DISCOVERED ISSUE / nested landing audit from bob-cli-bj.12.land: do not close this parent merely because bj.12 closes. Two parent contract parity gaps remain outside that bounded cache/build repair. (A) At bob-cli d8a8f1f8, Catalog::add_journal_only_keys in src/native/relation_labels/mod.rs iterates Prefs::names (journal.rs includes named explicit visible state), retaining unused labels after unhide as visible count-0 rows. At bob-plugins 21e9923, plugins/bob-ledger-tools/src/147-relation-label-model.js relationLabelCatalogRows skips journal-only prefs unless hidden===true. Scratch bob list with an explicit unhide event for see returns see/count0/hidden=false; running the exact JS helper with no edges and see:{hidden:false,name:see} returns []. Fix cross-client catalog agreement with regression coverage, retaining bob current behavior. (B) Mac 569cb36 CapturePanelModel.swift:7111 relationLabelKey(String) collapses whitespace/lowercases but does not strip one trailing colon; Rust task_relations/label.rs:95 collapse_label_text and JS relationLabelKey do. Exact workspace bob relations list -q see: matches an existing see row, but Mac prompt filtering at :7170 uses see: against candidate key see and yields no rows; exact typed-label rename eligibility also uses that helper. Correct Mac normalization and compile/test the change per Mac AGENTS.md. These are bj-owned defects, not new task beads; the bj.12 cache tale must stop at this incomplete parent unless concurrent work resolves them. Prior Mac compilation and three relation-test blockers are repaired and all 122 tests across the four required suites pass on CI 40146325983. Current bob-cli just check passes 5641 tests; plugins focused relation suites pass 55/55. Follow-up triage remains in bj.12 land notes, with bx/by newly filed because current feature type is agent-creatable.

[2026-10-25T00:55:41Z · bob-cli-bj.12.land] bj.12 LANDED, parent stays open: bob-cli-bj.12 closed with the constrained cache sweep (only obsolete catalog-v<older>-<64hex>.json and owned stale atomic temps; future/malformed/unrelated preserved; just check 5641 tests / 18 records green; Mac CI 40146325983 evidence carried; drift nil at d8a8f1f8 / 569cb36 / 21e9923; epic-symbols clean; no symvision recipe; repair plan status set done). Parent blockers from bj.12.land audit note #4 remain at unchanged tips, so this epic is NOT closed: (A) Rust Catalog::add_journal_only_keys retains named explicit unhidden-unused labels as visible count-0 rows while Obsidian relationLabelCatalogRows skips journal-only prefs unless hidden, breaking cross-client catalog agreement; (B) Mac relationLabelKey only collapses whitespace + lowercases while Rust/JS strip one trailing colon, so query `see:` matches in bob/Obsidian but not the Mac card (also affects typed-key rename eligibility; needs compiled Mac fix + regression coverage). Awaiting those two parity fixes; do not mark plan:202610/relation_label_vocabulary.md done.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-bj.1](bob-cli-bj.1.md) | Mac relation card as a navigate-then-accept chooser | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.10](bob-cli-bj.10.md) | Obsidian rename mode and the relation labels command | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.11](bob-cli-bj.11.md) | Decision records, docs sweep, and end-to-end acceptance | ✓ closed | small | 2026-10-24 | 1 | 2 |
| [bob-cli-bj.2](bob-cli-bj.2.md) | Shared preference journal, relation label catalog, and bob relations list/hide/unhide | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.3](bob-cli-bj.3.md) | capture-complete relation\_label rows from the catalog | ✓ closed | small | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.4](bob-cli-bj.4.md) | Shared vault-rewrite transaction extracted from bob themes rename | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.5](bob-cli-bj.5.md) | The \`\|\|\` one-off relation label capture syntax | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.6](bob-cli-bj.6.md) | bob relations rename across every note, done/ included | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.7](bob-cli-bj.7.md) | Mac card hide, one-off, Hidden section, and warnings | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.8](bob-cli-bj.8.md) | Obsidian label stage parity, JS mirrors, and api.relationLabels | ✓ closed | medium | 2026-10-24 | 1 | 1 |
| [bob-cli-bj.9](bob-cli-bj.9.md) | Mac card rename mode | ✓ closed | medium | 2026-10-24 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-bj: Relation label vocabulary — a chooser that works, hidden and one-off labels, and one global rename [in_progress]"]
    n1["bob-cli-bj.1: Mac relation card as a navigate-then-accept chooser [closed]"]
    n2["bob-cli-bj.10: Obsidian rename mode and the relation labels command [closed]"]
    n3["bob-cli-bj.11: Decision records, docs sweep, and end-to-end acceptance [closed]"]
    n4["bob-cli-bj.12: Relation label vocabulary landing repairs — green Mac build and tests, bounded catalog cache [closed]"]
    n5["bob-cli-bj.12.1: Bound the relation-label catalog cache and isolate its tests [closed]"]
    n6["bob-cli-bj.12.2: Repair the relation-card Mac build and failing relation XCTests [closed]"]
    n7["bob-cli-bj.12.3: Confirm macOS CI on the repair commit and fix any remaining epic-caused failures [closed]"]
    n8["bob-cli-bj.2: Shared preference journal, relation label catalog, and bob relations list/hide/unhide [closed]"]
    n9["bob-cli-bj.3: capture-complete relation_label rows from the catalog [closed]"]
    n10["bob-cli-bj.4: Shared vault-rewrite transaction extracted from bob themes rename [closed]"]
    n11["bob-cli-bj.5: The `||` one-off relation label capture syntax [closed]"]
    n12["bob-cli-bj.6: bob relations rename across every note, done/ included [closed]"]
    n13["bob-cli-bj.7: Mac card hide, one-off, Hidden section, and warnings [closed]"]
    n14["bob-cli-bj.8: Obsidian label stage parity, JS mirrors, and api.relationLabels [closed]"]
    n15["bob-cli-bj.9: Mac card rename mode [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n4 --> n5
    n4 --> n6
    n4 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n0 --> n14
    n0 --> n15
    n1 -.-> n13
    n2 -.-> n3
    n6 -.-> n7
    n8 -.-> n9
    n8 -.-> n10
    n8 -.-> n14
    n9 -.-> n11
    n10 -.-> n12
    n11 -.-> n13
    n12 -.-> n2
    n12 -.-> n15
    n13 -.-> n15
    n14 -.-> n2
    n15 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bj.1.md) | [bob-cli-bj.1](bob-cli-bj.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.10/README.md) | [bob-cli-bj.10](bob-cli-bj.10.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.11/README.md) | [bob-cli-bj.11](bob-cli-bj.11.md) | 2 |
| [bbugyi200.apollo.bob-cli-bj.12.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.12.1/README.md) | [bob-cli-bj.12.1](bob-cli-bj.12.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.12.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.12.2/README.md) | [bob-cli-bj.12.2](bob-cli-bj.12.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.12.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.12.3/README.md) | [bob-cli-bj.12.3](bob-cli-bj.12.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-bj.12.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bj.12.land.md) | [bob-cli-bj.12](bob-cli-bj.12.md) | 2 |
| [bbugyi200.apollo.bob-cli-bj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.2/README.md) | [bob-cli-bj.2](bob-cli-bj.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.3/README.md) | [bob-cli-bj.3](bob-cli-bj.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.4/README.md) | [bob-cli-bj.4](bob-cli-bj.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.5/README.md) | [bob-cli-bj.5](bob-cli-bj.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.6/README.md) | [bob-cli-bj.6](bob-cli-bj.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.7/README.md) | [bob-cli-bj.7](bob-cli-bj.7.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.8/README.md) | [bob-cli-bj.8](bob-cli-bj.8.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.9/README.md) | [bob-cli-bj.9](bob-cli-bj.9.md) | 1 |
| [bbugyi200.apollo.bob-cli-bj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bj.land.md) | [bob-cli-bj](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@7dc96cf`](https://github.com/bobs-org/bob-mac-capture/commit/7dc96cf1c975fb18e3a14df27cbf1b9db9b2ecfd) | feat(mac-capture): add relation chooser | [bob-cli-bj.1](bob-cli-bj.1.md) | 2026-10-24 14:25:23 EDT |
| bob-cli | [`57d7761`](https://github.com/bobs-org/bob-cli/commit/57d77612109f72c1f51aecbcb43c6be106e7398b) | feat(relations): shared preference journal, label catalog, and bob relations list/hide/unhide | [bob-cli-bj.2](bob-cli-bj.2.md) | 2026-10-24 15:08:39 EDT |
| bob-plugins | [`bob-plugins@eb6d26e`](https://github.com/bobs-org/bob-plugins/commit/eb6d26e2e244ebb4b919518c0b4e5e71407a779d) | feat(relation-labels): add journal-backed vocabulary API and picker controls | [bob-cli-bj.8](bob-cli-bj.8.md) | 2026-10-24 15:45:08 EDT |
| bob-cli | [`fd9380c`](https://github.com/bobs-org/bob-cli/commit/fd9380cbaefb8ceb481a914ca6490b6f70e54143) | refactor(themes): extract rename transaction into vault\_rewrite module | [bob-cli-bj.4](bob-cli-bj.4.md) | 2026-10-24 16:07:40 EDT |
| bob-cli | [`6def3ac`](https://github.com/bobs-org/bob-cli/commit/6def3ac88179c25ff6b54b4119c13c2875601ec8) | feat(capture-complete): use cached relation-label catalog | [bob-cli-bj.3](bob-cli-bj.3.md) | 2026-10-24 16:08:31 EDT |
| bob-cli | [`4c46dad`](https://github.com/bobs-org/bob-cli/commit/4c46dadd118a28c0c5255941419a77efc01c870b) | feat(relations): add verified label rename command | [bob-cli-bj.6](bob-cli-bj.6.md) | 2026-10-24 16:56:34 EDT |
| bob-plugins | [`bob-plugins@e368e38`](https://github.com/bobs-org/bob-plugins/commit/e368e38d836db83b44b8d09d92b83396b0f0f6c0) | feat(relation-labels): add Obsidian rename workflow | [bob-cli-bj.10](bob-cli-bj.10.md) | 2026-10-24 17:21:33 EDT |
| bob-cli | [`895b9ba`](https://github.com/bobs-org/bob-cli/commit/895b9ba7608b5c215334132d6d0ae0747e8c0210) | feat(capture): add \|\| one-off relation label syntax with hide-on-commit | [bob-cli-bj.5](bob-cli-bj.5.md) | 2026-10-24 17:51:32 EDT |
| bob-mac-capture | [`bob-mac-capture@556bb67`](https://github.com/bobs-org/bob-mac-capture/commit/556bb6720136d711e81f057cee32ad21d4795c30) | feat(relation-card): hide, one-off, Hidden section, and warnings | [bob-cli-bj.7](bob-cli-bj.7.md) | 2026-10-24 18:33:16 EDT |
| bob-mac-capture | [`bob-mac-capture@1001627`](https://github.com/bobs-org/bob-mac-capture/commit/1001627311646b2211167b906c1a65d4b610fa53) | feat(relation-card): Ctrl+R rename mode with live dry-run preview and merge confirm | [bob-cli-bj.9](bob-cli-bj.9.md) | 2026-10-24 19:09:37 EDT |
| bob-cli | [`8f50b30`](https://github.com/bobs-org/bob-cli/commit/8f50b304b97bcf2e28a98cf4bd60020f0b8df58c) | docs(records): add relation-label decisions, drop planned markers, record acceptance | [bob-cli-bj.11](bob-cli-bj.11.md) | 2026-10-24 19:34:36 EDT |
| bob-plugins | [`bob-plugins@21e9923`](https://github.com/bobs-org/bob-plugins/commit/21e99230f819184c8b6b14d4a1c62fe960520dcd) | fix(relation-labels): refresh shared vectors and match Rust rename fold rule | [bob-cli-bj.11](bob-cli-bj.11.md) | 2026-10-24 19:35:34 EDT |
| bob-mac-capture | [`bob-mac-capture@a2e230e`](https://github.com/bobs-org/bob-mac-capture/commit/a2e230e1c7e65dfe776d27db6e84f6f137b424cf) | fix(relation-card): repair rename build errors and failing relation XCTests | [bob-cli-bj.12.2](bob-cli-bj.12.2.md) | 2026-10-24 20:16:10 EDT |
| bob-cli | [`d8a8f1f`](https://github.com/bobs-org/bob-cli/commit/d8a8f1f8a4ba10c80583c9f638fdf7355678137f) | fix(relations): bound catalog cache and isolate its tests | [bob-cli-bj.12.1](bob-cli-bj.12.1.md) | 2026-10-24 20:21:41 EDT |
| bob-cli | [`303d8d2`](https://github.com/bobs-org/bob-cli/commit/303d8d248aae658feff47d7be9415b0e26c2929a) | fix(relations): constrain catalog sweep to owned files and older versions | [bob-cli-bj.12](bob-cli-bj.12.md) | 2026-10-24 20:56:48 EDT |
| bob-cli--plans | [`bob-cli--plans@f61d5a2`](https://github.com/bobs-org/bob-cli--plans/commit/f61d5a20cfa6638adbe8c8d031205b2972b23646) | docs(plans): mark relation repair plan done for bob-cli-bj.12 closeout | [bob-cli-bj.12](bob-cli-bj.12.md) | 2026-10-24 20:57:31 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bj.12.2][1] | Need parent DECISIONS and land note triage | 1 |
| read-by | [agent:bob-cli-bj.2][2] | epic context for phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.12.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.2/README.md

<!-- sase:referenced-by:end -->
