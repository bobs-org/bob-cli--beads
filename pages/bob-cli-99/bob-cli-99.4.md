# Bead: bob-cli-99.4 — Put it on dash\_references, document, verify live

[Bead Pages](../README.md) / [bob-cli-99](README.md) / bob-cli-99.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.8z](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.8z.md) · **Assignee:** `bob-cli-99.4` · **Size:** small
**Created:** 2026-10-18 13:02:21 EDT · **Closed:** 2026-10-18 15:51:14 EDT
**Plan:** [202610/reading\_board.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/reading_board.md)

## Description

rollout: add the board above the existing table on dash_references, document it in docs/ref.md and docs/dashboard.md, verify against the live vault, record follow-ups, and handle the memory decision.

## Notes

[2026-10-18T19:50:26Z · bob-cli-99.4] PROPOSED FOLLOW-UP: Mac Refs panel inspector should show the wake date and prerequisite from blocked_by — the Mac bob already emits the field (checked read-only over ssh mac).

[2026-10-18T19:50:33Z · bob-cli-99.4] PROPOSED FOLLOW-UP: dash REFERENCES badge tooltip should split awake and snoozed counts — the badge still counts the Base view, per the epic scope.

[2026-10-18T19:50:41Z · bob-cli-99.4] PROPOSED FOLLOW-UP: revisit the Reading Board after two weeks of use (lane order, Snoozed grouping, card density) — scheduled review, not a defect.

[2026-10-18T19:50:54Z · bob-cli-99.4] PROPOSED FOLLOW-UP: Record decisions:reading-board-is-bob-rendered — skipped because the epic auto-decided memory_board_record=no; claim: board is a bob-reading-board block drawn from bob ref list JSON, read-only, blocked refs in a Snoozed lane with blocked_by reasons; rejected: Bases kanban grouped by frontmatter status (cannot see the ^ref task: 23 of 45 open refs were blocked) and a JS mirror of the blocking rules; cost: a spawn per revalidation; reopens when Bases can read task lines or the spawn fails on the Mac; links decisions:mac-capture-is-a-thin-client and decisions:subprojects-inherit-project-blocking; run sase memory init after.

[2026-10-18T19:51:03Z · bob-cli-99.4] PROPOSED FOLLOW-UP: Ask Bryan to run just install-all on the MacBook (reinstalls bob-cli and plugins, restarts Obsidian) and then open References to confirm the board — not run unasked per the plan.

[2026-10-18T19:51:14Z · bob-cli-99.4] Vault dash_references.md now has the bob-reading-board fence above the refs.base embed with the new description. docs/ref.md has a new 'Reading Board in Obsidian' section plus a pointer from the bob ref list section; docs/dashboard.md and docs/README.md updated. bob plugins sync: 19 unchanged (already deployed). Live check: bob ref list JSON has 46 rows (2 wip, 5 next, 16 ready, 23 blocked); preview-reading-board.cjs --input rendered lanes 2/5/16/23 with 53/53 browser checks passed; human bob ref list at wide width shows 23 reason suffixes, matching the 23 blocked rows. ssh mac bob already emits blocked_by. Failures reproduce without my changes (docs-only diff): npm test has the same 7 failures recorded on bob-cli-99.2/99.3; just test has 3 failures (pandoc_maps_every_contract_construct_to_tex, diagrams_swap_pdf_error_keeps_note_and_source, diagrams_absent_results_match_unhooked_pdf) in files this phase did not touch. Memory decision skipped per epic (memory_board_record=no) and recorded as a PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-99.1](bob-cli-99.1.md) ✓ · ⧖ 2026-10-18
- **Depends on:** [bob-cli-99.3](bob-cli-99.3.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-99.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.4/README.md) | [bob-cli-99.4](bob-cli-99.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b291f23`](https://github.com/bobs-org/bob-cli/commit/b291f23fe6e91252f8ff0a00ae0a4af2ca07bea0) | docs(ref): document the Obsidian Reading Board on dash\_references | [bob-cli-99.4](bob-cli-99.4.md) | 2026-10-18 15:52:16 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-99.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-99.4/README.md

<!-- sase:referenced-by:end -->
