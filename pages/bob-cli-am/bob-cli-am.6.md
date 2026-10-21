# Bead: bob-cli-am.6 — One aggregated links block per task in bob-ledger-tools

[Bead Pages](../README.md) / [bob-cli-am](README.md) / bob-cli-am.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.29.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.29.linker.w0.md) · **Assignee:** `bob-cli-am.6` · **Size:** medium
**Created:** 2026-10-21 10:08:37 EDT · **Closed:** 2026-10-21 11:25:23 EDT
**Plan:** [202610/undirected\_task\_relations.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/undirected_task_relations.md)

## Description

ledger-chips: add the additive `related()` per-task view to `api.relationIndex` and render one `🪢 links` block per task (arrow-free plain chips, then statements) in Live Preview and Reading view, collapsing the second relation line, with v2-aware × and ＋ controls.

## Notes

[2026-10-21T15:25:05Z · bob-cli-am.6] PROPOSED FOLLOW-UP: Full bob-plugins npm test shows 6 pre-existing failures identical on the clean base tree plus 1 timing flake: test-ledger-tools-unblocked-glyph.cjs x4 (tracked by bob-cli-6v), test-navigation-decision-card-handlers.cjs Keep counts x1 (tracked by bob-cli-6w), test-navigation-hotkeys-forward-promotion.cjs forward conversion x1 and a stage-ranker 16ms timing miss (both noted on bob-cli-9k.5); none touch relation code and all relation suites pass

[2026-10-21T15:25:23Z · bob-cli-am.6] ledger-chips done in bob-plugins: additive related() on api.relationIndex v1 (same-generation plain/outgoing/incoming, storedOn, redundant-hidden); per-task 🪢 links block (plain chips no arrow, then statements) in Live Preview with continuation-row fallback on the second line (recorded in docs; both raw lines reveal on selection) and in Reading view with the second li hidden; v2 unlink/removeStatement with v1 removeLink fallback; shared relation-inverse-vectors.cjs pinned by the ledger suite (nav adoption left to nav-stage per its plan step). Verified: 19/19 chips, 9/9 index incl. new related() test, 59/59 relation suites; npm build+docs:check+plugins sync green; 7 unrelated full-suite failures reproduce identically on the clean base (recorded as follow-up). No epic-symbol leftovers.

## Dependencies

- **Depends on:** [bob-cli-am.1](bob-cli-am.1.md) ✓ · ⧖ 2026-10-21
- **Blocks:** [bob-cli-am.7](bob-cli-am.7.md) ◐ · ⧖ 2026-10-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-am.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-am.6/README.md) | [bob-cli-am.6](bob-cli-am.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-am.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-am.6/README.md

<!-- sase:referenced-by:end -->
