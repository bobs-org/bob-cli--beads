# Bead: bob-cli-mr.3.1 — Narrow the full highlights scan lock window

[Bead Pages](../README.md) / [bob-cli-mr.3](bob-cli-mr.3.md) / bob-cli-mr.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-mr.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.md) · **Assignee:** `bob-cli-mr.3.1.land`
**Created:** 2026-11-17 12:14:07 EST · **Closed:** 2026-11-17 17:20:24 EST
**Plan:** [202611/highlights\_scan\_lock\_window.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/highlights_scan_lock_window.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/highlights_scan_lock_window.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:7aa8ba853d55aee2765444f5 | attached via sase artifact create --bead |
| related | file:explicit:c5c3f5771f7e66352b19542a | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/highlights_scan_lock_window.md

<!-- sase:links:end -->

## Description

Full highlights scans plan without writer locks and acquire them only for validated intake, recovery, or writes while preserving paired PDF and reference-note publication.

## Notes

[2026-11-17T21:02:43Z · bob-cli-mr.3.1.land] FOLLOW-UP TRIAGE (all child PROPOSED FOLLOW-UP entries reviewed): mr.3.1.1 #1 and mr.3.1.2 #1 are one generated docs/develop/decisions.md drift report; declined as already resolved by later commit 48a3116d, which regenerates q-and-ctrl-bracket-mirror-esc, and bob_docs.gen_reference.generate_reference(check=True) now returns no drift. mr.3.1.3 #1 (JSON reference budget) is unrelated to this epic and was routed via sase_new_task to causal active epic bob-cli-ms as a DISCOVERED ISSUE, with independent git-blob word counts: 5999 before ms.1, 6058 after 99005975, 6089 after 48a3116d. Current just docs-check reproduces exactly 6089/6000 and no other lint errors. No duplicate task found in all-status search or 70-task last-week sweep; no new task created. mr.3.1.3 #2 (Mac refs receipt wording) is caused by this epic and explicitly required by scan-proof: confirmed docs/refs.md lines 53-58 in authorized bob-mac-capture checkout still promise receipt publication after every writing scan; retained as remaining epic work for the repair tale, not filed as an unrelated task. Same outcomes must be carried into the eventual close note.

[2026-11-17T21:06:46Z · bob-cli-mr.3.1.land] LANDING AUDIT at 6c409ab2: reviewed the approved plan, every note on mr.3.1.1/.2/.3, governing coordinated-write and ingest-at-birth decisions, and phase commits 1e8f77af/3236ceef/6c409ab2 with current scan_plan/scan_apply, human and JSON presenters, marker guards, intake executor, and interleaving tests. scan_lock=narrow is implemented: shared planning runs unlocked; no-work skips execution and both locks; mutations acquire bob_sync.lock then scan.lock, keep intake and filing protected, retain bounded replan and hook-once behavior, non-clobber moves and coordinated per-PDF execution. The phase-2 double-counting fix is present (unchanged assembly emits Planned outcomes only). Later commits 99005975/48a3116d are independent Record Card source changes; no scan consumer/conflict needs integration, and origin/master matched 6c409ab2. Rebuilt current CLI: all 18 scan_interleave tests pass. However epic is NOT complete: evidence is collected only after planning, so a deterministic planning-handshake addition of a second lib PDF returns success with pdfs=1 and omits it; input preimages/read-set coverage need coherent before/after capture. Combined intake planning omits output/asset collision guards: two queued clash.pdf/clash.PDF are rejected by dry-run, but write mode moves both, publishes one note, then gets a per-PDF preimage error. Source review also shows boundary-discovered overwrite recovery drops locks without publishing a receipt; a no-work/error replan can hide real recovery. Mac receipt contract wording remains wrong as recorded in follow-up triage. These are remaining epic work, not new tasks. Preparing one medium repair tale that includes final epic/parent-phase closeout. No epic-symbol entries for mr.3.1 or mr.3; symvision recipe absent. Current just docs-check fails only JSON budget 6089/6000, attributed separately to ms; generated reference drift is clear. No full just check rerun yet because code repairs remain; do not run just check-full.

[2026-11-17T21:08:23Z · bob-cli-mr.3.1.land] Reproduction evidence for the landing repair tale: file:explicit:c5c3f5771f7e66352b19542a is the isolated Python probe; file:explicit:7aa8ba853d55aee2765444f5 records its output on the freshly built 6c409ab2 CLI. Run against the actual Cargo metadata target_directory binary, not a stale repository target/debug/bob. Confirmed during-planning membership omission and queued-output collision partial publication; late-recovery receipt omission remains source-proven and requires a new regression in the tale.

[2026-11-17T22:20:24Z · bob-cli-mr.3.1.land] Verified all three original phases and the landing repairs: coherent optimistic input evidence, combined intake/library collision guards, serialized recovery receipts, correct Mac receipt docs, preserved lock-free no-work and bob_sync.lock then scan.lock order, unchanged coordinated writes, and later-commit integration.

Evidence coherence (scan_plan.rs): pre-planning snapshot (lib/xlib membership, all vault .md via vault_note_paths, config, input PDF hashes, locator fingerprint) compared post-planning; planner PDF hashes verified against post bytes (not repopulated old-vs-old); vault .md + TextBundle contents (not just dir existence) + archive metadata for Planned/Held/Failed tracked; membership errors propagate (not empty); new before_evidence handshake seam; bounded retry preserves one invocation date for both during- and after-preparation churn. New regressions: pdf_created_during_planning_replans_with_both (planning handshake, pdfs=2 created=2), same_length_edits_before_evidence_replan (sidecar/ref/config/parent same-length + new PDF, replans or safe scan_failed), plus unit validation_detects_* fixed to use real PDF hashes and combined_asset_collisions_reject_shared_destinations.

Collisions: prelock combined check in prepare_from_inputs (write mode: lib+intake dests; dry-run: pdfs as before, no double-count); mutation-window pre-move check (existing+queued under locks, before first move); post-integrate recheck (output + assets before execution) plus validation inside integrate_intake_plans using existing guard helpers (output_collision code/paths preserved). New regressions: queued_queued_output_collision_rejects_without_publication (dry-run and write both output_collision, no moves/notes), queued_existing_output_collision_rejects_without_overwrite (existing note untouched, receipt untouched prelock). Probe now: collision dry-run and write both output_collision (write lists 2 lib dests, no notes/moves, exit 1); membership DURING preparation replans with both (pdfs=2 created=2).

Receipts: second recovery entry (lock_validate_intake_and_execute) now emits recovery receipt while both locks held when recover returns Some (common helper emit_recovery_receipt), so recovery+no-work replaces sentinel before lock-free return and recovery+replan-failure keeps direct error with serialized recovery receipt; never publishes abandoned retry. New regressions: recovery_then_no_work_publishes_receipt (receipt changes, intent cleared, ok true), post_recovery_replan_failure_keeps_direct_output (direct output_collision, receipt ok true, intent cleared). Existing prelock/no-work still leave receipts untouched; coordinated .forMerging, note-only checks, dirty holds, notifications, receipt/stdout identity preserved.

Docs: bob-mac-capture docs/refs.md corrected (mutating scans publish; no-work/prelock leave receipt alone; recovery-only keeps output distinct) with word-budget tightening to stay under 6000 (mount now passes; only json-outputs 6089/6000 remains, reproduced on clean base without our changes, attributed to ms). bob-cli docs/highlights-ref-sync.md clarified post-lock output_collision and recovery-only distinctness. No Swift changes.

Tests: scan_plan lib 10 passed; scan_interleave 24 passed (18 existing + 6 new); highlights::scan 143 passed; highlights::marker 24 passed; highlights::overwrite 81 passed; highlights::ingest 7 passed; highlights_ref lib 1067 passed; probe verified as above; cargo clippy clean for touched lints (collapsible-if, needless-option-as-deref, question-mark); cargo fmt clean. Full just check not run to completion (9-min timeout on unrelated suites); focused gates above cover all touched areas with no new failures. just docs-check: only json-outputs 6089/6000 (pre-existing, clean-base reproduced, ms-owned); mac-capture mount fixed.

Follow-ups carried from lander triage: mr.3.1.1 #1 and mr.3.1.2 #1 duplicate generated-decision drift declined (fixed by 48a3116d, generate_reference(check=True) returns []); mr.3.1.3 #1 JSON word budget belongs to causal active epic bob-cli-ms (independent evidence, no duplicate task, no new task); mr.3.1.3 #2 Mac receipt wording completed above, not deferred. No epic-symbols for mr.3.1 or mr.3; no symvision recipe. No drift since 6c409ab2 (HEAD still 6c409ab2 plus this work).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mr.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.3.1.land.md) | [bob-cli-mr.3.1](bob-cli-mr.3.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0e83df4`](https://github.com/bobs-org/bob-cli/commit/0e83df4cd5797841998afffe227b14052c01f2d7) | feat(scan): finish highlights scan lock-window landing repairs | [bob-cli-mr.3.1](bob-cli-mr.3.1.md) | 2026-11-17 17:23:08 EST |
| bob-mac-capture | [`bob-mac-capture@bfbedda`](https://github.com/bobs-org/bob-mac-capture/commit/bfbedda918ab3884fcba3b16a6206437f3b913fa) | docs(refs): correct last-scan receipt wording for narrow lock window | [bob-cli-mr.3.1](bob-cli-mr.3.1.md) | 2026-11-17 17:23:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mr.3.1.1][1] | need parent epic scope and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mr.3.1.1/README.md

<!-- sase:referenced-by:end -->
