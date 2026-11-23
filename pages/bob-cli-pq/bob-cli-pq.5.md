# Bead: bob-cli-pq.5 — The Mac draft shows requirement bytes as a teal chip

[Bead Pages](../README.md) / [bob-cli-pq](README.md) / bob-cli-pq.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1f8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1f8.md) · **Assignee:** `bob-cli-pq.5` · **Size:** medium
**Created:** 2026-11-23 03:54:18 EST · **Closed:** 2026-11-23 13:03:45 EST
**Plan:** [202611/task\_reqs\_criterion\_diamond.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_reqs_criterion_diamond.md)

## Description

mac-editor: Bob Mac Capture deletes the hash overlay, the byte concealment, and its caret-reveal plumbing, and paints the real `[ ]` bytes as a teal chip like the existing route and theme washes.

## Notes

[2026-11-23T10:27:39Z · bob-cli-pq.5] SEQUENCING WAIT: Approved plan step 0 requires bob-cli-ph.7 and bob-cli-ph.8 to land before Mac editor changes; both are still in_progress. Linked Mac checkout is clean at 0b458fb1 and still has RequirementMarkerGlyphOverlay and caret concealment, so this phase has not landed. No implementation edits made. Resume after both prerequisites close, refresh the linked checkout through sase repo open, read the required research companions, and implement the mac-editor scope.

[2026-11-23T15:14:40Z · bob-cli-pq.5] SEQUENCING WAIT: Rechecked approved plan step 0 and both prerequisites on 2026-11-23; bob-cli-ph.7 and bob-cli-ph.8 are still in_progress. Refreshed bob-mac-capture through sase repo open; clean origin/master remains 0b458fb1 with RequirementMarkerGlyphOverlay, concealedRequirementMarkerSpans, and refreshRequirementMarkerConcealmentIfNeeded intact. This phase has not landed and no implementation changes were made. The original bounded mac-editor scope still fits one coding agent. Staging an automatic prerequisite monitor; successor must verify both resolutions, refresh the linked checkout, read all three research companions, implement the chip and tests/docs, run Mac gates, resolve epic symbols, and close only bob-cli-pq.5.

[2026-11-23T16:49:16Z · bob-cli-pq.5] IMPLEMENTATION: Proceeded under the user instruction that bob-cli-ph need not block this phase; ph.7/ph.8 remain in progress and no drawer code was changed. In the linked Mac checkout, removed the requirement hash overlay, transparent marker bytes, caret-reveal fingerprint and selectionUTF8 plumbing. Depth-bearing Bob req_marker spans now paint exactly [ ] in teal with 0.16/0.28 wash, restored after picker clear. Added paint, selection-no-write, picker restoration, expansion and atomic Backspace regressions plus verbatim bob 0.6.0 fixtures and capture-panel docs. Diff/shell checks pass; full compile, tests, docs and exact-SHA CI verification remain.

[2026-11-23T16:49:21Z · bob-cli-pq.5] PROPOSED FOLLOW-UP: Narrow bob-cli-pp after this phase lands — the requirement overlay and its independent wrapping/scroll geometry are deleted; the record-route emoji overlay and CaptureMonospaceGlyphOrigin.wrappingOrigin remain and still need that bead’s route-emoji fix.

[2026-11-23T16:49:25Z · bob-cli-pq.5] PROPOSED FOLLOW-UP: Requirements Wear The Criterion Diamond decision record was declined by memory_req_mark_record=no — no decision memory was edited; epic land agent should triage any future request to record it.

[2026-11-23T16:50:11Z · bob-cli-pq.5] VERIFICATION HANDOFF: Full gate script .git/pq5-verify.sh compiles and typechecks a disposable Mac scratch copy (never the user checkout), runs portable-check, docs-gen/docs-check with opened linked docs sources, bob-cli named check, and Scripts/macos-ci-check exact-SHA precommit CI. Per-step results go to .git/pq5-verification.tsv. No epic-symbol entries remain. After gates pass, inspect generated diffs, run epic-symbols again, close only bob-cli-pq.5 and submit SASE final commit decisions. No memory edits are authorized in this phase.

[2026-11-23T17:08:39Z · bob-cli-pq.5--1] PROPOSED FOLLOW-UP: Repair pre-existing docs contract-index drift — on clean bob-cli HEAD f6cf62cf, uv run --project tools/docs --group material pytest tools/docs/tests/test_contracts.py -q reproduces all three full docs-check failures identically: registry is 57 vs expected 56, llmstxt omits task-drawers.md, README table digest is 17180faf instead of b89c4426. Root git status is empty after docs-gen; these tests use only root checkout files, not the changed Mac mount. Full docs-check passed lint, generated drift, strict build, URLs, links, search, tutorial and media; unit suite was 444 passed / 1 skipped / these 3 failures. No out-of-scope fix made.

