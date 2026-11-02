# Bead: bob-cli-g1.3 — Real-Obsidian e2e and visual review (bob-plugins, bob-cli)

[Bead Pages](../README.md) / [bob-cli-g1](README.md) / bob-cli-g1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.176](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.176.md) · **Assignee:** `bob-cli-g1.3` · **Size:** medium
**Created:** 2026-11-02 12:45:29 EST · **Closed:** 2026-11-02 15:29:44 EST
**Plan:** [202611/ledger\_frees\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ledger_frees_marks.md)

## Description

live_verify: add an isolated real-Obsidian e2e with light/dark screenshots, tune CSS from the review, and record live verification in the contract.

## Notes

[2026-11-02T20:29:30Z · bob-cli-g1.3] PROPOSED FOLLOW-UP: Pre-existing bob-plugins npm test 5/5157 failures reproduce identically on clean HEAD f824dd1: freshness-namespace reload event (bob-cli-et), keep-inbox forced-check TZ 12:30 vs 16:30 (bob-cli-f7), note-ready startup storm 1!==2 and relationIndex layout-ready (bob-cli-eh), schedule-work-log future Pending 2026-11-02 (bob-cli-ff). Not caused by this phase.

[2026-11-02T20:29:44Z · bob-cli-g1.3] Verified 49/49 isolated real-Obsidian e2e (xvfb-run, /snap/bin/obsidian 1.15.0, scratch vault): compact 🔑N pill, light/dark LP+Reading, CSS unchanged (36.1×13.2px). Reading live-leaf refresh paints 🔑/🔓 after wrapped H2/list. Node 56/56 frees/progress/unblocked/e2e-self-test; npm run validate; just docs-check; bob plugins sync -F bob-ledger-tools. Full npm test 5152/5157 with 5 clean-base failures (et/f7/eh/ff).

## Dependencies

- **Depends on:** [bob-cli-g1.2](bob-cli-g1.2.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-g1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-g1.3/README.md) | [bob-cli-g1.3](bob-cli-g1.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`07edcdf`](https://github.com/bobs-org/bob-cli/commit/07edcdfa646ec234e2efee28dee7a201801e9f66) | docs(frees-marks): record live verification | [bob-cli-g1.3](bob-cli-g1.3.md) | 2026-11-02 15:30:36 EST |
| bob-plugins | [`bob-plugins@a28d1af`](https://github.com/bobs-org/bob-plugins/commit/a28d1af8a5f647486b33ea4e41312aaf331fe36b) | test(ledger-tools): real-Obsidian e2e for frees marks | [bob-cli-g1.3](bob-cli-g1.3.md) | 2026-11-02 15:30:53 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-g1.3][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-g1.3/README.md

<!-- sase:referenced-by:end -->
