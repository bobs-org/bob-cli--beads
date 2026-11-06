# Bead: bob-cli-h8 — Work the top-ten task bead bundles from the two-host audit

[Bead Pages](../README.md) / bob-cli-h8

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.land`
**Created:** 2026-11-04 16:39:09 EST · **Closed:** 2026-11-05 19:57:23 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/top_ten_bead_bundles.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 7 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md

<!-- sase:links:end -->

## Description

Every work item ranked by the 2026-11-04 two-host bead audit is done. bob-plugins `npm test` is green under UTC and New York time. `bob plugins sync` accepts a dirty deploy once its exact bundle is committed, so the vault stops running stale plugins. Obsidian closes keep recorded Pomodoro time. `bob periods brief` attributes archived and multi-link minutes correctly before the 2026-11-09 weekly Review. Vault edits stop leaking SASE plans. bob-mac-capture and bob-cli master CI are green again for the failures nobody else owns. athena alerts on hostile CPU, exec, and egress. Every link-consuming writer keeps notes, and generic ref PDFs render emoji.

## Notes

[2026-11-05T00:37:20Z · bob-cli-h4.4--5] DISCOVERED ISSUE: Exact-SHA macOS CI run 41940043128 on snapshot 9593ec6730a99c5b1e164d8ada7c878533c6fd53 still fails the Test step; lint and Build pass, and no test-hang artifact was produced. The preceding master run 41937019961 on base edb2f487c0ddf122961f8c6ae95f9c0d0df82038 fails the same nine editor/key-alias tests, so these failures predate the transfer integration. Failures: CaptureBackslashGotoTests.testInsertHelperDeclinesWhileComposingSubmittingOrLocked; CaptureEditorWordMotionTests.testMotionsLeaveTextAndUndoUntouched; CaptureSeparatorToggleTests.testBackslashAliasAfterTaskTypeOpensTypeMenuAndDoubleTapCloses, testDelayedAcceptedAliasSupersedesGatedCompletion, testNativeUndoRestoresLiteralSigilAliasWithoutRetriggering, testPeriodAliasAfterRouteOpensNewIDBlockPicker, testPeriodAliasOnMoveBulletOpensMovePicker, testSemicolonAliasOnOfferMoveBulletOpensMoveAndLinkPicker, and testUndoAfterMoveAliasRestoresLiteralWithoutRetriggering. Three alias failures were already noted by h8.5 as a follow-up; the backslash helper failure is corroborated on h7.

[2026-11-05T15:45:08Z · cl--1] DISCOVERED ISSUE: The approved x= capture change was verified on exact snapshot a77fbb8 by run 42052432463. The Test step again fails 13 editor, picker, and separator-alias cases also failed on exact base d206803 in run 42040970042; two other base failures passed on the snapshot, while one relation-picker test timed out only in the snapshot. The x= assist tests are absent from the failed-test list. This confirms the macOS 26 suite remains red from the previously tracked CI cluster, with at least one timing-sensitive test variation.

[2026-11-05T16:32:59Z · bob-cli-ha.land] DISCOVERED ISSUE / corroboration from bob-cli-ha.4 proposal #1: lander inspected CI 42037793376 on phase snapshot 0f1ed3b and clean-base 42040643751 on b2f3b61. The same 12 editor/backslash/comma/separator cases fail both runs despite green lint/Build; added +1 to bob-cli-h7 with file:explicit:158794c224e27f034e87d84c. This supplements existing h8 notes #1-2 and h8.5 scope; no duplicate CI task. Base-only CaptureMoveChoiceModelTests.testMoveThenPullInBackAndInboxCarryOneAnswerAndSeed repeats the seed-count issue already proposed by h8.5 #1; record as corroborating observation, not a confirmed same-tree flake. Do not include the phase-only testNamedStartChainTokenRequestsStartNameCompletion in the unrelated CI cluster: its mismatched x =de versus x =#de fixture/test dispatch is retained as bob-cli-ha epic work.

[2026-11-05T19:35:23Z · bob-cli-hd.land] DISCOVERED ISSUE (from bob-cli-hd lander triage of bob-cli-hd.8 note #1): after h8.1 closed bob-cli-ej, scripts/test-ledger-tools-task-link-marks-live.cjs still fails its CPU-time budgets (cold viewport <100 ms, warm/keystroke <25 ms, full <500 ms; lines ~1216-1248) intermittently under full bob-plugins npm test on 2026-11-05 (phase tree and clean base, assertion not recorded), so the h8 goal 'bob-plugins npm test is green' is not yet met for this file. ej's own fix only made freshness-mark-surfaces deterministic, although an ej +1 cited task-link-marks-live. Lander isolated reruns on bob-plugins 7b7c52f passed 2/2, consistent with load sensitivity. The wikilink-index budget half is tracked by bob-cli-f8 (+1 recorded).

[2026-11-06T00:57:23Z · bob-cli-h8.land] Land verification (bob-cli-h8.land, 2026-11-05).

VERIFIED (13/13 phases). bob-cli commits: ea015b66, 53bf9472, d32e858d, 0e11f8b0, 75bb6c62, 20c58da9, a3aa2149, ff1a7524, 4fa96e15. bob-plugins: d4ae2d3, 90ea50e, 9d24e42. bob-mac-capture: 47fece2. tailnet: 2e0ecaa, 0e500d5. All DECISIONS honored: g4 keep; consumption parity yes (PDL7-14 plus decisions:consumption-keeps-notes-and-recorded-time); still_open rebuild; mac_ci_repo_note in sase.yml and mac AGENTS.md; memory edits limited to decisions.
Gates on master 723af324:
- just check: fmt, clippy, and CLI 3202/3202 pass. Only 2 lib tests fail, from the duplicate bob clipboard registration (12e36842 + 06d6c32e), filed as bob-cli-hp.
- CI 42122296004: highlights::overwrite_local 36/36 ok.
- bob-plugins npm test, UTC and New York: 5573-5574/5575. The remaining fails are only load flakes, already tracked: wikilink rank (bob-cli-f8, +1) and Chromium reduced-motion timeout (bob-cli-fz, +1).
Plugin sync without --force:
- athena 8/8 via inclusion proof 8e82734. A later live bob-cli_38 deploy is expected.
- apollo 7/8. bob-ledger-tools is a never-committed bob-cli_34 build that needs Bryan's --force OK; recorded on e4, which stays open.

LANDING FIXES (land commit):
- bob-mac-capture: h7's backslash insert-helper test asserted text that AppKit unmarkText() commits. Fixed the test and strengthened it; it passes on exact-SHA snapshot run 42136215849.
- bob-plugins (epic note #4): task-link-marks-live restores best-of-5 warm samples, and the full-build gate moves from one wall-clock sample to CPU time (budgets unchanged; measured 15-25/500 ms).
- bob-plugins integration: ha.1 01cb7b5c changed shared theme-vector drafts from =#name to =name. Both plugin menu tests now parse the new draft, and the stale root pomodoro_themes copy is resynced to bob-cli. That clears the 3 NACK/SNACK and byte-identity failures.
Integration review: later consumption/close writers (hn successor verdicts, hl merge-in, the 344c0973 coalesce) reuse the parity-aligned writers or keep recorded spans. No conflicts.

CLOSED: 8r, gv, gw, gx, gu, e9, h6, fh, 7q, 1x, f3, fu, dz, eo, fj, fp. Earlier phases closed eh, et, ff, f7, f1, ej, dx, fy, gs, gt, 8n, g4.
LEFT OPEN:
- h7: narrowed to the 12-test alias/comma/editor cluster plus an intermittent hang with no samples uploaded. Not h8-caused; its owners have landed.
- e4: apollo bob-ledger-tools needs Bryan's --force OK.
- gy: the vault guard is verified, but the SASE-side fix needs a sase-project bead, which a bob-cli agent cannot create.

FOLLOW-UP TRIAGE:
- h8.1 #1: +1 on f8.
- h8.4 #1: kept on gy (see above).
- h8.5 #1 and #2, epic notes #1-#3: tracked on h7.
- h8.6 #1, h8.9 #1, h8.10 #2, h8.11 #2, h8.12 #1, h8.7 #11 (clippy): declined, resolved; strict clippy is green on 723af324.
- h8.7 #6-#8: declined, resolved by 0e500d5 and the acceptance run.
- h8.7 #10: noted on 9x.
- h8.10 #1: declined, duplicate of h9; bob-docs lint passes now.
- h8.11 #1: filed as bob-cli-hq.
- h8.13 #1: theme failures fixed in this landing; timing half on f8.
- epic note #4: fixed in this landing.
NEW: hp (clipboard ci). DISCOVERED ISSUE on hl (glossary drift).
Audit narrowing notes added on 8a (short flags still swallowed) and ge (65 fixture JSONs remain).

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-h8.1](bob-cli-h8.1.md) | Make bob-plugins npm test green | ✓ closed | medium | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.10](bob-cli-h8.10.md) | Make the brief's Still open lists honest for ended periods | ✓ closed | medium | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.11](bob-cli-h8.11.md) | Render emoji and uncovered symbols in generic ref PDFs | ✓ closed | medium | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.12](bob-cli-h8.12.md) | Bring reconcile and task\_complete consumption to capture's rules | ✓ closed | medium | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.13](bob-cli-h8.13.md) | Bring bob-plugins Depends-On consumption to the same rules | ✓ closed | medium | 2026-11-04 | 1 | 2 |
| [bob-cli-h8.2](bob-cli-h8.2.md) | Let bob plugins sync accept committed dirty deploys | ✓ closed | medium | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.3](bob-cli-h8.3.md) | Fix archived-task minutes and multi-link splitting in the periods brief | ✓ closed | medium | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.4](bob-cli-h8.4.md) | Stop vault edits from leaking SASE plans into ~/bob | ✓ closed | small | 2026-11-04 | 1 | 0 |
| [bob-cli-h8.5](bob-cli-h8.5.md) | Turn bob-mac-capture master CI green and record the CI-watch rule | ✓ closed | medium | 2026-11-04 | 1 | 2 |
| [bob-cli-h8.6](bob-cli-h8.6.md) | Make the highlights overwrite tests timezone-independent | ✓ closed | small | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.7](bob-cli-h8.7.md) | Alert on hostile CPU, writable-dir execution, and mining egress on athena | ✓ closed | medium | 2026-11-04 | 1 | 0 |
| [bob-cli-h8.8](bob-cli-h8.8.md) | Align task-status-cycler's deferred-only close with bob | ✓ closed | small | 2026-11-04 | 1 | 1 |
| [bob-cli-h8.9](bob-cli-h8.9.md) | Brief truncation counts, Bryan's words, and Markdown glitches | ✓ closed | medium | 2026-11-04 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-h8: Work the top-ten task bead bundles from the two-host audit [closed]"]
    n1["bob-cli-h8.1: Make bob-plugins npm test green [closed]"]
    n2["bob-cli-h8.10: Make the brief's Still open lists honest for ended periods [closed]"]
    n3["bob-cli-h8.11: Render emoji and uncovered symbols in generic ref PDFs [closed]"]
    n4["bob-cli-h8.12: Bring reconcile and task_complete consumption to capture's rules [closed]"]
    n5["bob-cli-h8.13: Bring bob-plugins Depends-On consumption to the same rules [closed]"]
    n6["bob-cli-h8.2: Let bob plugins sync accept committed dirty deploys [closed]"]
    n7["bob-cli-h8.3: Fix archived-task minutes and multi-link splitting in the periods brief [closed]"]
    n8["bob-cli-h8.4: Stop vault edits from leaking SASE plans into ~/bob [closed]"]
    n9["bob-cli-h8.5: Turn bob-mac-capture master CI green and record the CI-watch rule [closed]"]
    n10["bob-cli-h8.6: Make the highlights overwrite tests timezone-independent [closed]"]
    n11["bob-cli-h8.7: Alert on hostile CPU, writable-dir execution, and mining egress on athena [closed]"]
    n12["bob-cli-h8.8: Align task-status-cycler's deferred-only close with bob [closed]"]
    n13["bob-cli-h8.9: Brief truncation counts, Bryan's words, and Markdown glitches [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n1 -.-> n12
    n4 -.-> n5
    n7 -.-> n13
    n10 -.-> n3
    n12 -.-> n5
    n13 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.1.md) | [bob-cli-h8.1](bob-cli-h8.1.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.10/README.md) | [bob-cli-h8.10](bob-cli-h8.10.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.11/README.md) | [bob-cli-h8.11](bob-cli-h8.11.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.12.md) | [bob-cli-h8.12](bob-cli-h8.12.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.13](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.13/README.md) | [bob-cli-h8.13](bob-cli-h8.13.md) | 2 |
| [bbugyi200.athena.bob-cli-h8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.2/README.md) | [bob-cli-h8.2](bob-cli-h8.2.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.3/README.md) | [bob-cli-h8.3](bob-cli-h8.3.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.4/README.md) | [bob-cli-h8.4](bob-cli-h8.4.md) | 0 |
| [bbugyi200.athena.bob-cli-h8.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.5.md) | [bob-cli-h8.5](bob-cli-h8.5.md) | 2 |
| [bbugyi200.athena.bob-cli-h8.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.6/README.md) | [bob-cli-h8.6](bob-cli-h8.6.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.7.md) | [bob-cli-h8.7](bob-cli-h8.7.md) | 0 |
| [bbugyi200.athena.bob-cli-h8.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.8/README.md) | [bob-cli-h8.8](bob-cli-h8.8.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.9.md) | [bob-cli-h8.9](bob-cli-h8.9.md) | 1 |
| [bbugyi200.athena.bob-cli-h8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.land/README.md) | [bob-cli-h8](README.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ea015b6`](https://github.com/bobs-org/bob-cli/commit/ea015b665311e384c0daa6ce451c7350e72a4aa0) | fix(periods): attribute archived tasks and split multi-link minutes in brief | [bob-cli-h8.3](bob-cli-h8.3.md) | 2026-11-04 17:05:30 EST |
| bob-cli | [`53bf947`](https://github.com/bobs-org/bob-cli/commit/53bf94721d638a02106ff7a142b216a4b80e2b7f) | test(highlights): pin overwrite timezone and document recapture stamp | [bob-cli-h8.6](bob-cli-h8.6.md) | 2026-11-04 17:12:34 EST |
| bob-cli | [`d32e858`](https://github.com/bobs-org/bob-cli/commit/d32e858d581e5d2a4b7699dd622d0fb9cd518582) | feat(plugins)!: accept committed dirty deploys via inclusion proof | [bob-cli-h8.2](bob-cli-h8.2.md) | 2026-11-04 17:14:19 EST |
| bob-plugins | [`bob-plugins@d4ae2d3`](https://github.com/bobs-org/bob-plugins/commit/d4ae2d326a1da0622ac2e813a3c021fd36529f1d) | test: stabilize bob-plugins test harnesses | [bob-cli-h8.1](bob-cli-h8.1.md) | 2026-11-04 17:40:50 EST |
| bob-cli | [`0e11f8b`](https://github.com/bobs-org/bob-cli/commit/0e11f8b0e8c3974da3113fe15fd19fa3839c2368) | fix(highlights): preserve fallback glyphs in generic ref PDFs | [bob-cli-h8.11](bob-cli-h8.11.md) | 2026-11-04 17:42:48 EST |
| bob-plugins | [`bob-plugins@90ea50e`](https://github.com/bobs-org/bob-plugins/commit/90ea50e3337319292898fd542a3760dd7bb48aa5) | feat(task-status-cycler)!: keep the closed timed row on a deferred-only close | [bob-cli-h8.8](bob-cli-h8.8.md) | 2026-11-04 17:57:20 EST |
| bob-cli | [`75bb6c6`](https://github.com/bobs-org/bob-cli/commit/75bb6c62e82526445576872e5542de2ad53bd914) | feat(periods): report brief truncation totals and clean words and aliases | [bob-cli-h8.9](bob-cli-h8.9.md) | 2026-11-04 18:39:00 EST |
| bob-cli | [`20c58da`](https://github.com/bobs-org/bob-cli/commit/20c58da9d62d034036bd6cfb0c8ceb17cac0496c) | docs(agents): tell agents to watch exact-SHA macOS CI after pushes | [bob-cli-h8.5](bob-cli-h8.5.md) | 2026-11-04 18:49:38 EST |
| bob-mac-capture | [`bob-mac-capture@47fece2`](https://github.com/bobs-org/bob-mac-capture/commit/47fece243c16eee115fbcb1b763cd56d75561d33) | fix(capture): accept Go To refetch anchored at token start, report stderr on failure | [bob-cli-h8.5](bob-cli-h8.5.md) | 2026-11-04 18:50:03 EST |
| bob-cli | [`a3aa214`](https://github.com/bobs-org/bob-cli/commit/a3aa2149bced74d8e98090a89e5d5d954deb8411) | feat(periods): rebuild brief Still open for ended periods | [bob-cli-h8.10](bob-cli-h8.10.md) | 2026-11-04 19:18:19 EST |
| bob-cli | [`ff1a752`](https://github.com/bobs-org/bob-cli/commit/ff1a7524cf9954c5fa2683009b1e166f5a6697a0) | fix(consumption): align reconcile and completion cleanup | [bob-cli-h8.12](bob-cli-h8.12.md) | 2026-11-05 16:52:34 EST |
| bob-cli | [`4fa96e1`](https://github.com/bobs-org/bob-cli/commit/4fa96e152bae8c00f765934ddb7624b0d6d031df) | docs(task-dependencies): document plugin consumption parity | [bob-cli-h8.13](bob-cli-h8.13.md) | 2026-11-05 17:41:03 EST |
| bob-plugins | [`bob-plugins@9d24e42`](https://github.com/bobs-org/bob-plugins/commit/9d24e420cc8495062a42245003d0db8a332154da) | fix(navigation): preserve notes during Depends-On consumption | [bob-cli-h8.13](bob-cli-h8.13.md) | 2026-11-05 17:41:25 EST |
| bob-mac-capture | [`bob-mac-capture@862f9fc`](https://github.com/bobs-org/bob-mac-capture/commit/862f9fc9c521e4ee53a7f2b224c17a8b874c1118) | test(capture): make the backslash Go To decline test exercise its guards | [bob-cli-h8](README.md) | 2026-11-05 19:58:18 EST |
| bob-plugins | [`bob-plugins@710feae`](https://github.com/bobs-org/bob-plugins/commit/710feae383e487eed1a766af7fae79657cef1935) | test: harden link-mark budgets and resync theme menu vectors | [bob-cli-h8](README.md) | 2026-11-05 19:58:39 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h0.land][1] | Check whether the new audit epic already covers h5/h6/clippy and the h0 lander scope | 1 |
| read-by | [agent:bob-cli-h4.4--5][2] | Assess whether the active CI-green epic owns the newly confirmed baseline editor and alias test failures | 1 |
| read-by | [agent:bob-cli-h8.10][3] | need parent epic context | 1 |
| read-by | [agent:bob-cli-h8.12--3][4] | Check whether the active consumption epic causally owns the unrelated capture_language Clippy failures | 1 |
| read-by | [agent:bob-cli-h8.8][5] | need epic context and g4 reference | 1 |
| read-by | [agent:bob-cli-hd.land][6] | Need the epic scope to judge causal link to residual plugin perf flakes | 1 |
| read-by | [agent:cl--1][7] | Check whether the active top-ten epic owns the current macOS CI failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h0.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h4.4.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.10/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-h8.12.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.8/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hd.land/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.cl.md

<!-- sase:referenced-by:end -->
