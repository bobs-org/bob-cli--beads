# Bead: bob-cli-hn — Successor card verdicts — mark offers Done or Cancel from the card

[Bead Pages](../README.md) / bob-cli-hn

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.191](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.191/README.md) · **Assignee:** `bob-cli-hn.land`
**Created:** 2026-11-05 18:41:46 EST · **Closed:** 2026-11-06 13:19:32 EST
**Plan:** [202611/successor\_card\_verdicts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_card_verdicts.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/successor_card_verdicts.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-hy][2] | Epic whose reviewer decisions (memory_offers_supersede=yes, memory_verdict_record=no) produced the collision |

_Plus 8 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_card_verdicts.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-hy/README.md

<!-- sase:links:end -->

## Description

While reviewing a successor card in Obsidian, in Bob Mac Capture, or through `bob capture`, Bryan can stage Done (Ctrl+X) or Cancel (Ctrl+Shift+X, with an optional inline reason) on any eligible offer row. Those verdicts apply together with pull-ins in the gesture's existing write pass. The engine reports eligibility and consequences, closes are root-only, cascades are recover-only, failures are reported honestly, and the card uses Bob's existing ✓/⊘ visual grammar.

## Notes

[2026-11-06T04:37:46Z · bob-cli-hl.3.1.3--6] DISCOVERED ISSUE: The close descriptors added by bob-cli-hn.2 appear in successor offers, but the note-pull CLI fixtures omit offer.close. On clean pre-execution HEAD 12262fb29655d1efba1639db2c5883d98302e3d59 and the current implementation (monitors cse8a3qgj8n1 and brcp0cs9n851), these tests fail identically: capture::note_pull::np1_no_pick_matches_cli_json_and_human_fixtures, np13_required_choice_matches_refusal_fixture_without_writes, np_move_groups_follow_requested_sources_in_cli_fixtures, np2_pick_all_matches_cli_json_and_human_fixtures, and np16_inbox_choice_and_routed_pick_match_cli_fixtures. The closed bob-cli-h5 tracked an earlier mismatch from destination fields; these new close fields are a separate cause. Triage fixture updates under this epic; no bead created.

[2026-11-06T06:29:29Z · bob-cli-hl.3.1.land] DISCOVERED ISSUE (bob-cli-hl.3.1.land on master 6af313b4): three successor-verdict CLI tests added by efbe3470 (bob-cli-hn.3) fail against offer_close copy from 44c5c8c8 (bob-cli-hn.6.1.1): capture::successor_verdicts::new_task_verdicts_refuse_write_free expects refused.why == 'new_task' but gets '“Draft memo” is new in this capture — drop it from the draft instead'; ineligible_verdicts_refuse_with_why expects why 'recurring' but gets '“Weekly” repeats — close it in Obsidian so Tasks writes the next one'; done_verdict_resolves_root_only_with_scope_note expects '· its 2 embedded tasks stay open' but gets '· its 2 open subtasks stay open' (task_complete/offer_close.rs:346). Reproduce: cargo test -p bob-obsidian --test cli capture::successor_verdicts. Reported by bob-cli-hl.3.1.5 note #2 as a clean-base failure; not caused by capture merge-in. Decide whether refused.why is a code or a sentence and align tests/vectors. No task created.

