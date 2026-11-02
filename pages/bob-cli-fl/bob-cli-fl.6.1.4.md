# Bead: bob-cli-fl.6.1.4 — Render clocks in window lanes and time breakdowns

[Bead Pages](../README.md) / [bob-cli-fl.6.1](bob-cli-fl.6.1.md) / bob-cli-fl.6.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.6.md) · **Assignee:** `bob-cli-fl.6.1.4` · **Size:** medium
**Created:** 2026-11-02 05:03:38 EST · **Closed:** 2026-11-02 08:04:33 EST
**Plan:** [202611/stats\_clock\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/stats_clock_ui.md)

## Description

clock-breakdowns: preserve clock shares through root, project, and type models; render dashed tails, session marks, clock-aware lane transitions, and pinned-span details without changing Day strip lane semantics.

## Notes

[2026-11-02T13:04:08Z · bob-cli-fl.6.1.4] PROPOSED FOLLOW-UP: Stabilize five existing bob-plugins test failures — Clean-base HEAD reproduces the same failures seen in full `npm test`: unavailable Chromium in `test-command-mode-sheet-sequence-dom.cjs`, expected Tasks reload event absent in `test-ledger-tools-freshness-namespace.cjs`, startup storm scan count 1 vs 2 in `test-ledger-tools-note-ready.cjs`, relation startup scan timeout in `test-ledger-tools-relation-index.cjs`, and pending schedule status mismatch in `test-navigation-hotkeys-schedule-work-log.cjs`.

[2026-11-02T13:04:33Z · bob-cli-fl.6.1.4] Implemented clock breakdown and off-clock presentation across Stats roots, projects, types, lanes, and session drilldowns while keeping Day strip semantics unchanged. Focused Stats/Day strip tests pass (61/61); build:check, validate, docs:check (447 passed, 1 skipped), and diff check pass. Full npm test had 5 failures; the same five reproduce on clean base and are recorded as a proposed follow-up. Epic-symbol check is clear. Plugin sync was attempted but the tool refused to overwrite the installed plugin built from another uncommitted checkout; left that deployment untouched.

## Dependencies

- **Depends on:** [bob-cli-fl.6.1.3](bob-cli-fl.6.1.3.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fl.6.1.5](bob-cli-fl.6.1.5.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6.1.4/README.md) | [bob-cli-fl.6.1.4](bob-cli-fl.6.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@75e7875`](https://github.com/bobs-org/bob-plugins/commit/75e78759bdd09a737404dc1b8d842db84c63e59f) | feat(stats): render clock breakdowns in Stats lanes and panels | [bob-cli-fl.6.1.4](bob-cli-fl.6.1.4.md) | 2026-11-02 08:05:36 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fl.6.1.4][1] | Confirm phase notes and prior-work status before implementation | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6.1.4/README.md

<!-- sase:referenced-by:end -->
