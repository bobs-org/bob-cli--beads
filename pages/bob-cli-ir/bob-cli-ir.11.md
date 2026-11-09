# Bead: bob-cli-ir.11 — Mac new-note preview and success line

[Bead Pages](../README.md) / [bob-cli-ir](README.md) / bob-cli-ir.11

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1a0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1a0.md) · **Assignee:** `bob-cli-ir.11` · **Size:** large
**Created:** 2026-11-08 11:06:12 EST
**Plan:** [202611/record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_notes.md)

## Description

mac-record-preview: render dry-run note_files as a property sheet plus body with a View Markdown disclosure, and show the record success summary.

## Notes

[2026-11-09T15:11:44Z · bob-cli-ir.11] Phase ir.11 partial implementation (this turn): Bob wire + portable Mac foundation landed and verified; SwiftUI panel work remains.

IMPLEMENTED AND VERIFIED THIS TURN:
- bob-cli: per-item additive `record_note` summary (action, label, optional emoji, path, notes, properties; internal markdown/note_file skipped) in src/native/capture/output.rs. Ordinary items omit it. Live smoke: dry-run and commit agree on summary and markdown.
- bob-cli tests: new capture_record_note_summary_shape_matches_dry_run_and_commit in tests/cli/capture/record.rs (single/mixed shape, omission on ordinary items, dry-run==commit). Full record file: 41 passed. cargo fmt clean. just lint (clippy gate) exit 0.
- bob-cli docs: docs/reference/json-outputs.md documents record_note + refusal shape (trimmed for word budget).
- bob-mac-capture (portable, compiles + tests on athena): new Sources/CaptureCore/CaptureRecordPreviewPresentation.swift (CaptureNoteFile/Property/Line, CaptureRecordNoteSummary, CaptureRecordRefusal/InvalidField, headline/detail/noteCountText/pair helpers); CaptureCommandSuccess gains tolerant noteFiles/recordNote; CaptureCommandFailure gains draft/missing/invalid + recordRefusal. 8 real-Bob fixtures record-capture-*.json via extended Scripts/generate-record-fixtures.sh (BOB_BIN=new bob; dry-run/commit/refusal; dry-run==commit proven in-fixture). 17 new tests in CaptureRecordPreviewTests: all pass. Full just portable-check: 2334 tests, 0 failures.
- mac docs: compatibility-table row in docs/protocol.md + result-derivation paragraph in docs/capture-previews.md. just docs-test (script checks) green.
- Reverted unrelated grammar 21->22 drift in regenerated parse/complete fixtures; existing fixtures untouched.

HONESTLY UNVERIFIED / NOT DONE (do not close the bead):
- docs-check (both repos) fails identically on clean base: 3 reference pages over the 6000-word budget (json-outputs 6020 base/6045 mine; mac-capture previews 6140; protocol 6062). No existing tracker found via bead search.
- No SwiftUI RecordNotePreviewView, no PreviewPane/CapturePanelModel/NotificationService wiring, no hosted rendering, no Mac scratch build, no macos-ci-check/CI watch, no Mac latency benchmark. Mac-only targets never compiled this turn (athena has no Xcode).

PROPOSED FOLLOW-UP: SwiftUI RecordNotePreviewView + PreviewPane wiring (kind record_note/create pairing, View Markdown disclosure with exact bytes + copy, default badges, link chips, VoiceOver, Reduce Motion, 620/760px scroll behavior) — evidence: portable pair()/helpers/tests above.
PROPOSED FOLLOW-UP: Inline refusal card + CapturePanelModel wiring (live/explicit/submit paths, clear-on-edit/discard/success, stale-reply guards, quiet guided-entry preserved) — evidence: CaptureRecordRefusal + recordRefusal + refusal fixtures above.
PROPOSED FOLLOW-UP: Committed success wiring (panel status, accessibility, NotificationService record/mixed/legacy-fallback copy) + model tests on fake-Bob harness with bounded waits + notification tests — evidence: headline()/detail()/noteCountText() + commit fixture above.
PROPOSED FOLLOW-UP: Mac verification (disposable rsync scratch copy, Scripts/bundle.sh, just typecheck-tests; Scripts/macos-ci-check + exact-SHA CI watch after push; typing-to-preview latency benchmark record-vs-task, 20+ edits, median/p95) — nothing here substitutes for Mac measurement.
PROPOSED FOLLOW-UP: docs-check reference word-budget overage (pre-existing, fails identically on base 97f0b8f1; json-outputs/mac-capture previews+protocol) — evidence: base vs patched lint output.

[2026-11-09T15:30:08Z · bob-cli-ir.11] Full workspace gate: cargo test --workspace: 3392 passed, 1 failed (help::root_help_matches_sectioned_short_and_long_snapshots). The failure is pre-existing and unrelated: it fails identically on the clean base (verified via stash + rerun). Drift is in capture-related help text (actual mentions record notes, snapshot does not); no existing tracker bead found. PROPOSED FOLLOW-UP: refresh the root help snapshot or the capture-related help text so they agree. cargo fmt clean; just lint (clippy gate) green; record file 41/41 green.

