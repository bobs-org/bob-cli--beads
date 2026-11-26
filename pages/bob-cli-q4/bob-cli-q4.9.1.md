# Bead: bob-cli-q4.9.1 — Settle cycler gestures without moving rapid-cycle targets

[Bead Pages](../README.md) / [bob-cli-q4.9](bob-cli-q4.9.md) / bob-cli-q4.9.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.9.md) · **Assignee:** `bob-cli-q4.9.1.land`
**Created:** 2026-11-25 14:32:38 EST
**Plan:** [202611/cycler\_gesture\_settle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/cycler_gesture_settle.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/cycler_gesture_settle.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/cycler_gesture_settle.md

<!-- sase:links:end -->

## Description

Complete bob-cli-q4.9 so closes, promotions, demotions, and committed scaffolds settle immediately, while status cycling settles safely after the burst.

## Notes

[2026-11-25T22:35:33Z · bob-cli-q4.9.1.land] LAND TRIAGE of PROPOSED FOLLOW-UPs (q4.9.1 lander):
(1) q4.9.1.1 #1 / q4.9.1.3 #2: just check bob-obsidian lib(3)+cli(18). Declined as a new task: already a DISCOVERED ISSUE on containing epic bob-cli-q4 (notes #1, #3: 17 cli settle-drift nodes, fresh reproduction at d67a5b7b, q4-owned) plus bob-cli-q5.1.1.x notes (wispr_summary, capture_complete drawer). Not caused by q4.9.1, which is JS-only in bob-plugins.
(2) q4.9.1.2 #2: cargo test --workspace, 22 Rust fixture/timing failures. Declined for the same reason as (1), same trackers.
(3) q4.9.1.1 #2 / q4.9.1.2 #1 / q4.9.1.3 #1: docs-check word budgets. Declined: tracked by bob-cli-ob (plugin-apis.md, bob-navigation-hotkeys.md), bob-cli-il (bob-ledger-tools.md), bob-cli-jz (capture-syntax.md), q4 note #2, and q7.1's own proposals (json-outputs.md and capture-syntax.md growth from q7.1). At 7d53d189 the lint reports capture-syntax 6058, json-outputs 6007, ledger-tools 6040, nav 6068, plugin-apis 9279 (advisory). q4.9.1's only docs growth is 3 words in the advisory plugin-apis row.
(4) q4.9.1.2 #3: one transient test:unit failure with no test named. Declined: no reproducible evidence. The lander's full test:unit at 7d53d189 has 9681 pass, 3 fail, all deterministic and attributable to (5). The known load flakes bob-cli-km and bob-cli-io already cover transient wall-clock failures.
(5) Lander finding: nav records settle jumps reversed (origin=cursor, destination=jumpTarget) and double-records cycler-owned pending flush outcomes, so the first Ctrl+O does not move. Also, master nav main.js is stale after 0e8c70b7, with 3 test:unit failures. Recorded as a DISCOVERED ISSUE on active epic bob-cli-q4.10.1, which owns 181a/181b and is mid-flight. No standalone task.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.9.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.9.1.land.md) | [bob-cli-q4.9.1](bob-cli-q4.9.1.md) | 4 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c665869`](https://github.com/bobs-org/bob-plugins/commit/c665869ec38b912f5ba7bb179003789fe96e7516) | fix(cycler): join gesture settles to undo history | [bob-cli-q4.9.1](bob-cli-q4.9.1.md) | 2026-11-25 18:26:44 EST |
| bob-plugins | [`bob-plugins@95e6a55`](https://github.com/bobs-org/bob-plugins/commit/95e6a55bd89ea1bf01b09fc699ef8de3210d4589) | test(cycler): enter Vim normal mode in Obsidian settle harness | [bob-cli-q4.9.1](bob-cli-q4.9.1.md) | 2026-11-25 18:44:59 EST |
| bob-plugins | [`bob-plugins@df44ab1`](https://github.com/bobs-org/bob-plugins/commit/df44ab12b1d4c50886a2014e21add82dc152ce88) | test(cycler): drive Vim escape through Obsidian handler | [bob-cli-q4.9.1](bob-cli-q4.9.1.md) | 2026-11-25 18:59:43 EST |
| bob-plugins | [`bob-plugins@e1ae072`](https://github.com/bobs-org/bob-plugins/commit/e1ae0729d7ec75c59b797eaa1e6cb82441eb3b4e) | test(cycler): fix real Obsidian settle harness | [bob-cli-q4.9.1](bob-cli-q4.9.1.md) | 2026-11-25 19:24:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.9.1.1][1] | Need parent epic DECISIONS and inherited contract | 1 |
| read-by | [agent:bob-cli-q4.9.1.3][2] | Need parent epic DECISIONS and remaining phase context | 1 |
| read-by | [agent:bob-cli-q4.9.1.4][3] | Need epic decisions and phase context before implementing cycle settle | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.9.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.9.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.9.1.4/README.md

<!-- sase:referenced-by:end -->
