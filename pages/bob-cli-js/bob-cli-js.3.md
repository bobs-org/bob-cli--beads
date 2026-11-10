# Bead: bob-cli-js.3 — bob periods show charts and stacks contract

[Bead Pages](../README.md) / [bob-cli-js](README.md) / bob-cli-js.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.41.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.41.linker.w0.md) · **Assignee:** `bob-cli-js.3` · **Size:** medium
**Created:** 2026-11-10 11:49:24 EST · **Closed:** 2026-11-10 13:18:08 EST
**Plan:** [202611/period\_strip\_two\_charts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/period_strip_two_charts.md)

## Description

period_charts: parse stats.period_strip.top_roots, emit charts plus per-column and per-child stacks and display_short, fix long-period coverage copy, document the contract, and set top_roots 5 in chezmoi.

## Notes

[2026-11-10T18:17:31Z · bob-cli-js.3] PROPOSED FOLLOW-UP: just docs-check fails on clean base with bob-plugins mount collision (reference/plugins index.md) — already recorded on bob-cli-js.1 and bob-cli-js.2; reproduced here without docs/periods.md or docs/stats.md causing it

[2026-11-10T18:17:38Z · bob-cli-js.3] PROPOSED FOLLOW-UP: just lint/clippy gate fails on clean HEAD in src/native/gcal/note/write.rs (len_zero, two collapsible_if) and src/native/gcal/doctor.rs (collapsible_if); none of this phase's files are in the deny list

[2026-11-10T18:18:08Z · bob-cli-js.3] Verified period_charts: stats.period_strip.top_roots parses 1-8 (default 5, clamp/warn, never fail load); bob periods show schema 1 JSON adds charts, per-column/per-child stacks, and worked.display_short; Worked is always computed for charts when stats.hide hides the fact; D10 coverage copy (so far · Mon–Tue / W40–W46 / since <date>); chezmoi top_roots 5 with PLAN auto. cargo test --lib charts, config::stats, periods::report all pass; CLI periods_show_* chart tests and relative_period_ids_resolve pass; cargo fmt --check clean. just lint and just docs-check fail identically on clean HEAD (gcal clippy; bob-plugins mount collision, already noted). epic-symbols has no leftovers. PLAN aqua skipped (plan_type_color=no); sase.md pin and glossary rewrite left to long_periods.

## Dependencies

- **Depends on:** [bob-cli-js.2](bob-cli-js.2.md) ✓ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-js.4](bob-cli-js.4.md) ◐ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-js.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-js.3/README.md) | [bob-cli-js.3](bob-cli-js.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a985918`](https://github.com/bobs-org/bob-cli/commit/a985918614f5cd959fe6f22bf2302020c8c26613) | feat(periods): emit charts, stacks, and display\_short on show | [bob-cli-js.3](bob-cli-js.3.md) | 2026-11-10 13:19:19 EST |
| chezmoi | [`chezmoi@c6ae11b`](https://github.com/bbugyi200/dotfiles/commit/c6ae11ba186b82ad046eb4852e23cb26c4fcc09d) | feat(bob): set stats.period\_strip.top\_roots to 5 | [bob-cli-js.3](bob-cli-js.3.md) | 2026-11-10 13:19:55 EST |
