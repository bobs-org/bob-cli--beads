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

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_2.md

<!-- sase:links:end -->

## Description

The five open task beads that now cost agents the most time are fixed and closed: the chezmoi isolation test that fails every dotfiles push, the two deploy-guard arms that falsely refuse plugin syncs, the real-Obsidian e2e runners that fill athena's /tmp, and the most-reported bob-plugins perf flake. The lander triages what is left and proposes the next five-bead epic under the same rules, and the chain continues until no open task beads remain.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-r8.1](bob-cli-r8.1.md) | Poseidon chezmoi isolation test matches the Mac cargo config | ✓ closed | small | 2026-11-27 | 1 | 1 |
| [bob-cli-r8.2](bob-cli-r8.2.md) | Deploy guard runs the inclusion proof in both stamp arms | ◐ in_progress | medium | 2026-11-27 | 1 | 0 |
| [bob-cli-r8.3](bob-cli-r8.3.md) | Real-Obsidian e2e runners keep bounded failure scratch | ◐ in_progress | medium | 2026-11-27 | 1 | 0 |
| [bob-cli-r8.4](bob-cli-r8.4.md) | Stable task-wikilink cold-build 16 ms chunk measurement | ◐ in_progress | medium | 2026-11-27 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-r8: Task-bead burn-down 2: false deploy refusals, a red dotfiles CI, and leaking e2e scratch [in_progress]"]
    n1["bob-cli-r8.1: Poseidon chezmoi isolation test matches the Mac cargo config [closed]"]
    n2["bob-cli-r8.2: Deploy guard runs the inclusion proof in both stamp arms [in_progress]"]
    n3["bob-cli-r8.3: Real-Obsidian e2e runners keep bounded failure scratch [in_progress]"]
    n4["bob-cli-r8.4: Stable task-wikilink cold-build 16 ms chunk measurement [in_progress]"]
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
| [bbugyi200.athena.bob-cli-r8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.1/README.md) | [bob-cli-r8.1](bob-cli-r8.1.md) | 1 |
| [bbugyi200.athena.bob-cli-r8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.2/README.md) | [bob-cli-r8.2](bob-cli-r8.2.md) | 0 |
| [bbugyi200.athena.bob-cli-r8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.3/README.md) | [bob-cli-r8.3](bob-cli-r8.3.md) | 0 |
| [bbugyi200.athena.bob-cli-r8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.4/README.md) | [bob-cli-r8.4](bob-cli-r8.4.md) | 0 |
| [bbugyi200.athena.bob-cli-r8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-r8.land/README.md) | [bob-cli-r8](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@662569a`](https://github.com/bbugyi200/dotfiles/commit/662569a34eb9209baa03e4cc50d32356ee2c7a08) | test(chezmoi): align poseidon isolation assertions | [bob-cli-r8.1](bob-cli-r8.1.md) | 2026-11-27 13:11:07 EST |