[2026-11-23T17:11:28Z · bob-cli-pq.5--1] PROPOSED FOLLOW-UP: Repair pre-existing drawer Clippy failures — named check b240c610a80832fb27cc4c6dbc6a78cb ran directly on clean bob-cli f6cf62cf (DIRTY 0 -> 0) and exited 101: denied collapsible_if at src/native/task_children.rs:129 and src/native/task_reqs.rs:319, from drawer recognizer code. Formatting passed; Clippy blocked the Rust test stage. Same clean-base class was reported by pq.3; this phase changes no Rust or root files. Follow-up belongs to the drawer work, not the requirement chip.

[2026-11-23T17:11:39Z · bob-cli-pq.5--1] VERIFICATION UPDATE: Monitor pkas3eh3jdaw passed disposable Mac bundle plus all-test typecheck, portable-check (2700 tests, 1 skipped, 0 failures), and docs-gen. Full docs-check passed all gates except the three clean-base contract-index failures, corroborated by pq.3 note #7; named check failed only the two clean-base Clippy denies, corroborated by pq.3 note #4. Both are PROPOSED FOLLOW-UP entries per instruction. Reviewed all carried Mac diffs and verified fixture JSON is byte-identical to installed bob output. Root and plugins checkout are clean, Mac diff-check passes, no epic symbols. Only Scripts/macos-ci-check remains before closing this phase and host commit.

[2026-11-23T17:35:33Z · bob-cli-pq.5--2] CI RECOVERY: Exact-SHA macOS run https://github.com/bobs-org/bob-mac-capture/actions/runs/45225092648 at c2701f0e12737b5d25634302d61e5c30fd050a79 passed lint/build and ran 5119 tests (1 skipped), with only testPickerClearRestoresRequirementChip failing: expected [ ] wash, got no background. Root cause: cancelPicker restored the chip, then setPlainDraft rebuilt unstyled text while restoring the caret. Cancel and panel dismissal now call restoreSelection directly; regression covers both paths with a multibyte prefix, caret inside the marker, exact teal foreground/wash and unwashed trailing space. Changed Swift parse-lint and diff-check pass. Recompiling a disposable Mac copy and rerunning exact-SHA CI; unchanged prior gates and documented clean-base failures are retained.

[2026-11-23T17:38:55Z · bob-cli-pq.5--3] VERIFICATION RECOVERY: Monitor crkzg6670bj4 exited 255 at the initial SSH mktemp command (Mac connection timed out), before scratch setup, compilation, or CI. No remote scratch directory was created and no code gate ran. Linked AGENTS.md makes scratch compilation best effort; tailnet memory documents that Mac SSH is unavailable when the lid is closed. Carrying the unchanged picker fix forward and starting Scripts/macos-ci-check directly, which independently compiles/tests macOS targets and runs bundle/signature/launch/install gates. Mac targets remain unverified for this fix until that full gate passes; prior successful portable/docs checks and documented clean-base failures stand. Root remains clean and Mac diff-check passes.

[2026-11-23T18:03:45Z · bob-cli-pq.5--4] VERIFIED COMPLETE: Native teal requirement chips paint the real [ ] bytes; removed the hash overlay, byte concealment, and caret-reveal plumbing. Picker cancel and panel dismissal preserve chip attributes by restoring the selection directly. Exact-SHA macOS CI passed: https://github.com/bobs-org/bob-mac-capture/actions/runs/45230118421 at 1632ccd6bf636f035c860dba2da95df678690aca. Lint, build, tests, bundle, plist/signature, launch smoke test, and install/reinstall all passed; only conditional diagnostic uploads skipped. Temporary CI branch deleted. Current Mac worktree exactly matches verified tree 3a38c96058d2f3f067dc865b1c5690dd0c858b86. Full CI supersedes the unavailable best-effort scratch recompile after the picker fix. Prior portable-check passed 2700 tests with 1 skipped; docs-gen passed and root remains clean. Full docs-check has only the three identical clean-base contract-index failures in note 7; root named check b240c610a80832fb27cc4c6dbc6a78cb has only the two clean-base drawer Clippy denies in note 8, which blocked Rust tests. These accepted base failures were not rerun. No epic-symbol entries remain. User waived ph.7/ph.8 sequencing; only this phase is closed. Existing proposed follow-ups remain recorded; no memory edits.

## Dependencies

- **Depends on:** [bob-cli-ph.7](../bob-cli-ph/bob-cli-ph.7.md) ◐ · ⧖ 2026-11-22
- **Depends on:** [bob-cli-ph.8](../bob-cli-ph/bob-cli-ph.8.md) ◐ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pq.6](bob-cli-pq.6.md) ◐ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pq.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pq.5.md) | [bob-cli-pq.5](bob-cli-pq.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@c6c9c13`](https://github.com/bobs-org/bob-mac-capture/commit/c6c9c13e9353ce2dfdb3ed667e2ce916cbc30e91) | feat(capture): render native teal requirement chips | [bob-cli-pq.5](bob-cli-pq.5.md) | 2026-11-23 13:04:36 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.1fk/README.md

<!-- sase:referenced-by:end -->
