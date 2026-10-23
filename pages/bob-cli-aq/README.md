# Bead: bob-cli-aq — One-key recommended roll (Alt+P) with review-walk previews

[Bead Pages](../README.md) / bob-cli-aq

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.132](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.132.md) · **Assignee:** `bob-cli-aq.land`
**Created:** 2026-10-23 06:34:43 EDT
**Plan:** [202610/quick\_roll\_alt\_p.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/quick_roll_alt_p.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/quick_roll_alt_p.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/quick_roll_alt_p.md

<!-- sase:links:end -->

## Description

One keystroke on a task applies exactly what the Task Card's Ctrl+Enter recommends (same-level roll, decay, or a confirmed cancel), and every GTD review landing and the review footer say in a few words which priority that key would use and whether it decays.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-aq.1](bob-cli-aq.1.md) | The one-key roll command in bob-navigation-hotkeys | ✓ closed | medium | 2026-10-23 | 1 | 0 |
| [bob-cli-aq.2](bob-cli-aq.2.md) | Roll preview on review-walk landings and api.quickRoll | ✓ closed | medium | 2026-10-23 | 1 | 0 |
| [bob-cli-aq.3](bob-cli-aq.3.md) | Roll preview in the review footer | ✓ closed | small | 2026-10-23 | 1 | 0 |
| [bob-cli-aq.4](bob-cli-aq.4.md) | Review contract, API contract, and memory updates in bob-cli | ✓ closed | small | 2026-10-23 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-aq: One-key recommended roll (Alt+P) with review-walk previews [in_progress]"]
    n1["bob-cli-aq.1: The one-key roll command in bob-navigation-hotkeys [closed]"]
    n2["bob-cli-aq.2: Roll preview on review-walk landings and api.quickRoll [closed]"]
    n3["bob-cli-aq.3: Roll preview in the review footer [closed]"]
    n4["bob-cli-aq.4: Review contract, API contract, and memory updates in bob-cli [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n1 -.-> n4
    n2 -.-> n3
    n2 -.-> n4
    n3 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-aq.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-aq.1.md) | [bob-cli-aq.1](bob-cli-aq.1.md) | 0 |
| [bbugyi200.athena.bob-cli-aq.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aq.2/README.md) | [bob-cli-aq.2](bob-cli-aq.2.md) | 0 |
| [bbugyi200.athena.bob-cli-aq.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aq.3/README.md) | [bob-cli-aq.3](bob-cli-aq.3.md) | 0 |
| [bbugyi200.athena.bob-cli-aq.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aq.4/README.md) | [bob-cli-aq.4](bob-cli-aq.4.md) | 1 |
| [bbugyi200.athena.bob-cli-aq.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aq.land/README.md) | [bob-cli-aq](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8da0c84`](https://github.com/bobs-org/bob-cli/commit/8da0c843ca52dafb88dc34c4e49b2de25ddd916f) | docs(freshness): document Alt+P review roll preview | [bob-cli-aq.4](bob-cli-aq.4.md) | 2026-10-23 07:53:14 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-aq.2][1] | parent epic scope | 1 |
| read-by | [agent:research.55.final][2] | Check overlap of in-progress Alt+P review-walk preview epic with proposed Rotten Log prompt | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aq.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.55.final/README.md

<!-- sase:referenced-by:end -->
