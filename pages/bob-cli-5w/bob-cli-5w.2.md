# Bead: bob-cli-5w.2 — Specify Successor Links once, in docs and vectors

[Bead Pages](../README.md) / [bob-cli-5w](README.md) / bob-cli-5w.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0p.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0p.linker.w0.md) · **Assignee:** `bob-cli-5w.2` · **Size:** medium
**Created:** 2026-10-09 11:54:15 EDT · **Closed:** 2026-10-09 12:19:00 EDT
**Plan:** [202610/successor\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/successor_links.md)

## Description

contract: in bob-cli docs, add task-dependencies §12 (rule, anchors, placement, writes, reporting model, copy) plus §11.6 SL and SB vectors, with SB pinned by a Rust unit test. Rewrite the capture.md `!`, close, JSON, and human-output contracts. Document `plan.link_unblocked` and nav `api.notice`.

## Notes

[2026-10-09T16:18:28Z · bob-cli-5w.2] PROPOSED FOLLOW-UP: just check stays red on 9 pre-existing highlights_ref::return_links filter failures, identical on the clean base tree; already tracked by bead bob-cli-5t (Pandoc hyperlink form)

[2026-10-09T16:18:33Z · bob-cli-5w.2] PROPOSED FOLLOW-UP: record decisions strand closed-task-hands-slot-to-successors (claim, rejected alternatives, cost, reopens-when) per epic closeout memory decision

[2026-10-09T16:18:38Z · bob-cli-5w.2] PROPOSED FOLLOW-UP: add glossary strand successor-link cross-linked to task-link and task-dependency-link per epic closeout memory decision

[2026-10-09T16:19:00Z · bob-cli-5w.2] Contract landed: task-dependencies.md gained §12 (rule/anchors/writes/reporting/copy/perf/kill-switch/undo), §11.6 SL1-SL28, §11.7 SB1-SB9, §5 closing bullet, §9 nav notice member; capture.md ! step 6, close, JSON, and human-output contracts rewritten; plan.link_unblocked documented in plan.md; hooks Ctrl+Enter paragraph fixed. New mint_block_id plus SB unit test passes (4/4 capture_block_ids tests green); cargo fmt and clippy clean. Full just check red only on 9 pre-existing highlights_ref return_links failures, identical on clean base, tracked by bob-cli-5t.

## Dependencies

- **Blocks:** [bob-cli-5w.3](bob-cli-5w.3.md) ◐ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5w.6](bob-cli-5w.6.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5w.7](bob-cli-5w.7.md) ◐ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5w.9](bob-cli-5w.9.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5w.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.2/README.md) | [bob-cli-5w.2](bob-cli-5w.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`16df9b6`](https://github.com/bobs-org/bob-cli/commit/16df9b6a63161023f1acb1a828fe8af4d1cfa886) | feat(deps): add Successor Links contract docs and vectors | [bob-cli-5w.2](bob-cli-5w.2.md) | 2026-10-09 12:21:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5w.2][1] | check notes and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5w.2/README.md

<!-- sase:referenced-by:end -->
