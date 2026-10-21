# Bead: bob-cli-ak — PRE/POST checklist glyphs and compact recurrence marks

[Bead Pages](../README.md) / bob-cli-ak

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.28.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.28.linker.w0.md) · **Assignee:** `bob-cli-ak.land`
**Created:** 2026-10-21 08:49:59 EDT
**Plan:** [202610/gtd\_checklist\_glyphs\_and\_recurrence\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gtd_checklist_glyphs_and_recurrence_marks.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/gtd_checklist_glyphs_and_recurrence_marks.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gtd_checklist_glyphs_and_recurrence_marks.md

<!-- sase:links:end -->

## Description

In Obsidian, a canonical `#task #gtd #pre` / `#task #gtd #post` run renders as one teal sunrise / flag identity glyph, and every readable `[repeat:: …]` rule renders as a quiet loop glyph plus a spoken cadence (`daily`, `Mondays`, `monthly · 1st`). This works in Live Preview, reading view, and Tasks query results. Nothing changes in storage, and anything uncertain keeps its honest pill.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ak.1](bob-cli-ak.1.md) | PRE/POST checklist identity glyphs | ✓ closed | medium | 2026-10-21 | 1 | 2 |
| [bob-cli-ak.2](bob-cli-ak.2.md) | Recurrence marks in Live Preview and rendered views | ✓ closed | medium | 2026-10-21 | 1 | 1 |
| [bob-cli-ak.3](bob-cli-ak.3.md) | Recurrence marks in Tasks query results | ◐ in_progress | small | 2026-10-21 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ak: PRE/POST checklist glyphs and compact recurrence marks [in_progress]"]
    n1["bob-cli-ak.1: PRE/POST checklist identity glyphs [closed]"]
    n2["bob-cli-ak.2: Recurrence marks in Live Preview and rendered views [closed]"]
    n3["bob-cli-ak.3: Recurrence marks in Tasks query results [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n2
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ak.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ak.1.md) | [bob-cli-ak.1](bob-cli-ak.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-ak.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ak.2/README.md) | [bob-cli-ak.2](bob-cli-ak.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ak.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ak.3/README.md) | [bob-cli-ak.3](bob-cli-ak.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-ak.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ak.land/README.md) | [bob-cli-ak](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8a4936f`](https://github.com/bobs-org/bob-cli/commit/8a4936f4879a326034aae934c392c6e332d3c067) | docs(task-tag-marks): specify PRE and POST glyph behavior | [bob-cli-ak.1](bob-cli-ak.1.md) | 2026-10-21 09:20:29 EDT |
| bob-plugins | [`bob-plugins@328d212`](https://github.com/bobs-org/bob-plugins/commit/328d212f03acb44bd23d5a14bd592c8de7f5bdca) | feat(ledger-tools): add PRE and POST checklist glyphs | [bob-cli-ak.1](bob-cli-ak.1.md) | 2026-10-21 09:21:40 EDT |
| bob-cli | [`6e34d50`](https://github.com/bobs-org/bob-cli/commit/6e34d5076b16e718a1f750fb769cba4bdc1bc5df) | docs(date-marks): specify recurrence-mark display contract and vault repeat row | [bob-cli-ak.2](bob-cli-ak.2.md) | 2026-10-21 09:50:08 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ak.1--1][1] | Need epic decisions and prior phase notes before closing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ak.1.md

<!-- sase:referenced-by:end -->