[2026-11-06T12:40:01Z · bob-cli-hj.land] DISCOVERED ISSUE (bob-cli-hj.land, triaging bob-cli-hj.6 PROPOSED FOLLOW-UP note #3): bob-mac-capture CapturePullInChoiceTests.testFooterContractPinsHintsAndAccessibilityText (Tests/BobMacCaptureTests/CapturePullInChoiceTests.swift:1157) fails on macOS CI (seen on base 6f4e279 and on bob-cli-hj.6's exact-SHA run 42201738623). Cause: 6f4e279 (bob-cli-hn.9) added CapturePullInChoiceFooter.hintItems(openAfterCapture:closeSupported: Bool = false), which drops the ⌃X/⌃⇧X hints when closeSupported is false, but the test's second assertion calls hintItems(openAfterCapture: true) with the default and still expects [⌃N ⌃P, space, ⌘A, ⌃X, ⌃⇧X, esc]. Fix the test (pass closeSupported: true) or the default, per the intended contract; still red on bob-mac-capture master a3e533b source.

[2026-11-06T16:57:48Z · bob-cli-hn.land] FOLLOW-UP TRIAGE (bob-cli-hn.land). Every PROPOSED FOLLOW-UP from hn.1–hn.9 is resolved below. The hn.6.1.x proposals were already triaged in hn.6.1 note #1.
- Memory collision (hn.1 #1, hn.2 #1, hn.3 #4): one proposal, not three. memory_offers_supersede=yes needs the superseding record that memory_verdict_record=no declined, and the decisions web requires a superseded_by target. No memory note was edited. Created ready task bob-cli-hy (memory, xsmall) so Bryan can decide: approve the record and then mark, or cancel.
- BOB_GMAIL_* docs lint (hn.1 #2, hn.2 #3, hn.4 #1): declined as resolved. docs/reference/configuration.md now documents BOB_GMAIL_GOG and BOB_GMAIL_CONSENT_SECS, and the lint no longer fires.
- Clipboard duplicate registrations, catalog protocol count, and help-root gmail snapshot (hn.2 #2, hn.3 #3): declined as resolved. just check on ec39e1a0 passes 9135/0, including the named nodes. Added a note to bob-cli-hp saying it no longer reproduces.
- Unused TODAY const in merge_in.rs (hn.3 #1): declined as resolved by fbb6da46.
- Task-merge lychee anchor (hn.3 #2, hn.9 #1): declined as resolved. docs/capture.md defines #merging-tasks-into-a-new-task-with.
- SV13 disk-preimage e2e gap (hn.3 #5): this is epic work, not a task. It goes into the remaining-work tale as a lib-level test modelled on IRA15.
- npm test theme vectors and wikilink perf (hn.4 #2, hn.5 #1): theme vectors fixed by 710feae, and bob-plugins docs:check glossary drift passed later. Corroborated the wikilink CPU budget on bob-cli-f8 (+1).
- README contract-table SHA (hn.7 #1): corroborated bob-cli-hs (+1). Reproduced on ec39e1a0 with the focused pytest.
- macOS CI cluster (hn.9--2 #2): corroborated bob-cli-h7 (+1) with exact-SHA run 42250497927 on 5b0dca6. It fails only the separator/comma/word-motion cluster, and every Pull-In verdict test passes.
Epic DISCOVERED ISSUES #1–#3 are fixed. capture::note_pull and capture::successor_verdicts pass 29/29 on ec39e1a0, and the Mac footer contract test passes on run 42250497927.

[2026-11-06T18:19:32Z · bob-cli-hn.land--4] Landing verification (2026-11-06). All nine phases bob-cli-hn.1 through bob-cli-hn.9 are closed, and I read and reviewed every phase note with sase bead read.

Epic DISCOVERED ISSUES #1–#3 are fixed. The original note-pull and successor_verdicts regressions passed 29/29 on ec39e1a0; this landing's focused CLI suites passed 80/80 across capture::note_pull, capture::successor_verdicts, capture::merge_in, and capture::inbox_route, and its focused library suites passed 20/20. Mac CapturePullInChoiceTests.testFooterContractPinsHintsAndAccessibilityText is green on exact-SHA run 42250497927. Shared offer-close vectors are byte-identical between bob-cli and cycler; plugin verdict suites pass 343/343. Mac exact-SHA run 42250497927 fails only the pre-existing bob-cli-h7 separator, comma, and word-motion cluster; every Pull-In verdict, footer, inbox-route, and design test passes.

This landing makes four fixes: (1) check explicit route keys against the original report while numeric selectors refer to the filtered choices, covered by capture::successor_verdicts::inbox_route_answer_on_resolved_task_conflicts; (2) remove card-resolved rows before the required-choice guard and renumber remaining routes, covered by capture::successor_verdicts::card_resolved_np16_row_is_not_an_inbox_route_candidate and capture::successor_verdicts::pulled_in_inbox_row_remains_required_and_is_renumbered; (3) print verdict receipts for merge-in offers, covered by capture::merge_in::merge_in_human_offer_prints_the_verdict_receipt and integration equivalence tests capture::merge_in::merge_in_bytes_match_the_equivalent_two_item_transfer and capture::merge_in::merge_in_selected_and_unselected_offer_bytes_match_transfer; (4) show dry-run -x/-X hints only when an unresolved close-eligible offer exists, covered by capture::successor_verdicts::verdict_human_output_prints_receipt_and_hint, capture::successor_verdicts::verdict_dry_run_human_output_uses_would_forms, and capture::keep_moving::human_dry_run_leads_with_why_and_folds.

cargo build --locked --bin bob and note-pull fixture generation passed. just check passed, including formatting, Clippy, and the workspace test suite. just docs-check had 446 passed and 1 skipped; its sole failure was the known test_readme_table_matches_original_contract_index_snapshot SHA mismatch (expected fedc20a…, actual 96a429d5…), tracked by bob-cli-hs and reproduced on clean base. No other docs gate failed. Merge-in integration is verified.

Triage: bob-cli-hy was created for the unresolved memory decision; bob-cli-hs, bob-cli-h7, and bob-cli-f8 were corroborated; the remaining phase proposals were declined as resolved. sase bead epic-symbols bob-cli-hn returned no entries on both runs. just --list has no symvision recipe. No memory note was edited.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-hn.1](bob-cli-hn.1.md) | Contract, vectors table, and decision record | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-hn.2](bob-cli-hn.2.md) | Rust offer-close engine and per-row close descriptors | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-hn.3](bob-cli-hn.3.md) | bob capture -x/-X flags, batch post-pass, and receipts | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-hn.4](bob-cli-hn.4.md) | Obsidian successor picker verdict UI (api.successors v4) | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-hn.5](bob-cli-hn.5.md) | Nav cancel API v1 and Unblocked notice v4 | ✓ closed | small | 2026-11-05 | 1 | 1 |
| [bob-cli-hn.6](bob-cli-hn.6.md) | Cycler eligibility, verdict apply step, receipts, and undo | ✓ closed | large | 2026-11-05 | 1 | 0 |
| [bob-cli-hn.7](bob-cli-hn.7.md) | Verdicts on the Obsidian project-promotion card | ✓ closed | small | 2026-11-05 | 1 | 1 |
| [bob-cli-hn.8](bob-cli-hn.8.md) | CaptureCore decoding, outcome model, argv, and fixtures | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-hn.9](bob-cli-hn.9.md) | Mac Pull-In card verdict UI | ✓ closed | large | 2026-11-05 | 1 | 2 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-hn: Successor card verdicts — mark offers Done or Cancel from the card [closed]"]
    n1["bob-cli-hn.1: Contract, vectors table, and decision record [closed]"]
    n2["bob-cli-hn.2: Rust offer-close engine and per-row close descriptors [closed]"]
    n3["bob-cli-hn.3: bob capture -x/-X flags, batch post-pass, and receipts [closed]"]
    n4["bob-cli-hn.4: Obsidian successor picker verdict UI (api.successors v4) [closed]"]
    n5["bob-cli-hn.5: Nav cancel API v1 and Unblocked notice v4 [closed]"]
    n6["bob-cli-hn.6: Cycler eligibility, verdict apply step, receipts, and undo [closed]"]
    n7["bob-cli-hn.6.1: Complete cycler successor-card verdicts [closed]"]
    n8["bob-cli-hn.6.1.1: Repair the shared offer-close contract and executable vectors [closed]"]
    n9["bob-cli-hn.6.1.2: Add cycler close descriptors and normalize staged choices [closed]"]
    n10["bob-cli-hn.6.1.3: Apply guarded verdicts and recover dependents with Undo snapshots [closed]"]
    n11["bob-cli-hn.6.1.4: Connect verdicts to gestures, notices, reopen, and the review walk [closed]"]
    n12["bob-cli-hn.7: Verdicts on the Obsidian project-promotion card [closed]"]
    n13["bob-cli-hn.8: CaptureCore decoding, outcome model, argv, and fixtures [closed]"]
    n14["bob-cli-hn.9: Mac Pull-In card verdict UI [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n6 --> n7
    n7 --> n8
    n7 --> n9
    n7 --> n10
    n7 --> n11
    n0 --> n12
    n0 --> n13
    n0 --> n14
    n1 -.-> n2
    n1 -.-> n4
    n2 -.-> n3
    n2 -.-> n6
    n3 -.-> n13
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n12
    n8 -.-> n9
    n9 -.-> n10
    n10 -.-> n11
    n13 -.-> n14
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hn.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.1/README.md) | [bob-cli-hn.1](bob-cli-hn.1.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.2/README.md) | [bob-cli-hn.2](bob-cli-hn.2.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.3/README.md) | [bob-cli-hn.3](bob-cli-hn.3.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.4/README.md) | [bob-cli-hn.4](bob-cli-hn.4.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.5/README.md) | [bob-cli-hn.5](bob-cli-hn.5.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.6.md) | [bob-cli-hn.6](bob-cli-hn.6.md) | 0 |
| [bbugyi200.athena.bob-cli-hn.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.6.1.1/README.md) | [bob-cli-hn.6.1.1](bob-cli-hn.6.1.1.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.6.1.2.md) | [bob-cli-hn.6.1.2](bob-cli-hn.6.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.6.1.3/README.md) | [bob-cli-hn.6.1.3](bob-cli-hn.6.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.6.1.4.md) | [bob-cli-hn.6.1.4](bob-cli-hn.6.1.4.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.6.1.land.md) | [bob-cli-hn.6.1](bob-cli-hn.6.1.md) | 2 |
| [bbugyi200.athena.bob-cli-hn.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.7/README.md) | [bob-cli-hn.7](bob-cli-hn.7.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.8/README.md) | [bob-cli-hn.8](bob-cli-hn.8.md) | 1 |
| [bbugyi200.athena.bob-cli-hn.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.9.md) | [bob-cli-hn.9](bob-cli-hn.9.md) | 2 |
| [bbugyi200.athena.bob-cli-hn.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.land.md) | [bob-cli-hn](README.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`723af32`](https://github.com/bobs-org/bob-cli/commit/723af3246886bd84fba1899a4aa19f280314ca05) | feat(docs): define successor offer verdict contract | [bob-cli-hn.1](bob-cli-hn.1.md) | 2026-11-05 18:56:31 EST |
| bob-plugins | [`bob-plugins@8a16ebe`](https://github.com/bobs-org/bob-plugins/commit/8a16ebeab6e4e2e1069527575cdd5a97352e3bc1) | feat(nav-hotkeys): successor picker verdict UI (api.successors v4) | [bob-cli-hn.4](bob-cli-hn.4.md) | 2026-11-05 19:21:44 EST |
| bob-plugins | [`bob-plugins@996fc83`](https://github.com/bobs-org/bob-plugins/commit/996fc839a1e55b3e39265116cfc831170d6df225) | feat(navigation): add cancel and notice v4 APIs | [bob-cli-hn.5](bob-cli-hn.5.md) | 2026-11-05 19:47:11 EST |
| bob-cli | [`53f9c2c`](https://github.com/bobs-org/bob-cli/commit/53f9c2c758653cb54fbb1fd4d4339d18ae23d459) | feat(capture): add staged offer close descriptors | [bob-cli-hn.2](bob-cli-hn.2.md) | 2026-11-05 20:19:35 EST |
| bob-cli | [`44c5c8c`](https://github.com/bobs-org/bob-cli/commit/44c5c8c8fd44340dcfb7376fcd13464032131ee1) | fix(capture): repair shared offer-close contract and executable vectors | [bob-cli-hn.6.1.1](bob-cli-hn.6.1.1.md) | 2026-11-05 21:24:04 EST |
| bob-cli | [`efbe347`](https://github.com/bobs-org/bob-cli/commit/efbe3470dd1eee15711d639e8f0ead022ff86d27) | feat(capture): implement offer verdict surface with complete and cancel offers | [bob-cli-hn.3](bob-cli-hn.3.md) | 2026-11-05 21:54:15 EST |
| bob-plugins | [`bob-plugins@ef9257d`](https://github.com/bobs-org/bob-plugins/commit/ef9257d7faac679fb80fab2a27da5ee654b5d202) | feat(task-status-cycler): add successor offer close descriptors | [bob-cli-hn.6.1.2](bob-cli-hn.6.1.2.md) | 2026-11-05 22:21:31 EST |
| bob-mac-capture | [`bob-mac-capture@8ab7c4e`](https://github.com/bobs-org/bob-mac-capture/commit/8ab7c4ebe845ac6872bc74cfc1b37d76778ff4ee) | feat(capture): add offer-close model support | [bob-cli-hn.8](bob-cli-hn.8.md) | 2026-11-05 22:33:38 EST |
| bob-plugins | [`bob-plugins@3af8d0c`](https://github.com/bobs-org/bob-plugins/commit/3af8d0cddaf7a7bf1ae3d4073f58c9a39a4e2934) | feat(task-status-cycler): apply guarded offer-close verdicts with Undo snapshots | [bob-cli-hn.6.1.3](bob-cli-hn.6.1.3.md) | 2026-11-05 22:49:07 EST |
| bob-mac-capture | [`bob-mac-capture@6f4e279`](https://github.com/bobs-org/bob-mac-capture/commit/6f4e27990823b7174d5902f08f20f52c1390c53f) | feat(mac-capture): stage Done and Cancel verdicts on Pull-In card | [bob-cli-hn.9](bob-cli-hn.9.md) | 2026-11-05 23:14:41 EST |
| bob-plugins | [`bob-plugins@1c3aaf1`](https://github.com/bobs-org/bob-plugins/commit/1c3aaf1235e8e175240d08b9541b8a275f895bb8) | feat(plugins): integrate successor close verdicts | [bob-cli-hn.6.1.4](bob-cli-hn.6.1.4.md) | 2026-11-06 00:31:23 EST |
| bob-cli | [`5c119a0`](https://github.com/bobs-org/bob-cli/commit/5c119a06983ecdb8489098d4da73ef0d02978899) | fix(task-complete): repair successor verdict contracts and receipts | [bob-cli-hn.6.1](bob-cli-hn.6.1.md) | 2026-11-06 01:46:50 EST |
| bob-plugins | [`bob-plugins@d45d8f7`](https://github.com/bobs-org/bob-plugins/commit/d45d8f7ddd8b422faf7f152a978138d5bad8e4d7) | fix(task-status-cycler): preserve guarded undo and recovery receipts | [bob-cli-hn.6.1](bob-cli-hn.6.1.md) | 2026-11-06 01:47:10 EST |
| bob-plugins | [`bob-plugins@f7ae51e`](https://github.com/bobs-org/bob-plugins/commit/f7ae51e90d0a28fd58dd2aa789cc3c3cf8636136) | feat(promotion): wire successor verdicts into the project-promotion card via cycler api v5 | [bob-cli-hn.7](bob-cli-hn.7.md) | 2026-11-06 10:24:57 EST |
| bob-mac-capture | [`bob-mac-capture@5b0dca6`](https://github.com/bobs-org/bob-mac-capture/commit/5b0dca60fbcc6695ed7a1dad77b27be01a9b3eb0) | fix(mac-capture): reopen Pull-In verdicts after offer-close refusal | [bob-cli-hn.9](bob-cli-hn.9.md) | 2026-11-06 11:14:23 EST |
| bob-cli--plans | [`bob-cli--plans@3ebf27e`](https://github.com/bobs-org/bob-cli--plans/commit/3ebf27e5fdf9b08fa381ad1a56f55ccf8ead00ef) | chore(plans): mark finished successor-verdict child tales done | [bob-cli-hn](README.md) | 2026-11-06 12:00:34 EST |
| bob-cli--plans | [`bob-cli--plans@2b7e853`](https://github.com/bobs-org/bob-cli--plans/commit/2b7e853b8bdfc9caf327d7d2158780193e9539eb) | docs(plan): mark successor card verdicts complete | [bob-cli-hn](README.md) | 2026-11-06 13:20:54 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h8.land][1] | Check owner epic of theme vector drift | 1 |
| read-by | [agent:bob-cli-hj.land][2] | Check whether the Pull-In footer contract test failure from hn.9 is already recorded before adding a DISCOVERED ISSUE | 1 |
| read-by | [agent:bob-cli-hl.3.1.3--6][3] | Need to compare this candidate with exact clean-base and current gate failures before recording follow-up evidence | 1 |
| read-by | [agent:bob-cli-hl.3.1.land][4] | Check whether the successor verdict test failures are tracked by the offer epic | 1 |
| read-by | [agent:bob-cli-hn.3][5] | Need epic scope for cli phase | 1 |
| read-by | [agent:bob-cli-hn.4][6] | Need epic status and phase list | 1 |
| read-by | [agent:bob-cli-hn.7][7] | Need epic context and plan for hn.7 | 1 |
| read-by | [agent:bob-cli-hn.land][8] | Need the epic scope, children, and linked plan file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.land/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hl.3.1.3.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hl.3.1.land/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.3/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.4/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hn.7/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hn.land.md

<!-- sase:referenced-by:end -->
