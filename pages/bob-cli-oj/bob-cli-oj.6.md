# Bead: bob-cli-oj.6 — Group arms and hints in the links walker footer

[Bead Pages](../README.md) / [bob-cli-oj](README.md) / bob-cli-oj.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.6` · **Size:** medium
**Created:** 2026-11-21 07:41:35 EST · **Closed:** 2026-11-21 12:38:44 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

## Description

links-footer: add outer `«`/`»` group arms, the current-group context, the `]} next week` and boundary hints, ghost and creatable arm states, end-first shedding, and re-validated arm activation through the group commands.

## Notes

[2026-11-21T17:38:19Z · bob-cli-oj.6] PROPOSED FOLLOW-UP: skipped memory_decision_group_stops — epic DECISION is no; do not add decisions:group-stops-are-derived. Land agent may still file that strand in the glossary phase if policy changes.

[2026-11-21T17:38:24Z · bob-cli-oj.6] PROPOSED FOLLOW-UP: bob-cli docs-check fails on clean master: docs/reference/vault-format.md over budget at 6016 words (cap 6000). ledger-tools page was trimmed to 5999 so this phase stays under its own cap.

[2026-11-21T17:38:29Z · bob-cli-oj.6] PROPOSED FOLLOW-UP: live obsidian-walker-footer-e2e on athena proves week/daily group arms (W30: Q3 4/13 « Q2+ / Q4+ » ]} next quarter; 20261121: W47 6/7 « W46+ / W48+ » ]} next week) but geometryStable fails — .bob-bracket-mode x shifts with footer content width (s 819, w 956, n 1085, b 968 at 1400x900). Height stays 30. Pre-existing vs panel content width; this phase did not change s/w/b paint.

[2026-11-21T17:38:44Z · bob-cli-oj.6] links-footer in bob-ledger-tools 1.149.3: outer «/» group arms, context, ]} next week / ]n enters hints, ghost/creatable states, end-first shedding, revalidated group-command activation. npm test 8158 pass / 4 skip / 11 perf pass; unit footer table+ghost+conflict+shed+stale 54/54; live e2e on athena proved W30 Q3/Q2+/Q4+ next quarter and 20261121 W47/W46+/W48+ next week (geometryStable x-shift recorded as follow-up). Deployed with bob plugins sync -p bob-ledger-tools. Glossary strands left for oj.8; memory_decision_group_stops skipped per DECISION.

## Dependencies

- **Depends on:** [bob-cli-oj.1](bob-cli-oj.1.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-oj.2](bob-cli-oj.2.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-oj.4](bob-cli-oj.4.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.7](bob-cli-oj.7.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md) | [bob-cli-oj.6](bob-cli-oj.6.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.6][1] | Need the phase scope, notes, remaining work, and design | 5 |
| read-by | [agent:bob-cli-oj.7][2] | Need landed phase notes, versions, and follow-ups before adoption and e2e proof | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.7/README.md

<!-- sase:referenced-by:end -->
