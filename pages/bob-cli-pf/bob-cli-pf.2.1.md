# Bead: bob-cli-pf.2.1 — Generic bob props show and update

[Bead Pages](../README.md) / [bob-cli-pf.2](bob-cli-pf.2.md) / bob-cli-pf.2.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.md) · **Assignee:** `bob-cli-pf.2.1.land`
**Created:** 2026-11-22 14:47:18 EST
**Plan:** [202611/props\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/props_cli.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/props_cli.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/props_cli.md

<!-- sase:links:end -->

## Description

Complete bob-cli-pf.2 with an ordered property report and guarded, reversible frontmatter edits that preserve unrelated bytes and enforce one writer per key.

## Notes

[2026-11-22T22:53:38Z · research.5y.cld] DISCOVERED ISSUE: the props role table on master (src/native/props/roles.rs @ e98c7fe9, also origin/master) classifies every area/project bookkeeping key as loose, although the plan asks to 'audit bob's frontmatter writers to complete this list'. Missing derived keys: done_tasks (written by bob task archive; on 11 areas and 42 projects); project status (bob projects sync mirrors ^prj: checked→done, canceled→canceled, reopen→wip); leftover frontmatter scheduled on projects (projects sync hoists it onto ^prj); template (written by capture_project_note.rs:562, never read); task_count/open_task_count (written by the bob-project-tasks plugin, see bob-cli-pi). Impact: =+ on any area/project note would offer free-text edits of done_tasks (breaking archive pairing) and status: done on an open project (silently reverted by the next projects sync). Evidence: research:202611/area_project_property_cards__cld.md §1.4–§1.5, §5.5 (file:explicit:a4873a8805c572a2cd19068c).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.2.1.land/README.md) | [bob-cli-pf.2.1](bob-cli-pf.2.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.2.1.1--1][1] | Need epic decisions governing phase implementation and closure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.2.1.1.md

<!-- sase:referenced-by:end -->
