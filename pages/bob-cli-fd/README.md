# Bead: bob-cli-fd — Timestamped Work Log entries

[Bead Pages](../README.md) / bob-cli-fd

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c3.md) · **Assignee:** `bob-cli-fd.land`
**Created:** 2026-11-01 15:12:25 EST
**Plan:** [202611/work\_log\_timestamps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/work_log_timestamps.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/work_log_timestamps.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/work_log_timestamps.md

<!-- sase:links:end -->

## Description

Every new Work Log entry, from any of Bob's four writers, opens with one italic `*YYYY-MM-DD HH:MM*` stamp of the minute it was written. Older date-only entries stay valid and untouched, and every reader handles both forms the same way.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-fd.1](bob-cli-fd.1.md) | Bob Mac Capture strips both stamp forms | ✓ closed | small | 2026-11-01 | 1 | 1 |
| [bob-cli-fd.2](bob-cli-fd.2.md) | Navigation hotkeys read and write stamps | ○ open | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fd.3](bob-cli-fd.3.md) | bob capture close stamps entries and owns the grammar docs | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fd.4](bob-cli-fd.4.md) | Unlink prompt and Pomodoro checkbox close write stamps | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-fd: Timestamped Work Log entries [in_progress]"]
    n1["bob-cli-fd.1: Bob Mac Capture strips both stamp forms [closed]"]
    n2["bob-cli-fd.2: Navigation hotkeys read and write stamps [open]"]
    n3["bob-cli-fd.3: bob capture close stamps entries and owns the grammar docs [in_progress]"]
    n4["bob-cli-fd.4: Unlink prompt and Pomodoro checkbox close write stamps [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n1 -.-> n3
    n2 -.-> n3
    n2 -.-> n4
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fd.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fd.1/README.md) | [bob-cli-fd.1](bob-cli-fd.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-fd.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fd.2/README.md) | [bob-cli-fd.2](bob-cli-fd.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-fd.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fd.3/README.md) | [bob-cli-fd.3](bob-cli-fd.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-fd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fd.4/README.md) | [bob-cli-fd.4](bob-cli-fd.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-fd.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fd.land/README.md) | [bob-cli-fd](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@01c753b`](https://github.com/bobs-org/bob-mac-capture/commit/01c753b0e6e045a0cc69b3d3f51302b8423b7e55) | feat(mac-capture): strip stamped Work Log dates on the close card | [bob-cli-fd.1](bob-cli-fd.1.md) | 2026-11-01 15:43:29 EST |
