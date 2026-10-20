# Bead: bob-cli-a0.10.1 — Publish the generated Obsidian plugin reference

[Bead Pages](../README.md) / [bob-cli-a0.10](bob-cli-a0.10.md) / bob-cli-a0.10.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.10.md) · **Assignee:** `bob-cli-a0.10.1.land`
**Created:** 2026-10-19 23:16:00 EDT
**Plan:** [202610/plugin\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plugin_reference.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/plugin_reference.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plugin_reference.md

<!-- sase:links:end -->

## Description

Complete bob-cli-a0.10 with source-owned documentation for all seven plugins, generated command and version facts, a concise README, and verified reference and development mounts in the Bob site.

## Notes

[2026-10-20T05:21:12Z · bob-cli-a0.10.1.land] LAND TRIAGE (bob-cli-a0.10.1.land): PROPOSED FOLLOW-UPs from .2#1, .3#2, .4#1, .5#2 all describe pre-existing bob-plugins npm test failures not caused by this docs-only epic; each is an existing READY task, corroborated once with +1: bob-cli-6v (unblocked-glyph x4), bob-cli-6w (Keep counts once), bob-cli-7i (project conversion BLOCKS ^prj link), bob-cli-3w (stage-ranker 16ms budget; .4's 'stage-entry 17.87ms, no matching bead' is the same test stage-ranker-filters-1000-synthetic-tasks-under-16-ms-per-keystroke, so no new task). .5#1 limitation 'live urls.txt not published yet' belongs to active epic bob-cli-a0.5.1 (first publish in a0.5.1.5) and was declined as a follow-up. .5#1 limitation 'publish workflow has no setup-node' is caused by this epic (bob-docs check --production now runs the Node inventory generator) and is folded into the remaining-work tale. Discovered while landing: docs-publish.yml/docs-weekly.yml jobs lack runs-on — caused by active epic bob-cli-a0.5.1, recorded there as a DISCOVERED ISSUE note, no task created.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.10.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.10.1.land.md) | [bob-cli-a0.10.1](bob-cli-a0.10.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.10.1.1][1] | Need epic DECISIONS that this phase must honor | 2 |
| read-by | [agent:bob-cli-a0.10.1.2][2] | Review the epic decisions governing this implementation | 1 |
| read-by | [agent:bob-cli-a0.10.1.3][3] | Need parent epic DECISIONS and phase scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.3/README.md

<!-- sase:referenced-by:end -->
