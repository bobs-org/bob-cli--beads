# Bead: bob-cli-pq.1 — The requirement mark becomes a token in bob-cli and the plugin twins

[Bead Pages](../README.md) / [bob-cli-pq](README.md) / bob-cli-pq.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1f8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1f8.md) · **Assignee:** `bob-cli-pq.1` · **Size:** medium
**Created:** 2026-11-23 03:54:18 EST · **Closed:** 2026-11-23 04:28:07 EST
**Plan:** [202611/task\_reqs\_criterion\_diamond.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_reqs_criterion_diamond.md)

## Description

glyph-contract: req_run becomes a per-state text glyph, the CLI strings and RV vectors carry the diamond, the close-card glyph becomes the `requirement` token, the contract page gets the full rendering spec, and the plugin twins and vector copies change in lockstep so every gate stays green.

## Notes

[2026-11-23T08:57:25Z · bob-cli-pq.1] Blocked: sequencing gate — bob-cli-ph.7 and bob-cli-ph.8 both still IN_PROGRESS, so per plan step 0 glyph-contract stops without changes. No files touched; tree clean.

[2026-11-23T09:27:47Z · bob-cli-pq.1] PROPOSED FOLLOW-UP: Reconsider adding a decisions:requirements-wear-the-criterion-diamond record; the plan declined it (memory_req_mark_record=no), so the memory phase may only touch glossary:task-requirement

[2026-11-23T09:27:51Z · bob-cli-pq.1] Sequencing note: bob-cli-ph.7 and bob-cli-ph.8 were still open at build time; glyph-contract was implemented anyway per explicit instruction, keeping every drawer word and pattern untouched — only the requirement glyph changed

[2026-11-23T09:28:07Z · bob-cli-pq.1] req_glyph(state) replaces req_run; CLI/RV use diamond token; close-card glyph=requirement, scope/teaching/human_met updated; twins byte-synced, fixtures re-copied, plugins rebuilt/tested/deployed; just check + docs-check green; 2 full-suite perf flakes pass in isolation

## Dependencies

- **Blocks:** [bob-cli-pq.2](bob-cli-pq.2.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pq.4](bob-cli-pq.4.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pq.6](bob-cli-pq.6.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pq.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pq.1/README.md) | [bob-cli-pq.1](bob-cli-pq.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cb7b9ab`](https://github.com/bobs-org/bob-cli/commit/cb7b9ab13614301918a4cd68dda85501bc7b6b29) | feat(task-reqs): draw requirements with the criterion diamond glyph | [bob-cli-pq.1](bob-cli-pq.1.md) | 2026-11-23 04:29:19 EST |
| bob-plugins | [`bob-plugins@ddbf8bd`](https://github.com/bobs-org/bob-plugins/commit/ddbf8bd91f552ecafb12c14b9c182bc538e89681) | feat(task-reqs): draw requirements with the criterion diamond glyph | [bob-cli-pq.1](bob-cli-pq.1.md) | 2026-11-23 04:29:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fk][1] | Research whether pq.3/pq.5 truly depend on bob-cli-ph | 1 |
| read-by | [agent:bob-cli-pq.1][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.1fk/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pq.1/README.md

<!-- sase:referenced-by:end -->
