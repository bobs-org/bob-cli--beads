# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6 — Backlog batch 17: a precommit macOS gate, the attach-source backfill skips, duplicate research references, scan-wide dirty refusals, and a Swift format config

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land`
**Created:** 2026-10-27 06:23:58 EDT · **Closed:** 2026-10-27 11:02:26 EDT
**Plan:** [202610/backlog\_batch17\_macos\_gate\_source\_backfill\_hook\_dedupe\_dirty\_scans\_swift\_format.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md

<!-- sase:links:end -->

## Description

Close five existing tasks by giving Linux-launched agents a bounded precommit macOS check, attaching saved sources to the skipped agent-report references, stopping the research hook from creating duplicate references, refusing dirty ref-scan targets per PDF, and pinning bob-mac-capture's Swift format.

## Notes

[2026-10-27T13:19:50Z · bob-cli-d2.land] DISCOVERED ISSUE / d2 landing integration: your attach-source-skips phase .2 added JSON in 69b7d962, but commit_batch still prints committed <sha> (N references) to stdout. Reproduced on d38bef59 in an isolated Git vault: successful bob ref attach-source report -f json adoption exits 0 but json.loads(stdout) fails at line 1. Existing tests only cover dry-run JSON. bob-cli-d2 will include the shared commit-output repair and write-mode adoption/search JSON regressions in its remaining-work tale, avoiding duplicate edits. Also recorded bob-cli-d2.3 proposed overlap #2 on bob-cli-co: 17 hook-time attachments independently confirmed, historical membership in the old ambiguous/title-mismatch sets unproven; co stays open. Evidence: file:explicit:c61a26370b705cae1446a6ed.

[2026-10-27T14:18:28Z · bob-cli-d2.land--1] The shared attach-source JSON write-mode repair is implemented in this working diff: commit diagnostics go to stderr in JSON mode so stdout stays one parseable envelope across batch and final commits. Verified by focused attach (25 passed) and full CLI checks (2,291 CLI tests passed; just check and just docs-check passed). Verification evidence: file:explicit:65cf00f6aef47b5c575e10e2 and file:explicit:0b7f8779ba750441f4469595. The broader saved-Markdown landing remains open on bob-cli-d2 because its approved attachment stop gate failed.

[2026-10-27T14:21:17Z · bob-cli-d2.land--1] Updated landing summary after the live vault fast-forward is file:explicit:a56b38495295a784e55ac0a0; it supersedes the earlier summary snapshot while preserving the JSON repair verification and stop-gate record.

[2026-10-27T15:02:22Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land] LANDER VERIFICATION (batch 17), 2026-10-27.

All 5 phases are closed. I re-read every phase note and checked the source of each epic commit against its decision:
- .1 macos-precommit-gate (scratch_ci): bob-cli 79b2859d and bob-mac-capture b8ca374. The macos-ci-check copies are byte-identical, snapshot through a temp GIT_INDEX_FILE, push create-only to ci/precommit/<id>, wait under bounded deadlines, exit 0/1/2, and always delete the branch. Mac Capture CI has a ci/** trigger, and offline tests are wired into check-scripts. AGENTS.md was not edited by the phase.
- .2 attach-source-skips (verify): bob-cli 69b7d962. An ambiguous stem attaches only on exactly one verified candidate (0 or 2+ stay skipped). Explicit pairs skip only the title check, the thresholds are unchanged (12/0.85/0.80), and -f json lists per-candidate verdicts. Tests cover one-pass, zero-pass, two-pass, and explicit-pair cases.
- .3 research-hook-dedupe (implement): chezmoi 10e9f1d2 adds the bob_research_capture wrapper: a hash-free stable stem, -f overwrite while the earlier capture is ready with 0 highlights, else -f reread, and 14 offline tests. Fold proposal: file:explicit:19e2c6c00fdc72a47b88c967.
- .4 per-pdf-dirty-refusal (hold): bob-cli af3a8fd4 (marked !). A pre-execution porcelain -z preflight holds each dirty plan as a whole-PDF dirty_targets hold ('retrying next scan') in human output, JSON held[], and the receipt. Clean PDFs proceed, all-held scans exit 0 (documented), and there is no bypass. bob-mac-capture f8a258f renders the hold as a footer with no banner.
- .5 swift-format-config: bob-mac-capture aab0211, merged as dfd4e7b. .swift-format is 4-space/100-column; the 80 minority files were re-indented whitespace-only.

EPIC-CAUSED DEFECTS FIXED IN THE LANDING:
1. f8a258f (.4) wrote its new Swift lines 2-space inside files .5 had pinned to 4-space, adding 84 Indentation findings. bob-mac-capture e6296bc re-indents only those lines: diff -w is empty, and per-file counts are back at baseline. Linux portable-check: 1696 tests, 0 failures.
2. macos-ci-check (.1) returned as soon as the run reported completed, so a passing run whose macOS job still read in_progress exited 2 (observed live on 40516192731, every step ok). bob-cli b4a5850d and bob-mac-capture 3f70d49 poll a completed run up to 12 poll intervals for the jobs to settle; a job that never settles is still exit 2. Two new tests, 42/42 in both copies. Live rerun 40519931954 exit 0, branch deleted, HEAD and index unchanged.
3. Write-mode attach-source -f json printed 'committed <sha>' to stdout (.2). By agreement in note #1, bob-cli-d2's tale owned the shared repair. It landed in 4cc0ef7d (commit diagnostics to stderr in JSON mode), and CI 40520523548 is green.

INTEGRATION: non-epic commits since c2b69089 were bob-cli 3a13ec6f, d38bef59, 4cc0ef7d (bob-cli-d2, which integrated with .2's candidate selection itself) and ad65a906 (release v0.4.0); chezmoi 62806ca3 (d2: kept the .3 wrapper and raised the timeout to 300 s); bob-plugins b13d634 (command-mode). Nothing else consumes the dirty_targets or scan contract: the chezmoi intake service only runs scan --intake-only, and bob-plugins never calls ref scan. No docs still point to draft PRs.

VERIFICATION: just check passes (6206 tests, 0 failures). CI is green on every landed SHA:
- bob-cli: 69b7d962 (40492305421), 3a13ec6f (40500981278), and d38bef59 (40504551068; it also covers 79b2859d, whose own run was cancelled), af3a8fd4 (40514140736), b4a5850d (40524734722). Every run passed ubuntu, macOS, lint, and package.
- bob-mac-capture: aab0211/dfd4e7b (40490755429/40493057212), b8ca374 (40504593309), f8a258f (40514430994), e6296bc (40523881793), 3f70d49 (40524220187), ed8f3d3 (40524471897). Every run passed through install.

ACCEPTANCE: bob-plugins master b13d634 passes build:check and was re-synced with the stamp-aware workspace bob (--repo linked checkout, --no-pull): 2 copied (bob-command-mode main.js/styles.css), 20 unchanged. bob plugins list: 8 synced, 0 drift; vault tree clean. Packaged smoke gate (xvfb-run -a npm run smoke:obsidian -- --deployed-vault /home/bryan/bob): PASS, layout-ready 426 ms, heap 69.7 MiB, relation ready, 4/4 editors, 0 exceptions/rejections/crashes.

TARGET TASKS: closed done with evidence: bob-cli-by, bob-cli-b1, bob-cli-8k. Kept open with lander notes:
- bob-cli-co: the code is done, but the write pass needs a Bryan-approved /sase_gate, and it should re-dry-run after bob-cli-d2's concurrent backfill and matcher repair land, rather than race them.
- bob-cli-cm: the hook fix is deployed, but folding the five existing duplicates needs a gate, Mac scans, and Bryan's decision on the annotated row.

FOLLOW-UP TRIAGE:
- .1 PROPOSED FOLLOW-UP (put macos-ci-check in agent guidance) duplicates memory task bob-cli-1x: +1 recorded with the gate evidence, no new task.
- .5 PROPOSED FOLLOW-UP (mention .swift-format in bob-mac-capture AGENTS.md) was part of bob-cli-8k's own requested fix, and that file is hand-written, not SASE memory, so it was done in the landing (ed8f3d3), no task.
- .2, .3, and .4 proposed none; .3's gated repairs remain on bob-cli-cm.
- No new tasks filed.

Epic symbols: none. No just symvision recipe.

[2026-10-27T15:02:26Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land] Verified all 5 phases against source and decisions. Fixed three epic-caused defects in the landing: e6296bc re-indents f8a258f's 2-space lines; b4a5850d/3f70d49 add the macos-ci-check job-status settle, with a live exit 0 on 40519931954; the d2 tale's 4cc0ef7d makes write-mode attach-source JSON pure. just check passes (6206 tests). CI is green on every landed SHA in bob-cli and bob-mac-capture. Plugins re-synced from b13d634 (8 synced, 0 drift), and the smoke gate passed. Closed by, b1, and 8k; co and cm stay open with notes, pending gated live writes. Follow-ups: .1 → +1 on bob-cli-1x; .5 done in ed8f3d3; no new tasks. Full detail in the preceding note.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 5 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e6296bc`](https://github.com/bobs-org/bob-mac-capture/commit/e6296bc9727a0f5e2533049b36212e6ea2e6d40b) | style(refs): re-indent per-PDF dirty-hold lines to the pinned 4-space format | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 2026-10-27 10:43:29 EDT |
| bob-mac-capture | [`bob-mac-capture@3f70d49`](https://github.com/bobs-org/bob-mac-capture/commit/3f70d498e156506599f67606defd1c014d9edeb0) | fix(ci): wait for lagging job status before judging a completed run | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 2026-10-27 10:45:31 EDT |
| bob-mac-capture | [`bob-mac-capture@ed8f3d3`](https://github.com/bobs-org/bob-mac-capture/commit/ed8f3d3a17b599ed6d3c81ed58a43a075f7fb529) | docs(agents): point Swift formatting at the pinned .swift-format | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 2026-10-27 10:47:03 EDT |
| bob-cli | [`b4a5850`](https://github.com/bobs-org/bob-cli/commit/b4a5850d32508eeb1133deab68444599d268e9db) | fix(ci): wait for lagging job status before judging a completed run | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 2026-10-27 10:48:41 EDT |
| bob-cli--plans | [`bob-cli--plans@9ec75a2`](https://github.com/bobs-org/bob-cli--plans/commit/9ec75a28aa785fef2e8022238ff55f982df5db45) | chore(plans): mark backlog batch 17 done | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) | 2026-10-27 11:02:37 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land][1] | Need the epic scope, children, and linked plan file | 1 |
| read-by | [agent:bob-cli-d2.land--1][2] | Confirm the named JSON repair epic after note append | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d2.land.md

<!-- sase:referenced-by:end -->
