# Bead: bob-cli-eq — (( task wikilink picker in Obsidian

[Bead Pages](../README.md) / bob-cli-eq

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b5.md) · **Assignee:** `bob-cli-eq.land`
**Created:** 2026-10-30 16:10:20 EDT
**Plan:** [202610/obsidian\_task\_wikilinks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/obsidian_task_wikilinks.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/obsidian_task_wikilinks.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/obsidian_task_wikilinks.md

<!-- sase:links:end -->

## Description

Typing (( anywhere prose is allowed in an Obsidian note opens a fast, calm, keyboard-first picker over every task in the vault. Choosing a task replaces the token with the same [[note#^id]] block link Bob Mac Capture would insert, naming an ID-less task first. Under an open Pomodoro the link obeys Task Link rules. Nothing else ever changes by surprise.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-eq.1](bob-cli-eq.1.md) | Shared task wikilink rules and parity vectors | ✓ closed | medium | 2026-10-30 | 1 | 2 |
| [bob-cli-eq.2](bob-cli-eq.2.md) | Note grammar for the (( trigger | ✓ closed | small | 2026-10-30 | 1 | 1 |
| [bob-cli-eq.3](bob-cli-eq.3.md) | Warm vault task index | ✓ closed | medium | 2026-10-30 | 1 | 1 |
| [bob-cli-eq.4](bob-cli-eq.4.md) | Task Wikilink Picker card and identified-link insert | ◐ in_progress | medium | 2026-10-30 | 1 | 0 |
| [bob-cli-eq.5](bob-cli-eq.5.md) | Name-then-link for ID-less tasks | ◐ in_progress | small | 2026-10-30 | 1 | 0 |
| [bob-cli-eq.6](bob-cli-eq.6.md) | Task Link rules under an open Pomodoro | ◐ in_progress | medium | 2026-10-30 | 1 | 0 |
| [bob-cli-eq.7](bob-cli-eq.7.md) | Real-Obsidian verification, visual polish, and docs | ◐ in_progress | medium | 2026-10-30 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-eq: (( task wikilink picker in Obsidian [in_progress]"]
    n1["bob-cli-eq.1: Shared task wikilink rules and parity vectors [closed]"]
    n2["bob-cli-eq.2: Note grammar for the (( trigger [closed]"]
    n3["bob-cli-eq.3: Warm vault task index [closed]"]
    n4["bob-cli-eq.4: Task Wikilink Picker card and identified-link insert [in_progress]"]
    n5["bob-cli-eq.5: Name-then-link for ID-less tasks [in_progress]"]
    n6["bob-cli-eq.6: Task Link rules under an open Pomodoro [in_progress]"]
    n7["bob-cli-eq.7: Real-Obsidian verification, visual polish, and docs [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n3
    n2 -.-> n4
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eq.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.1/README.md) | [bob-cli-eq.1](bob-cli-eq.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-eq.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.2/README.md) | [bob-cli-eq.2](bob-cli-eq.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-eq.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.3/README.md) | [bob-cli-eq.3](bob-cli-eq.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-eq.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.4/README.md) | [bob-cli-eq.4](bob-cli-eq.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-eq.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.5/README.md) | [bob-cli-eq.5](bob-cli-eq.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-eq.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.6/README.md) | [bob-cli-eq.6](bob-cli-eq.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-eq.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.7/README.md) | [bob-cli-eq.7](bob-cli-eq.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-eq.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.land/README.md) | [bob-cli-eq](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@27acd61`](https://github.com/bobs-org/bob-plugins/commit/27acd61630e576e9964ab9639fe09b5c96762fc3) | feat(block-id-prompt): pure (( trigger grammar with vectors and tests | [bob-cli-eq.2](bob-cli-eq.2.md) | 2026-10-30 16:27:23 EDT |
| bob-cli | [`ebd74b7`](https://github.com/bobs-org/bob-cli/commit/ebd74b7b7a21b3888623651a54997fbe9cea2550) | feat(capture): add task-wikilink ranker vectors and candidates tests | [bob-cli-eq.1](bob-cli-eq.1.md) | 2026-10-30 16:51:08 EDT |
| bob-plugins | [`bob-plugins@9dd0374`](https://github.com/bobs-org/bob-plugins/commit/9dd0374e2d19dd5397a9887d2e7b07561d146bdc) | feat(block-id-prompt): mirror task-wikilink rank model with vectors and tests | [bob-cli-eq.1](bob-cli-eq.1.md) | 2026-10-30 17:04:25 EDT |
| bob-plugins | [`bob-plugins@4ef761a`](https://github.com/bobs-org/bob-plugins/commit/4ef761a6ec491e607c405ee4d7bf0a1867c1a145) | feat(block-id-prompt): warm vault task index for the (( picker | [bob-cli-eq.3](bob-cli-eq.3.md) | 2026-10-30 17:40:44 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eq.1][1] | Need epic scope for eq.1 phase work | 1 |
| read-by | [agent:bob-cli-eq.2][2] | epic scope and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.2/README.md

<!-- sase:referenced-by:end -->
