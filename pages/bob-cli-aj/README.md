# Bead: bob-cli-aj — Reliable \`\|\` relation-card trigger in Bob Mac Capture

[Bead Pages](../README.md) / bob-cli-aj

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.12t](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12t.md) · **Assignee:** `bob-cli-aj.land`
**Created:** 2026-10-21 08:01:49 EDT
**Plan:** [202610/relation\_pipe\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_pipe_card.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/relation_pipe_card.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_pipe_card.md

<!-- sase:links:end -->

## Description

Typing `|` after a `~note:id` / `~~note:id` relation token in Bob Mac Capture always opens the relation card, with or without a space before the `|`. The card shows the correct direction, and committing a label never deletes text after the token.

## Notes

[2026-10-21T13:12:47Z · research.29.final] DISCOVERED ISSUE: (corroboration from research.29 lead, undirected task relations research) The data-loss case this epic targets is reproducible at the Bob level. A read-only probe 'bob capture-complete -f json --cursor 49' on the leading-run draft '~sase:ref-athena-apollo-operational-log-audit|"see Fix it' (installed bob built after bcc201fe) returned context relation_label, replacement range {start:45,end:57} covering through the end of the draft, and typed candidate '|see'. Meanwhile CapturePanelModel.insertRelationLabelReplacement (bob-mac-capture bf30f9e, :6695-6702) replaces token end through draft end, and the label probe splices '|"typed' before the tail (:6740-6754). Accepting a label for '~sase:x Fix it' would therefore drop ' Fix it'. Please cover leading-run tokens and a modifier after the token ('Fix it ~a:b &c:d') in aj.2's tests. Details: research:202610/undirected_task_relations/undirected_task_relations__final.md section 8.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-aj.1](bob-cli-aj.1.md) | bob-cli relation-label typing assist and completion contract | ✓ closed | medium | 2026-10-21 | 1 | 1 |
| [bob-cli-aj.2](bob-cli-aj.2.md) | Bob Mac Capture relation-card trigger and label-range fixes | ✓ closed | medium | 2026-10-21 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-aj: Reliable `|` relation-card trigger in Bob Mac Capture [in_progress]"]
    n1["bob-cli-aj.1: bob-cli relation-label typing assist and completion contract [closed]"]
    n2["bob-cli-aj.2: Bob Mac Capture relation-card trigger and label-range fixes [closed]"]
    n0 --> n1
    n0 --> n2
    n1 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-aj.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aj.1/README.md) | [bob-cli-aj.1](bob-cli-aj.1.md) | 1 |
| [bbugyi200.athena.bob-cli-aj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-aj.2.md) | [bob-cli-aj.2](bob-cli-aj.2.md) | 1 |
| [bbugyi200.athena.bob-cli-aj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-aj.land/README.md) | [bob-cli-aj](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bcc201f`](https://github.com/bobs-org/bob-cli/commit/bcc201feebc262f2b4f16569e959bd03cedecce4) | feat(capture): attach relation labels on typed pipe and expose relation in completions | [bob-cli-aj.1](bob-cli-aj.1.md) | 2026-10-21 08:28:52 EDT |
| bob-mac-capture | [`bob-mac-capture@bf40f48`](https://github.com/bobs-org/bob-mac-capture/commit/bf40f48c465378ad175fdc8817f6a95f8c0f54da) | feat(capture): open relation label cards from typed pipe | [bob-cli-aj.2](bob-cli-aj.2.md) | 2026-10-21 09:46:45 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.29.final][1] | Check whether the relation-card truncation bug falls in this epic's scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.29.final/README.md

<!-- sase:referenced-by:end -->
