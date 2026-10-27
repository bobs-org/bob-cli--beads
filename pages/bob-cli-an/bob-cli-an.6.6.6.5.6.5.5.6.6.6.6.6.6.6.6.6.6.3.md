# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3 — Fix the mechanical clippy lint classes and gate them

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3` · **Size:** large
**Created:** 2026-10-27 11:12:34 EDT · **Closed:** 2026-10-27 12:41:58 EDT
**Plan:** [202610/backlog\_batch18\_hooks\_legacy\_key\_stats\_perf\_clippy\_gate\_refs\_copy\_docs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch18_hooks_legacy_key_stats_perf_clippy_gate_refs_copy_docs.md)

## Description

clippy-gate: resolve bob-cli-v per the clippy_scope decision by applying behavior-preserving fixes for the mechanical lint classes and denying them in just lint.

## Notes

[2026-10-27T15:32:55Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3] PLANNING BASELINE (no implementation changes): clean tree b4a5850d32508eeb1133deab68444599d268e9db; rustc/Clippy 1.95.0. Read the batch-18 plan and bob-cli-v batch-10 scope note; this phase had no prior work notes. cargo clippy --all-targets --all-features --message-format short exited 0 in 124.3s; supplemental JSON diagnostics identify 435 distinct primary file:line warning sites across 79 lint classes (436 class/site pairs because a line can have multiple lints). Per-class file:line counts, deduplicated across targets: assertions_on_constants=1; bind_instead_of_map=1; bool_assert_comparison=3; bool_comparison=3; chars_next_cmp=1; clone_on_copy=1; cloned_ref_to_slice_refs=4; cmp_owned=3; collapsible_if=118; collapsible_match=6; collapsible_str_replace=4; comparison_to_empty=1; derivable_impls=1; doc_lazy_continuation=2; double_comparisons=1; double_ended_iterator_last=2; enum_variant_names=1; expect_fun_call=6; explicit_auto_deref=1; explicit_counter_loop=1; extend_with_drain=3; field_reassign_with_default=1; filter_map_bool_then=5; for_kv_map=1; format_in_format_args=3; if_same_then_else=2; int_plus_one=2; items_after_test_module=4; iter_cloned_collect=3; large_enum_variant=5; len_zero=3; let_and_return=3; manual_clamp=1; manual_contains=2; manual_ignore_case_cmp=1; manual_is_multiple_of=1; manual_pattern_char_comparison=3; manual_range_patterns=1; manual_rem_euclid=1; manual_strip=1; manual_unwrap_or=3; map_identity=4; match_like_matches_macro=2; match_single_binding=3; missing_const_for_thread_local=1; needless_as_bytes=1; needless_borrow=29; needless_borrows_for_generic_args=24; needless_lifetimes=2; needless_option_as_deref=2; needless_range_loop=2; needless_return=8; no_effect_replace=1; nonminimal_bool=5; op_ref=2; print_literal=2; ptr_arg=2; question_mark=9; redundant_closure=3; redundant_guards=2; redundant_locals=3; replace_box=2; result_large_err=13; single_char_add_str=1; single_element_loop=4; single_match=2; single_range_in_vec_init=1; suspicious_command_arg_space=1; too_many_arguments=60; type_complexity=7; unnecessary_get_then_check=5; unnecessary_map_or=1; unnecessary_sort_by=3; unnecessary_to_owned=2; unnecessary_unwrap=2; useless_concat=2; useless_format=11; while_let_on_iterator=1; wrong_self_convention=1. The eight classes explicitly named by the epic total 180 class/site pairs; collapsible_else_if, useless_conversion, and unnecessary_lazy_evaluations currently have zero sites. Current justfile has only the rustc_gate, and macOS CI already invokes just lint. No epic-symbol entries currently refer to this phase. Preparing a medium tale for reviewed mechanical fixes, an explicit shared deny list, developer docs, Linux checks, cross-target checks, and the packaged macOS CI check; bob-cli-v stays open for the parent lander.

[2026-10-27T15:44:12Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3] IMPLEMENTATION BASELINE (refreshed after ff to origin/master, no implementation changes yet): tree SHA f8dc405b (planning SHA was b4a5850d; landed since then: b1c6be2c hooks-legacy-key, f8dc405b web-clip saved source views). rustc/Clippy 1.95.0. cargo clippy --all-targets --all-features --message-format json exited 0 in 42.9s (CARGO_TARGET_DIR set). Deduplicated primary file:line: 435 distinct locations, 79 lint classes, 436 class/site pairs. Selected mechanical classes: 286 class/site pairs (same as planning); advisory remainder: 150; other: 0. Selected zeros still: collapsible_else_if, unnecessary_lazy_evaluations, useless_conversion. Non-machine selected: 4 unique question_mark MaybeIncorrect (pomodoro_adjust.rs:657, sidecar.rs:496, projects/scan.rs:226, note_snapshot/tests.rs:945) and 2 unique map_identity Unspecified (editor_classify.rs:717, tokens.rs:1721). justfile still has only rustc_gate. Proceeding to scoped cargo clippy --fix for the 48 selected lints.

[2026-10-27T16:18:56Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3] IMPLEMENTATION COMPLETE pending macOS CI.

Tree: dirty working tree on f8dc405b (origin/master unchanged at start of this note). rustc/Clippy 1.95.0. CARGO_TARGET_DIR used.

BEFORE (f8dc405b, refreshed): 435 distinct locations, 79 classes, 436 class/site pairs; selected mechanical 286; advisory 150; selected zeros: collapsible_else_if, unnecessary_lazy_evaluations, useless_conversion.

AFTER (Linux cargo clippy --all-targets --all-features --message-format json): 151 distinct locations / 151 class/site pairs / 35 classes; selected remaining 0; advisory remainder 151 (too_many_arguments=60, result_large_err=13, type_complexity=7, expect_fun_call=6, large_enum_variant=5, nonminimal_bool=5, unnecessary_get_then_check=5, cloned_ref_to_slice_refs=4, format_in_format_args=3, match_single_binding=3, redundant_locals=3, unnecessary_sort_by=3, plus the documented 1-2 count advisory classes). One transient redundant_field_names at task_complete/successors.rs:2092 was a leftover of the needless_borrow rewrite (project_states: project_states) and was completed to the shorthand; it is not in clippy_gate.

POLICY: justfile rustc_gate unchanged; new shared clippy_gate with exactly the 48 explicit -D clippy::<lint> flags. just lint and just check consume the same list. just --dry-run confirmed identical clippy invocations plus check still runs cargo fmt --check and cargo test --no-fail-fast. No -D warnings / -D clippy::all. docs/develop/ci.md documents deny classes, shared Linux/macOS gate, advisory boundary, and just lint / just check.

FIX METHOD: cargo clippy --fix --all-targets --all-features with transient -A clippy::all plus -W for each selected lint (two passes, second --allow-dirty for our own tree). Manual remaining: 4 question_mark let-else -> ? (pomodoro_adjust.rs, sidecar.rs, projects/scan.rs, note_snapshot/tests.rs) preserving bindings; 2 map_identity identity closures removed (editor_classify.rs, tokens.rs); 4 items_after_test_module moves (link_guard.rs, ledger.rs, gkeep/list.rs, task_complete/tree.rs); remaining machine-applicable sites clippy --fix skipped (PathBuf cmp_owned via Path::new, unwrap_or, collapsible_if, single_element_loop, bool_comparison, single_char_add_str, useless_format, filter_map_bool_then, bool_assert_comparison, single_match, needless_borrow). Restored tokens.rs glued-timing/overflow comment next to `parse_pomodoro_start_suffix(&effective)?` and the Keep URL percent-decode comment in gkeep/migrate.rs. Arithmetic: doctor.rs `% 3 == 0` -> is_multiple_of(3); pomodoro_adjust.rs normalize_minutes -> rem_euclid(1440) as u64 (signed semantics/cast unchanged). macOS-only needless_return in capture_clip/clipboard.rs, highlights_ref/io.rs, highlights_ref/pdf_write_policy.rs.

MODULE GROUPS: highlights_ref (largest, including note_snapshot/obsidian.rs), ref_library (attach/migrate_tasks/show/recatalog/code/links), capture + capture_language, gkeep, task_complete/task_status_*, stats, pomodoro_themes, articles, vault_sync, runner, plus tests/cli.

VERIFICATION:
- just lint (deny gate) exit 0
- just --dry-run lint/check share the 48 flags and rustc_gate
- Linux cargo clippy JSON remainder: 0 selected
- cargo clippy --target aarch64-apple-darwin --all-targets --all-features with rustc_gate+clippy_gate from just --evaluate, stub CC/AR in /tmp (not in the source tree), CRATE_CC_NO_DEFAULTS=1: exit 0 after the three macOS needless_return fixes
- just docs-check passed
- sase tool run check a6cbcfe614194387e996bd41137b40f8 succeeded in 288855ms (just check: fmt, clippy gate, cargo test --no-fail-fast)
- sase bead epic-symbols: no entries
- macos-ci-check via sase monitor is next; parent lander owns bob-cli-v under clippy_scope=gate_mechanical

[2026-10-27T16:41:58Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3--1] PHASE COMPLETE. Mechanical clippy gate landed; bob-cli-v stays open for the parent lander.

IMPLEMENTATION: 48 selected mechanical lints denied in justfile clippy_gate (shared by just lint and just check). rustc_gate unchanged. No -D warnings / -D clippy::all. docs/develop/ci.md lint-policy documents deny classes, shared Linux/macOS gate, and advisory remainder.

BEFORE (f8dc405b): 435 distinct locations, 79 classes, 436 class/site pairs; selected mechanical 286; advisory 150; selected zeros: collapsible_else_if, unnecessary_lazy_evaluations, useless_conversion.

AFTER (Linux cargo clippy JSON): 151 distinct locations / 151 class/site pairs / 35 classes; selected remaining 0; advisory remainder 151 (too_many_arguments=60, result_large_err=13, type_complexity=7, expect_fun_call=6, large_enum_variant=5, nonminimal_bool=5, unnecessary_get_then_check=5, cloned_ref_to_slice_refs=4, plus documented 1-3 count advisory classes).

MODULE GROUPS: highlights_ref (incl. note_snapshot/obsidian.rs), ref_library (attach/migrate_tasks/show/recatalog/code/links), capture + capture_language, gkeep, task_complete/task_status_*, stats, pomodoro_themes, articles, vault_sync, runner, tests/cli. macOS-only needless_return: capture_clip/clipboard.rs, highlights_ref/io.rs, highlights_ref/pdf_write_policy.rs.

VERIFICATION:
- just lint exit 0
- just --dry-run lint/check share the 48 flags and rustc_gate
- Linux cargo clippy JSON remainder: 0 selected
- sase tool run check a6cbcfe614194387e996bd41137b40f8 succeeded in 288855ms (fmt, clippy gate, cargo test --no-fail-fast)
- just docs-check passed
- cargo clippy --target aarch64-apple-darwin --all-targets --all-features with rustc_gate+clippy_gate, stub CC/AR in /tmp (not in source tree), CRATE_CC_NO_DEFAULTS=1: exit 0
- sase bead epic-symbols: no entries
- origin/master rebased: ff 9613af85 docs(guides) Mac Capture Command-\\ alias; docs-only, no overlap with clippy tree, no conflicts; tested tree unchanged so lint/check not rerun
- macos-ci-check mf6jgyac69hv / sase tool run ad37cf3952eb0ac4d6391cf0cd620ff4 exit 0
  snapshot SHA 16383d048459daa3ee4a759ae7bc876323b9d7dd
  run https://github.com/bobs-org/bob-cli/actions/runs/40539786195
  workflow CI conclu

… and 376 more characters

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a1dc020`](https://github.com/bobs-org/bob-cli/commit/a1dc02069f9178b4ecde129bb79bac99559d3780) | refactor(lint): fix and deny 48 mechanical clippy classes | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3.md) | 2026-10-27 12:43:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3--1][1] | Read phase notes and status before closing clippy-gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.6.3.md

<!-- sase:referenced-by:end -->
