# Bead: bob-cli-ft.3.1 — Blocked checkbox rendering and verification for bob-cli-ft.3

[Bead Pages](../README.md) / [bob-cli-ft.3](bob-cli-ft.3.md) / bob-cli-ft.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ft.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.md) · **Assignee:** `bob-cli-ft.3.1.land`
**Created:** 2026-11-02 07:34:43 EST · **Closed:** 2026-11-02 11:44:56 EST
**Plan:** [202611/block\_marks\_editor.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/block_marks_editor.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/block_marks_editor.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:123b0af950b157cd98921769 | attached via sase artifact create --bead |
| related | file:explicit:1656bef2dea171eba6964f38 | attached via sase artifact create --bead |
| related | file:explicit:3dc753f559a57517a7a5bed9 | attached via sase artifact create --bead |
| related | file:explicit:3ee7ff7fe8a3e65c2a00b7ca | attached via sase artifact create --bead |
| related | file:explicit:43f614454c48c21b61cea418 | attached via sase artifact create --bead |
| related | file:explicit:460358b1b87b654ffd8f5e5c | attached via sase artifact create --bead |
| related | file:explicit:55a612058c1373e9ca6880b1 | attached via sase artifact create --bead |
| related | file:explicit:560a0424655432c08f3a62b5 | attached via sase artifact create --bead |
| related | file:explicit:7a6f9f6a48c085ec27cb91b6 | attached via sase artifact create --bead |
| related | file:explicit:b2825fb913c4cb5f79048abc | attached via sase artifact create --bead |
| related | file:explicit:d56219a291b8599f2685ac7e | attached via sase artifact create --bead |
| related | file:explicit:f826b23ed46ccb980f3496b6 | attached via sase artifact create --bead |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/block_marks_editor.md

<!-- sase:links:end -->

## Description

Blocked task checkboxes show their proven reason across Live Preview and rendered source-note surfaces, with accessible tooltips, reversible toggling, a shared miniature API, and verified light/dark Obsidian behavior; bob-cli-ft.3 is completed.

## Notes

[2026-11-02T15:32:30Z · bob-cli-ft.3.1.land] FOLLOW-UP TRIAGE before landing-repair tale: reviewed every note on children .1-.4; sase_new_task semantic search, last-week all-status sweep, and all 22 active-epic scopes found the repeated proposals are existing external test defects, with no active-epic causal owner. Corroborated bob-cli-et (freshness reload; .1 #1/.2 #1/.3 #4/.4 #1), bob-cli-f7 (UTC/local notice; .1 #1/.2 #1/.3 #1/.4 #1), bob-cli-eh (startup fake pair; .1 #1/.2 #1/.3 #3/.4 #1), bob-cli-ff (expired schedule date; .1 #1/.2 #1/.3 #2/.4 #1), and bob-cli-f8 (performance budgets; .2 #1/.4 #1), each with file:explicit:55a612058c1373e9ca6880b1. Independent run at bob-plugins 4502b73: 112/119 pass, same five deterministic failures plus snapshot 75.0ms >50 and cold chunk 16.8ms >16; ranking passes. Do not call all phase full-suite failures identical or load-only flakes. The isolated base-only reduced-motion miss from .2 #1 is declined as a separate task: current motion suite passes 2/2 and phase focused run passed; no reproduced distinct failure or evidence warranting another task. Cold-chunk observation stays on f8 without claiming a proven shared root cause. No new task created. Epic-caused rendering and harness gaps remain this epic work and go into a medium tale; copy this disposition into the final close note.

[2026-11-02T15:37:02Z · bob-cli-ft.3.1.land] LAND AUDIT: reviewed epic/all four children/all notes, accepted child and parent plans/DECISIONS, plugin commits 89dae58/257255e/5f1c23c/bded172 and CLI 311b1514/a7931a64. Current bob-cli a7931a64 and plugins 4502b73 match fetched origin/master. No conflicting new API consumer: Stats clocks, off-clock tag chip, relation-successor writes, CLI section completion, event ordering/default starts, escaping and CANCEL LOG indentation stay independent; starts-after relations must not become blocking dependencies. 46 block-mark tests and 158 neighboring/shared-fence-helper tests pass. Four standalone probes fail: recycled fallback retains removed date; repeated off sweep clobbers new external aria; Tasks row as processor root is marked; Dataview with no proven origin gets date. Full probe source file:explicit:1656bef2dea171eba6964f38; first-three failure log file:explicit:7a6f9f6a48c085ec27cb91b6. Prior real-app report file:explicit:ee8f976abf31be54c7612c4b has tooltip tip empty while marked pass, because aria satisfies the assertion; snippet removal/refresh/day/config/host checks also fail to prove accepted scenarios. Inspected dark screenshot against mockup; basic appearance aligns, but aggregate marks cannot prove owned checkboxes or tooltip behavior. These are epic-caused remaining work, not task follow-ups. Medium tale sase_plan_block_marks_landing_repair.md repairs the adapter, strengthens/reruns isolated real-app evidence, carries triage dispositions, and concretely closes this epic and parent phase bob-cli-ft.3 in the coder turn. No epic-symbol entries for either bead; no symvision recipe. Both beads deliberately remain open, original plan remains wip.

[2026-11-02T16:44:56Z · bob-cli-ft.3.1.land--1] Landing-repair complete and just check passed (monitor rp04x2zzmm7r, exit 0). Child phases .1–.4 and original decisions remain complete: own_first, chevron, quiet, memory_decision_record=no; stored Markdown stays [?].

Checks: primary just check passed after adapter/editor landing repair; focused reading 28/28; live xvfb e2e 114/114; report file:explicit:f826b23ed46ccb980f3496b6; npm run validate and docs:check passed; primary just docs-check passed. Manifest 1.90.1. Vault left at clean 1.90.0 from canonical bob-plugins 806ba69: bob plugins sync --no-pull refused because forcing would regress day-strip. Host commits after this turn. Origin bob-plugins +3 (ffe1727, 806ba69, 1115a14) and bob-cli +6 have no block-marks fragment overlap; did not rebase.

Dispositions:
- et, f7, eh, ff, f8: corroborated existing tasks; independent evidence file:explicit:55a612058c1373e9ca6880b1; no new task.
- Reduced-motion: declined; focused motion tests pass 2/2.
- Live Dataview of this Obsidian build does not emit origin; harness injects proven origin on BM4; adapter recovers from Tasks cache; unprovable rows stay unmarked.
- BM23 is a controlled clock (dateMarksToday + refreshDateMarksForRollover), not a midnight observation.

Leave outer epic bob-cli-ft open.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.1.land.md) | [bob-cli-ft.3.1](bob-cli-ft.3.1.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`217341c`](https://github.com/bobs-org/bob-cli/commit/217341c40c6842f824e565dc52e8c42d2e7b76ae) | docs(blocked-marks): record landing-repair live verification | [bob-cli-ft.3.1](bob-cli-ft.3.1.md) | 2026-11-02 11:46:56 EST |
| bob-plugins | [`bob-plugins@de8fb6b`](https://github.com/bobs-org/bob-plugins/commit/de8fb6bf5fae6c7efccdbb26df903c5561293eda) | fix(block-marks): repair reading adapter and editor tooltip landing | [bob-cli-ft.3.1](bob-cli-ft.3.1.md) | 2026-11-02 11:47:18 EST |
| bob-cli--plans | [`bob-cli--plans@f4c0e7d`](https://github.com/bobs-org/bob-cli--plans/commit/f4c0e7d63d5946ca0fa9780d1f7402338c0c931c) | chore(plans): mark block\_marks\_editor epic done | [bob-cli-ft.3.1](bob-cli-ft.3.1.md) | 2026-11-02 11:47:35 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ft.3.1.1][1] | Need child epic scope for paint_api phase | 1 |
| read-by | [agent:bob-cli-ft.3.1.2--2][2] | Need the child epic's final decisions that govern this phase | 1 |
| read-by | [agent:bob-cli-ft.3.1.3][3] | Need parent epic DECISIONS for rendered_views phase | 1 |
| read-by | [agent:bob-cli-ft.3.1.4][4] | Need parent epic decisions and handoff | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.1.2.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.4/README.md

<!-- sase:referenced-by:end -->