[2026-11-09T15:44:15Z · bob-cli-ir.11] Mac verification evidence (this turn, all on kellys-macbook-pro MacBookPro17,1 macOS 26.5 25F71).

APP + TEST TARGETS COMPILE: disposable scratch /tmp/bob-mac-capture-ir11 (rsync excl .build/.git; harness + main-hook are scratch-only, never in the real tree). Scripts/bundle.sh: build of product BobMacCapture complete. just typecheck-tests: PASS all 4 suites (BobMacCaptureTests, InstallHelper, CaptureCore, RefsCore). No Swift landed uncompiled. Scratch copies removed at the end (mac-app scratch kept until CI; bob-cli scratch /tmp/bob-cli-ir11 removed).

RENDERING: 12 headless ImageRenderer PNGs (620/760px, light/dark, collapsed/expanded Markdown, two-file stack, refusal card) from real fixtures; inspected pixels: heading + destination path, property sheet in Bob order with default badge adjacent to value, aliased link chips, body title/Notes/dated + nested bullets as note content, exact Markdown disclosure with Copy, refusal message + field rows + selectable draft + Copy. No clipping; long values wrap; 620px reachable. One layout fix made from inspection (default badge floated right; chip layout now sizes to content) and re-verified.

LATENCY (real Bob subprocess + synthetic scratch vault/config, production debounce): 4 warmup + 20 measured alternating edits per case. record: median 82.59ms, p95 82.81ms (n=20). task: median 82.77ms, p95 87.63ms (n=20). No material regression. Boundaries: model edit acceptance through ready preview (debounce, parse, dry run); rendering covered by the render check above, not timed. Bob: bob-cli 97f0b8f1 + uncommitted record_note wire change, built on the Mac (cargo build --bin bob, debug). App: bob-mac-capture eded3b9 + uncommitted ir.11 work. Only timings + synthetic identifiers logged.

[2026-11-09T16:01:49Z · bob-cli-ir.11] Exact-SHA macOS CI: run 42647834107 (snapshot 18e93e6d1b3429a39192fd91908f3874c7746bf7 of bob-mac-capture @ eded3b9 + uncommitted ir.11 work, via Scripts/macos-ci-check; branch deleted on exit as designed). Verdicts: Check scripts PASS, Lint Swift formatting PASS, Build PASS. Test step did not finish: the run was canceled by Bryan mid-test, so no Test/Bundle/Install verdict exists. The render-fixtures artifact (27MB) contains no record-note/refusal images because the record design tests never ran before the cancel. https://github.com/bobs-org/bob-mac-capture/actions/runs/42647834107

Remaining to close: re-run Scripts/macos-ci-check to a full green Test verdict (do not re-push while Bryan's cancel stands unexplained), then sase bead epic-symbols + sase bead close bob-cli-ir.11. Everything else in the phase is implemented and verified: Bob record_note wire + tests, portable decode/presentation + 22 tests, fixtures, SwiftUI preview + refusal card + model/notification wiring + Mac tests (run on CI), Mac scratch build + typecheck PASS, 12 inspected renders, latency record 82.59/82.81ms vs task 82.77/87.63ms (n=20 each, no regression).

[2026-11-09T16:17:27Z · bob-cli-ir.11] Exact-SHA macOS CI, second attempt: run 42650743936 (snapshot d41c4ed264d17b9c05fb5c677d8f3311c84f1353 of bob-mac-capture @ eded3b9 + uncommitted ir.11 work). Verdicts again: Check scripts PASS, Lint PASS, Build PASS. Test: 1464 passed, 0 failed before the run was canceled by Bryan at the same stage (during CapturePanelAgendaLayoutTests). New test files compiled on CI (CaptureRecordPreviewDesignTests, CaptureRecordPreviewPanelTests); CaptureRecordPreview* and NotificationService record suites never ran. https://github.com/bobs-org/bob-mac-capture/actions/runs/42650743936

Two consecutive user cancels at the same stage: no third push made. Bead stays open for one reason only: a full-green Test verdict. To close: re-run Scripts/macos-ci-check to green (after confirming with Bryan), then sase bead epic-symbols (clean) + sase bead close bob-cli-ir.11. All other phase evidence stands: Bob wire + 41 record tests, portable 2339 green, Mac scratch build + typecheck PASS, 12 inspected renders, latency record 82.59/82.81ms vs task 82.77/87.63ms.

## Dependencies

- **Depends on:** [bob-cli-ir.10](bob-cli-ir.10.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-ir.12](bob-cli-ir.12.md) ◐ · ⧖ 2026-11-08
- **Depends on:** [bob-cli-ir.5](bob-cli-ir.5.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ir.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ir.11.md) | [bob-cli-ir.11](bob-cli-ir.11.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`84ff0bb`](https://github.com/bobs-org/bob-cli/commit/84ff0bb8ed9dd12bfc9dc5741319b30ccf26a93a) | feat(capture): add per-item record\_note summary to record JSON output | [bob-cli-ir.11](bob-cli-ir.11.md) | 2026-11-09 11:38:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:d5][1] | Know which Mac record-note UX has shipped vs in progress for the user report | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.d5/README.md

<!-- sase:referenced-by:end -->
