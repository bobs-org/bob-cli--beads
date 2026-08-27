# Bead: bob-cli-1n — Make the bobs-org/bob GitHub repo the only Bob vault sync channel

[Bead Pages](../README.md) / bob-cli-1n

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ez](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ez.md) · **Assignee:** `bob-cli-1n.land`
**Created:** 2026-08-27 12:48:58 EDT
**Plan:** [202608/vault\_git\_sync.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/vault_git_sync.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202608/vault_git_sync.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202608/vault_git_sync.md

<!-- sase:links:end -->

## Description

The Bob Obsidian vault stays converged between athena and the MacBook through git alone, driven by a new `bob vault-sync` command that pulls, merges, commits, and pushes unattended without ever leaving conflict markers or a halted merge; Obsidian Sync is switched off on both devices; and large PDF trees that must not enter the repo reach the MacBook over an explicit rsync bridge invoked by a new configurable `bob highlights` pre-scan command.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-1n.1](bob-cli-1n.1.md) | Converge both vaults and fix what the first \`git add -A\` would sweep in | ◐ in_progress | medium | 2026-08-27 | 1 | 0 |
| [bob-cli-1n.2](bob-cli-1n.2.md) | Implement \`bob vault-sync\` and its conflict-copy policy | ✓ closed | medium | 2026-08-27 | 1 | 1 |
| [bob-cli-1n.3](bob-cli-1n.3.md) | Retire \`bulk-git-commit\` and rewire \`bob nightly\` | ◐ in_progress | small | 2026-08-27 | 1 | 0 |
| [bob-cli-1n.4](bob-cli-1n.4.md) | Add a configurable pre-scan command to \`bob highlights\` | ✓ closed | medium | 2026-08-27 | 1 | 1 |
| [bob-cli-1n.5](bob-cli-1n.5.md) | Provision credentials, triggers, and the MacBook git clone | ◐ in_progress | medium | 2026-08-27 | 1 | 0 |
| [bob-cli-1n.6](bob-cli-1n.6.md) | Prove the acceptance matrix end to end, then cut over | ◐ in_progress | medium | 2026-08-27 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-1n: Make the bobs-org/bob GitHub repo the only Bob vault sync channel [in_progress]"]
    n1["bob-cli-1n.1: Converge both vaults and fix what the first `git add -A` would sweep in [in_progress]"]
    n2["bob-cli-1n.2: Implement `bob vault-sync` and its conflict-copy policy [closed]"]
    n3["bob-cli-1n.3: Retire `bulk-git-commit` and rewire `bob nightly` [in_progress]"]
    n4["bob-cli-1n.4: Add a configurable pre-scan command to `bob highlights` [closed]"]
    n5["bob-cli-1n.5: Provision credentials, triggers, and the MacBook git clone [in_progress]"]
    n6["bob-cli-1n.6: Prove the acceptance matrix end to end, then cut over [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n5
    n2 -.-> n3
    n3 -.-> n5
    n4 -.-> n5
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1n.1](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.bob-cli-1n.1.md) | [bob-cli-1n.1](bob-cli-1n.1.md) | 0 |
| [bbugyi200.athena.bob-cli-1n.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.2/README.md) | [bob-cli-1n.2](bob-cli-1n.2.md) | 1 |
| [bbugyi200.athena.bob-cli-1n.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.3/README.md) | [bob-cli-1n.3](bob-cli-1n.3.md) | 0 |
| [bbugyi200.athena.bob-cli-1n.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.4/README.md) | [bob-cli-1n.4](bob-cli-1n.4.md) | 1 |
| [bbugyi200.athena.bob-cli-1n.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.5/README.md) | [bob-cli-1n.5](bob-cli-1n.5.md) | 0 |
| [bbugyi200.athena.bob-cli-1n.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.6/README.md) | [bob-cli-1n.6](bob-cli-1n.6.md) | 0 |
| [bbugyi200.athena.bob-cli-1n.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1n.land/README.md) | [bob-cli-1n](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`86bff41`](https://github.com/bobs-org/bob-cli/commit/86bff4105b7ac7de2d8b60d4b2241ff3204db9b9) | feat(highlights): add scan pre-scan hook | [bob-cli-1n.4](bob-cli-1n.4.md) | 2026-08-27 13:04:01 EDT |
| bob-cli | [`eee290a`](https://github.com/bobs-org/bob-cli/commit/eee290ab546820b615de952f9c086f3935cb1f5c) | feat(vault-sync): add git reconcile command | [bob-cli-1n.2](bob-cli-1n.2.md) | 2026-08-27 13:14:12 EDT |
