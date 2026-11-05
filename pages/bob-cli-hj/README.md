# Bead: bob-cli-hj — Place past Pomodoros on today's timeline with the x= segment suffix

[Bead Pages](../README.md) / bob-cli-hj

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18s](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18s.md) · **Assignee:** `bob-cli-hj.land`
**Created:** 2026-11-05 14:25:23 EST
**Plan:** [202611/past\_pomodoro\_segment\_suffix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/past_pomodoro_segment_suffix.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/past_pomodoro_segment_suffix.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/past_pomodoro_segment_suffix.md

<!-- sase:links:end -->

## Description

`x=E[~|~n|~n+|~~][!][=X]` records past work against an edge of today's timeline (the tail since the last closed Pomodoro, a closed Pomodoro, a gap, or the head before the first row). Placement is exact and guarded, every cut is reported, and a plain `x=` stays byte-for-byte unchanged. bob ships a segment picker, a typed `-` to `~` assist, and a stale-preview guard. Bob Mac Capture renders the suffix, the picker, and a card that names the segment.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-hj.1](bob-cli-hj.1.md) | Timeline catalog and pinned layout engine | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-hj.2](bob-cli-hj.2.md) | Segment suffix lexer, pins, spans, and teaching errors | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-hj.3](bob-cli-hj.3.md) | Record pinned runs end to end and ship grammar 14 | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-hj.4](bob-cli-hj.4.md) | Segment picker, dash-to-tilde rewrite, and submit guards | ✓ closed | medium | 2026-11-05 | 1 | 1 |
| [bob-cli-hj.5](bob-cli-hj.5.md) | Decision record for segment placement | ✓ closed | small | 2026-11-05 | 1 | 0 |
| [bob-cli-hj.6](bob-cli-hj.6.md) | Bob Mac Capture segment typing, picker, card, and guard | ◐ in_progress | medium | 2026-11-05 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-hj: Place past Pomodoros on today's timeline with the x= segment suffix [in_progress]"]
    n1["bob-cli-hj.1: Timeline catalog and pinned layout engine [closed]"]
    n2["bob-cli-hj.2: Segment suffix lexer, pins, spans, and teaching errors [closed]"]
    n3["bob-cli-hj.3: Record pinned runs end to end and ship grammar 14 [closed]"]
    n4["bob-cli-hj.4: Segment picker, dash-to-tilde rewrite, and submit guards [closed]"]
    n5["bob-cli-hj.5: Decision record for segment placement [closed]"]
    n6["bob-cli-hj.6: Bob Mac Capture segment typing, picker, card, and guard [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n3
    n2 -.-> n3
    n3 -.-> n4
    n3 -.-> n5
    n4 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.1/README.md) | [bob-cli-hj.1](bob-cli-hj.1.md) | 1 |
| [bbugyi200.athena.bob-cli-hj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.2/README.md) | [bob-cli-hj.2](bob-cli-hj.2.md) | 1 |
| [bbugyi200.athena.bob-cli-hj.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.3/README.md) | [bob-cli-hj.3](bob-cli-hj.3.md) | 1 |
| [bbugyi200.athena.bob-cli-hj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.4/README.md) | [bob-cli-hj.4](bob-cli-hj.4.md) | 1 |
| [bbugyi200.athena.bob-cli-hj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.5/README.md) | [bob-cli-hj.5](bob-cli-hj.5.md) | 0 |
| [bbugyi200.athena.bob-cli-hj.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.6/README.md) | [bob-cli-hj.6](bob-cli-hj.6.md) | 0 |
| [bbugyi200.athena.bob-cli-hj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.land/README.md) | [bob-cli-hj](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ae33095`](https://github.com/bobs-org/bob-cli/commit/ae330951b597c55360a854674bf5ba2f775411c1) | feat(capture): add timeline catalog and pinned layout engine | [bob-cli-hj.1](bob-cli-hj.1.md) | 2026-11-05 16:51:13 EST |
| bob-cli | [`6e81677`](https://github.com/bobs-org/bob-cli/commit/6e816775f0252b6bd68af2900699e6bd537168fb) | feat(capture): segment suffix lexer, pins, spans, and teaching errors | [bob-cli-hj.2](bob-cli-hj.2.md) | 2026-11-05 16:59:22 EST |
| bob-cli | [`86554bf`](https://github.com/bobs-org/bob-cli/commit/86554bf66551e6f44dd269295cfca19eba570a65) | feat(capture): record pinned past-Pomodoro segments and ship grammar 14 | [bob-cli-hj.3](bob-cli-hj.3.md) | 2026-11-05 17:42:43 EST |
| bob-cli | [`35c2a42`](https://github.com/bobs-org/bob-cli/commit/35c2a426c3411a91e7825c64adf1121fe013e9ac) | feat(capture): add past-Pomodoro segment picker, dash rewrite, and submit guards | [bob-cli-hj.4](bob-cli-hj.4.md) | 2026-11-05 18:50:38 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hj.3][1] | epic context for phase 3 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-hj.3/README.md

<!-- sase:referenced-by:end -->
