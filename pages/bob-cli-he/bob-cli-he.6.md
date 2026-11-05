# Bead: bob-cli-he.6 — One clipboard snapshot per capture and bounded clipboard commands

[Bead Pages](../README.md) / [bob-cli-he](README.md) / bob-cli-he.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5r.linker.w0.md) · **Assignee:** `bob-cli-he.6` · **Size:** medium
**Created:** 2026-11-05 10:29:53 EST · **Closed:** 2026-11-05 14:22:51 EST
**Plan:** [202611/percent\_c\_history\_agreement.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/percent_c_history_agreement.md)

## Description

read-hardening: share one live read and one largest-count history read per capture invocation, and run every clipboard command with a deadline, output cap, and reaping.

## Notes

[2026-11-05T19:22:34Z · bob-cli-he.6] PROPOSED FOLLOW-UP: just fmt, just lint, and 2 CLI tests fail identically on the clean base tree (already tracked by siblings, no action here): rustfmt drift in src/native/config/mod.rs, src/native/plan_budget/mod.rs, src/native/task_status_hooks/sync.rs (see bob-cli-he.3 follow-up); clippy collapsible_if at sync.rs:1625 and redundant binding at articles/inbound.rs:485; plan::plan_reports_full_budget_as_json and task_move::move_without_field_relocates_live_link_to_new_inherited_type (see bob-cli-hd.6 follow-ups)

[2026-11-05T19:22:51Z · bob-cli-he.6] read-hardening done and verified: per-invocation ClipSnapshot shares one live read plus one largest-count history read (each %c<N> takes first N values/provenance; %c-only drafts never read history); every clipboard subprocess (BOB_CLIPBOARD_CMD, pbpaste/wl-paste/xclip/xsel/tmux, both history-command sources) runs via new subprocess_runner::run_raw with 5s deadline, 16MiB stdout cap, 64KiB stderr cap, process-group kill and reaping; timeout names command+deadline, over-cap refuses with the 16MiB copy-a-file-path message. Tests: 4 new subprocess_runner unit tests; 3 new CLI tests (shared single live+history reads with N-slicing and provenance counts, hung history command refuses ~5s with vault untouched and no surviving child, 17MiB live output refuses); updated multi_target fanout test xx->x per the new per-invocation contract; full lib 5127 pass, all 1617 capture CLI tests pass, docs-check passes, my files fmt- and lint-clean. Base-only failures (fmt drift, 2 clippy lints, plan budget JSON + task_move CLI tests) reproduce identically on clean base and are already tracked by he.2/he.3/hd.6. macos-ci-check skipped: diff touches no cfg-gated lines (verified), all edited paths compile and are tested on Linux.

## Dependencies

- **Depends on:** [bob-cli-he.3](bob-cli-he.3.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-he.7](bob-cli-he.7.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-he.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-he.6/README.md) | [bob-cli-he.6](bob-cli-he.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dd3cfd8`](https://github.com/bobs-org/bob-cli/commit/dd3cfd8cb5d9a0fdba8b8e86c8985ee0f7c6570a) | fix(capture): read the clipboard once per capture and bound clipboard commands | [bob-cli-he.6](bob-cli-he.6.md) | 2026-11-05 14:24:07 EST |
