# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1 — Coordinate remaining reference PDF writes and moves

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.land`
**Created:** 2026-10-26 22:51:27 EDT · **Closed:** 2026-10-27 02:18:58 EDT
**Plan:** [202610/remaining\_pdf\_write\_coordination.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/remaining_pdf_write_coordination.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/remaining_pdf_write_coordination.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/remaining_pdf_write_coordination.md

<!-- sase:links:end -->

## Description

With PDF coordination enabled, reference renames, id repairs, and capture replacements preserve presenter saves, notify moves, and hold without partial publication; Bob Refs and the scratch acceptance kit reflect the contract.

## Notes

[2026-10-27T06:01:25Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.land] Land audit at 0e6b0400 (follow-up triage): none of the five child phases recorded a PROPOSED FOLLOW-UP note, so no /sase_new_task filing was needed. The parent phase's note #2 (annotated-overwrite archive moves issue no didMoveToURL) predates this epic and says the batch-15 lander should decide; it is left to that lander. Native macOS verification is still unavailable (ssh mac timed out again on 2026-10-27), so the Mac move-fixture run, the Mac app bundle/typecheck, and real Highlights acceptance stay recorded limitations, not new tasks. Epic-caused leftover to finish before close: phase 2 left the old uncoordinated rename path (apply_and_verify/apply_transaction/rollback_applied/write_id_marker using MarkerWriteSession::uncoordinated) as dead code. The module-wide #[allow(dead_code)] on highlights_ref::rename hides it. There is also a stale allow on coordinate_explicit_pdf_move_with and a no-op block in rollback_inside_move_scope. No commits landed on master after the epic started, so no integration was needed. No epic-symbol entries for the epic or its parent phase.

[2026-10-27T06:18:58Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.land] Land audit: all five phases verified in source at bob-cli 0e6b0400 (phase 1 f00ae66e move-coordination scope; phase 2 1e923594 rename+id-repair as one coordinated transaction; phase 3 22882a7d guarded publish boundary in highlights_ref/publish.rs; phase 4 0971ad56 capture writers on that boundary; phase 5 0e6b0400 docs plus acceptance kit, Bob Refs hint removed). Mac commit 9db33a6 removed quietHint and added retry-draft tests. No post-epic drift on master to integrate. No epic-symbol entries for the epic or its parent phase.

This tale's cleanup (bob-cli working tree): deleted the legacy uncoordinated rename path in src/native/highlights_ref/rename/plan.rs (apply_and_verify, apply_transaction, rollback_applied, write_id_marker, plus the forced_verify_failure_reverses_moves_and_restores_rewrites test that only exercised it). Production goes execute_rename_with_session -> rename_move_accessor/rename_merge_accessor -> write_id_marker_with_saved. Removed the no-op block in rollback_inside_move_scope and the now write-only AppliedRename.moves field (extend line and transaction_for_rollback literal). Fixed the phase-2 clippy lints without behavior or message changes (matches! merge of the three retry hints; dropped to_path_buf; let-chain collapses in commit_inside_scope, rollback_inside_move_scope, rename_merge_accessor). Removed the dead-code allows on highlights_ref::rename and coordinate_explicit_pdf_move_with; MarkerWriteSession::uncoordinated() is now #[cfg(test)] with its only caller the marker_write test. Removing the module allow surfaced no other dead item. No docs/CLI/version/CHANGELOG/memory edits; bob-plugins and bob-mac-capture untouched.

Verification (all on this tree): cargo clippy --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces exit 0 (remaining warnings pre-date the epic, none in the touched files); cargo test --lib highlights_ref::rename 30 passed; cargo test --lib marker_write 20 passed; cargo test --lib publish 30 passed; cargo test --test cli ref_library::rename 15 passed; just check exit 0 (includes fmt plus the full suite).

Follow-up triage: no child phase recorded a PROPOSED FOLLOW-UP, so no task beads filed. Parent phase note #2 (archive moves issue no didMoveToURL) is left to the batch-15 lander, as that note asks.

Native limitations: the Mac was offline (ssh mac timed out), so the macOS NSDocument move-fixture run, the disposable Mac Scripts/bundle.sh / just typecheck-tests, and real Highlights acceptance were not run. Linux portable tests, just portable-check via just check, and the acceptance kit --self-test passed during the phases.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.land.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`da3fa75`](https://github.com/bobs-org/bob-cli/commit/da3fa75106d90b7e00fd8be1fe2e2ab4c8731118) | refactor(rename): remove dead uncoordinated legacy write path | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.md) | 2026-10-27 02:20:59 EDT |
| bob-cli--plans | [`bob-cli--plans@0c50d77`](https://github.com/bobs-org/bob-cli--plans/commit/0c50d7768628f5ed5724d3d5472c1c522f1b088b) | docs(plans): mark PDF coordination epic plan done | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.md) | 2026-10-27 02:22:47 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2][1] | Need parent epic decisions and scope | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4][2] | parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land][3] | Need phase-2 child epic scope, children, and landing notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.2.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
