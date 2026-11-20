# Bead: bob-cli-nu.2 — Command Mode chip engine (resolve, runText, openText, provenance)

[Bead Pages](../README.md) / [bob-cli-nu](README.md) / bob-cli-nu.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.2` · **Size:** medium
**Created:** 2026-11-20 05:59:33 EST · **Closed:** 2026-11-20 06:55:17 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

## Description

engine: add feature-detected api.commandMode members. resolve(text) parses a chip payload into catalog-legal steps. runText runs it with sheet Ctrl+Enter semantics plus the confirm floor, and openText is the guarded path. Also add activeRun and onCatalogChanged, plus trigger/source provenance on run records. One activation planner is shared with the sheet so they can never drift.

## Notes

[2026-11-20T11:37:40Z · bob-cli-nu.2] PROPOSED FOLLOW-UP: Fix the two published URL obligations reported by docs:check at docs/develop/plugins/architecture.md:74 and docs/reference/glossary.md:301; the same errors reproduce identically on a clean base checkout.

[2026-11-20T11:54:35Z · bob-cli-nu.2--2] PROPOSED FOLLOW-UP: Investigate the 25 ms build budgets for the unchanged ledger-tools paths. scripts/test-ledger-tools-event-link-times.cjs and scripts/test-ledger-tools-frees-marks.cjs failed in both full-suite runs, while those scripts and plugins/bob-ledger-tools/main.js and styles.css are unchanged from clean HEAD.

[2026-11-20T11:55:17Z · bob-cli-nu.2--2] Verified Command Mode phase: full npm test rerun had no feature failures; only the two unchanged ledger-tools timing-budget tests failed and are recorded as a PROPOSED FOLLOW-UP. bob plugins sync completed without force, and epic-symbols reports no entries for this phase.

## Dependencies

- **Blocks:** [bob-cli-nu.4](bob-cli-nu.4.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nu.2.md) | [bob-cli-nu.2](bob-cli-nu.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@591998e`](https://github.com/bobs-org/bob-plugins/commit/591998e36b0f41e61c3871d24a48478b541e52b5) | feat(bob-command-mode): add chip execution engine and provenance | [bob-cli-nu.2](bob-cli-nu.2.md) | 2026-11-20 07:12:03 EST |
