# Bead: bob-cli-re — Task-bead burn-down 3: signal-safe CI, executable stubs, capture block identity, and merchant names

[Bead Pages](../README.md) / bob-cli-re

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-r8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-r8.land.md) · **Assignee:** `bob-cli-re.land`
**Created:** 2026-11-27 15:31:18 EST
**Plan:** [202611/task\_bead\_burndown\_3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_3.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/task_bead_burndown_3.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_bead_burndown_3.md

<!-- sase:links:end -->

## Description

Close five verified task beads by repairing the clipboard CI signal harness, executable-stub races, two capture block-reference panics, and spaced merchant order-code cleaning; then triage and continue the task-bead burn-down.

## Notes

[2026-11-27T20:38:01Z · bryanbugyi34@gmail.com] I think three rounds are enough for now. The Lander agent should not create a new epic unless issues were caused by this work or one of the previous rounds.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-re.1](bob-cli-re.1.md) | Make the clipboard SIGINT test independent of inherited signal disposition | ✓ closed | small | 2026-11-27 | 1 | 0 |
| [bob-cli-re.2](bob-cli-re.2.md) | Adopt fork-safe writers for the remaining executable test stubs | ✓ closed | medium | 2026-11-27 | 1 | 1 |
| [bob-cli-re.3](bob-cli-re.3.md) | Preserve task block identity when canceling an ID-less successor | ◐ in_progress | medium | 2026-11-27 | 1 | 0 |
| [bob-cli-re.4](bob-cli-re.4.md) | Preserve Pomodoro block references around an existing timed entry | ◐ in_progress | medium | 2026-11-27 | 1 | 0 |
| [bob-cli-re.5](bob-cli-re.5.md) | Clean spaced Amazon order codes without erasing sub-merchants | ◐ in_progress | small | 2026-11-27 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-re: Task-bead burn-down 3: signal-safe CI, executable stubs, capture block identity, and merchant names [in_progress]"]
    n1["bob-cli-re.1: Make the clipboard SIGINT test independent of inherited signal disposition [closed]"]
    n2["bob-cli-re.2: Adopt fork-safe writers for the remaining executable test stubs [closed]"]
    n3["bob-cli-re.3: Preserve task block identity when canceling an ID-less successor [in_progress]"]
    n4["bob-cli-re.4: Preserve Pomodoro block references around an existing timed entry [in_progress]"]
    n5["bob-cli-re.5: Clean spaced Amazon order codes without erasing sub-merchants [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
    n4 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-re.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-re.1.md) | [bob-cli-re.1](bob-cli-re.1.md) | 0 |
| [bbugyi200.athena.bob-cli-re.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.2/README.md) | [bob-cli-re.2](bob-cli-re.2.md) | 1 |
| [bbugyi200.athena.bob-cli-re.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.3/README.md) | [bob-cli-re.3](bob-cli-re.3.md) | 0 |
| [bbugyi200.athena.bob-cli-re.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.4/README.md) | [bob-cli-re.4](bob-cli-re.4.md) | 0 |
| [bbugyi200.athena.bob-cli-re.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.5/README.md) | [bob-cli-re.5](bob-cli-re.5.md) | 0 |
| [bbugyi200.athena.bob-cli-re.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-re.land/README.md) | [bob-cli-re](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`69f8aae`](https://github.com/bobs-org/bob-cli/commit/69f8aae63cdf25cf926461f0d96a1156de1997e5) | fix(tests): eliminate ETXTBSY races via child-cp executable stubs | [bob-cli-re.2](bob-cli-re.2.md) | 2026-11-27 16:56:03 EST |
