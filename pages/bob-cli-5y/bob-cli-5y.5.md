# Bead: bob-cli-5y.5 — The done/-aware ref-task locator and read-side contracts

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.5` · **Size:** large
**Created:** 2026-10-09 12:29:34 EDT · **Closed:** 2026-10-09 14:55:39 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

ref-locator: build the read-only locator, derive status/parent/dates from the located task, add the task object, diagnostics, ref list -P aliases, and capture-complete task_kind.

## Notes

[2026-10-09T18:01:23Z · 0z4] Status: plan reviewed, implementation deferred to a dedicated phase worker. Baseline timing (before, athena, installed bob 0.1.0, BOB_DIR=/home/bryan/bob, 953 notes): bob ref list -R all -A -f json = 52-60ms over 3 runs. External checkout fast-forwarded to origin/master 90214f1 (parent_notes resolver present; verified resolve_parent/parent_candidates/mark-seam/scan_capture_targets signatures and tests/cli/ref_library harness for the implementer). epic-symbols clean. Bead left open; nothing to close yet.

[2026-10-09T18:55:21Z · 0z5] INTERFACE CHANGE: RefTaskIndex::build(bob_dir: &Path, ref_dir: &Path) -> RefTaskIndex (paths, not config); select(&self, ref_path: &str, v1_hits: &[TrackerHit]) -> RefTaskSelection; LocatedRefTask { path, line_index, line, mark, block_id, archived, residence, closed_on, in_capture_target }; find_managed_embed(body) -> Option<ManagedEmbed { line_index, target, block_id }>; REF_TASK_DIAGNOSTIC_CODES lists 7 codes. Timings: before 52-60ms (athena, on bead); after 98-143ms over 3 runs (this machine, release build, BOB_DIR=/home/bryan/bob, ref list -R all -A -f json), locator adds ~40-80ms, within ~150ms budget.

[2026-10-09T18:55:25Z · 0z5] PROPOSED FOLLOW-UP: Add decisions strand ref-tasks-live-with-their-parent recording that ref tasks live with their parent note (skipped per epic memory_ref_parent_decision=no)

[2026-10-09T18:55:28Z · 0z5] PROPOSED FOLLOW-UP: Update glossary strands reference-task, reference-note, and area-note for the ref-lives-with-parent model (skipped per epic memory_glossary_ref_terms=no)

[2026-10-09T18:55:39Z · 0z5] just check passes (fmt, clippy warnings-only, cargo test --no-fail-fast all green incl 18 ref_tasks unit + 5 ref tasks CLI + lib 2019); perf 98-143ms vs 52-60ms baseline (+40-80ms, within 150ms); CLI/JSON contracts: task object with link/block_id join, -P route/alias/literal, show human/markdown/JSON with follow-up path, doctor ref tasks + parents rows, capture task_kind on 6 pickers

## Dependencies

- **Depends on:** [bob-cli-5y.2](bob-cli-5y.2.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5y.7](bob-cli-5y.7.md) ◐ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5y.8](bob-cli-5y.8.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.5/README.md) | [bob-cli-5y.5](bob-cli-5y.5.md) | 0 |
