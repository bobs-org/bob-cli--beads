# Bead: bob-cli-fl.3.1.3 — Expose and document all three Stats clocks

[Bead Pages](../README.md) / [bob-cli-fl.3.1](bob-cli-fl.3.1.md) / bob-cli-fl.3.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.3.md) · **Assignee:** `bob-cli-fl.3.1.3` · **Size:** medium
**Created:** 2026-11-02 01:23:57 EST · **Closed:** 2026-11-02 03:56:39 EST
**Plan:** [202611/stats\_clock.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock.md)

## Description

clock_interfaces: add CLI clock selection and completion, human and CSV output, integration coverage, documentation, and the inherited authorized glossary sentence.

## Notes

[2026-11-02T08:55:46Z · bob-cli-fl.3.1.3] PROPOSED FOLLOW-UP: clippy needless_borrow blocks just check on clean base — src/native/capture_language/editor_parse.rs:4286 `detect_list_header(&line)` should be `detect_list_header(line)` (-D clippy::needless-borrow; introduced with 0ebd0714; file untouched by this phase, so cargo test never runs under `just check`).

[2026-11-02T08:56:00Z · bob-cli-fl.3.1.3] PROPOSED FOLLOW-UP: stale grammar assertions on clean base — GRAMMAR_REVISION is 6 (src/native/capture_language/mod.rs:42) but tests/cli/capture/complete_drawers.rs:118 and :431 and complete_relationship_owner.rs:315 still expect grammar 5; 3 cargo tests fail identically without this phase.

[2026-11-02T08:56:06Z · bob-cli-fl.3.1.3] PROPOSED FOLLOW-UP: `bob stats` human output prints the journal_gap warning twice (report.warnings and the metric warnings both render in render.rs warning_lines) — pre-existing duplicate, left unchanged to keep default output byte-identical; dedupe in a dedicated change.

[2026-11-02T08:56:39Z · bob-cli-fl.3.1.3] Added -k/--clock (worked|off-clock|total; hidden aliases on/off/untracked/all) to bob stats overview and show with completion descriptions; human output (Worked off-clock hint line, Off-clock header and empty-window text, Total worked/off-clock breakdown in overview, detail and part cells); CSV gains a final clock column; fixed clock_drift warning grammar; docs/stats.md Clocks section, schema-1 clock contract, C-vectors, json-outputs; just docs-gen and just docs-check pass; glossary:off-clock-pomodoro sentence added under inherited memory_off_clock_glossary. Verified: cargo fmt --check; stats lib tests (196) and tests/cli stats/stats_clock/help_options all pass; full cargo test --workspace passes except 3 capture grammar-5-vs-6 tests that fail identically on the clean base; just check stops at one pre-existing clippy needless_borrow in capture_language/editor_parse.rs:4286 (recorded as PROPOSED FOLLOW-UPs). epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-fl.3.1.2](bob-cli-fl.3.1.2.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.3.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.3.1.3/README.md) | [bob-cli-fl.3.1.3](bob-cli-fl.3.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`daf785b`](https://github.com/bobs-org/bob-cli/commit/daf785b6f44fa71e28af2026f83dde6ad648beee) | feat(stats)!: expose and document the Worked, Off-clock, and Total clocks | [bob-cli-fl.3.1.3](bob-cli-fl.3.1.3.md) | 2026-11-02 03:57:26 EST |
