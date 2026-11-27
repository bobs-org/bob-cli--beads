# Bead: bob-cli-r8 — Task-bead burn-down 2: false deploy refusals, a red dotfiles CI, and leaking e2e scratch

[Bead Pages](../README.md) / bob-cli-r8

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r7.land.md) · **Assignee:** `bob-cli-r8.land`
**Created:** 2026-11-27 13:01:15 EST
**Plan:** [202611/task\_bead\_burndown\_2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_2.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/task_bead_burndown_2.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_2.md

<!-- sase:links:end -->

## Description

The five open task beads that now cost agents the most time are fixed and closed: the chezmoi isolation test that fails every dotfiles push, the two deploy-guard arms that falsely refuse plugin syncs, the real-Obsidian e2e runners that fill athena's /tmp, and the most-reported bob-plugins perf flake. The lander triages what is left and proposes the next five-bead epic under the same rules, and the chain continues until no open task beads remain.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-r8.1](bob-cli-r8.1.md) | Poseidon chezmoi isolation test matches the Mac cargo config | ✓ closed | small | 2026-11-27 | 1 | 0 |
| [bob-cli-r8.2](bob-cli-r8.2.md) | Deploy guard runs the inclusion proof in both stamp arms | ✓ closed | medium | 2026-11-27 | 1 | 2 |
| [bob-cli-r8.3](bob-cli-r8.3.md) | Real-Obsidian e2e runners keep bounded failure scratch | ✓ closed | medium | 2026-11-27 | 1 | 1 |
| [bob-cli-r8.4](bob-cli-r8.4.md) | Stable task-wikilink cold-build 16 ms chunk measurement | ✓ closed | medium | 2026-11-27 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-r8: Task-bead burn-down 2: false deploy refusals, a red dotfiles CI, and leaking e2e scratch [in_progress]"]
    n1["bob-cli-r8.1: Poseidon chezmoi isolation test matches the Mac cargo config [closed]"]
    n2["bob-cli-r8.2: Deploy guard runs the inclusion proof in both stamp arms [closed]"]
    n3["bob-cli-r8.3: Real-Obsidian e2e runners keep bounded failure scratch [closed]"]
    n4["bob-cli-r8.4: Stable task-wikilink cold-build 16 ms chunk measurement [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-r8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.1/README.md) | [bob-cli-r8.1](bob-cli-r8.1.md) | 0 |
| [bbugyi200.athena.bob-cli-r8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.2/README.md) | [bob-cli-r8.2](bob-cli-r8.2.md) | 2 |
| [bbugyi200.athena.bob-cli-r8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r8.3.md) | [bob-cli-r8.3](bob-cli-r8.3.md) | 1 |
| [bbugyi200.athena.bob-cli-r8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.4/README.md) | [bob-cli-r8.4](bob-cli-r8.4.md) | 1 |
| [bbugyi200.athena.bob-cli-r8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.land/README.md) | [bob-cli-r8](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`dbdc7d2`](https://github.com/bobs-org/bob-cli/commit/dbdc7d24b28b2e72b2a3119155800738d4ad16ec) | feat(plugins): run deploy inclusion proof in both stamp arms | [bob-cli-r8.2](bob-cli-r8.2.md) | 2026-11-27 13:42:45 EST |
| bob-plugins | [`bob-plugins@ce4cb69`](https://github.com/bobs-org/bob-plugins/commit/ce4cb692999ad7db70015af5baaa11e85a079da6) | docs(deployment): sync guard rule covers clean stamps and dirty incoming | [bob-cli-r8.2](bob-cli-r8.2.md) | 2026-11-27 13:43:11 EST |
| bob-plugins | [`bob-plugins@6827a27`](https://github.com/bobs-org/bob-plugins/commit/6827a275650185b1341c781fe6c2cfc5fa153873) | fix(test): bound retained Obsidian e2e scratch | [bob-cli-r8.3](bob-cli-r8.3.md) | 2026-11-27 14:39:48 EST |
| bob-plugins | [`bob-plugins@4eb201e`](https://github.com/bobs-org/bob-plugins/commit/4eb201ecf730dac950b9737d65ae61eb1eb22315) | test(block-id-prompt): stabilize wikilink cold-chunk 16ms gate | [bob-cli-r8.4](bob-cli-r8.4.md) | 2026-11-27 15:13:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-r8.2][1] | epic decisions and scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.2/README.md

<!-- sase:referenced-by:end -->
