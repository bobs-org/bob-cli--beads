# Bead: bob-cli-rb — Capture type leads — \`#f\` ⇥ types \`#fix Fix ▌\`

[Bead Pages](../README.md) / bob-cli-rb

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hh.md) · **Assignee:** `bob-cli-rb.land`
**Created:** 2026-11-27 15:03:20 EST
**Plan:** [202611/capture\_type\_leads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_type_leads.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_type_leads.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_type_leads.md

<!-- sase:links:end -->

## Description

Accepting a configured task type from the Capture panel's `#` menu at the start of an empty new-task item also types that type's lead word (`#f` ⇥ → `#fix Fix ▌`). The menu previews the lead before you accept, one Backspace or ⌘Z removes it, and accept-and-capture never mints a one-word task. The five leads (BUILD, FIX, PLAN, READ, WRITE) come from `capture.type_leads` in the chezmoi-managed bob config.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-rb.1](bob-cli-rb.1.md) | bob-cli capture.type\_leads loader, bob types surfacing, rename guard | ✓ closed | medium | 2026-11-27 | 1 | 1 |
| [bob-cli-rb.2](bob-cli-rb.2.md) | bob-cli task\_type candidates carry an optional lead | ◐ in_progress | medium | 2026-11-27 | 1 | 0 |
| [bob-cli-rb.3](bob-cli-rb.3.md) | Mac decodes the lead and previews it in the Task type menu | ◐ in_progress | small | 2026-11-27 | 1 | 0 |
| [bob-cli-rb.4](bob-cli-rb.4.md) | Mac inserts the lead undoably, peels it with one Backspace, skips it on ⌘↩ | ◐ in_progress | medium | 2026-11-27 | 1 | 0 |
| [bob-cli-rb.5](bob-cli-rb.5.md) | Enable the five leads in chezmoi and verify end to end | ◐ in_progress | small | 2026-11-27 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-rb: Capture type leads — `#f` ⇥ types `#fix Fix ▌` [in_progress]"]
    n1["bob-cli-rb.1: bob-cli capture.type_leads loader, bob types surfacing, rename guard [closed]"]
    n2["bob-cli-rb.2: bob-cli task_type candidates carry an optional lead [in_progress]"]
    n3["bob-cli-rb.3: Mac decodes the lead and previews it in the Task type menu [in_progress]"]
    n4["bob-cli-rb.4: Mac inserts the lead undoably, peels it with one Backspace, skips it on ⌘↩ [in_progress]"]
    n5["bob-cli-rb.5: Enable the five leads in chezmoi and verify end to end [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n2
    n1 -.-> n5
    n2 -.-> n3
    n3 -.-> n4
    n4 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rb.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rb.1.md) | [bob-cli-rb.1](bob-cli-rb.1.md) | 1 |
| [bbugyi200.athena.bob-cli-rb.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rb.2/README.md) | [bob-cli-rb.2](bob-cli-rb.2.md) | 0 |
| [bbugyi200.athena.bob-cli-rb.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rb.3/README.md) | [bob-cli-rb.3](bob-cli-rb.3.md) | 0 |
| [bbugyi200.athena.bob-cli-rb.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rb.4/README.md) | [bob-cli-rb.4](bob-cli-rb.4.md) | 0 |
| [bbugyi200.athena.bob-cli-rb.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rb.5/README.md) | [bob-cli-rb.5](bob-cli-rb.5.md) | 0 |
| [bbugyi200.athena.bob-cli-rb.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rb.land/README.md) | [bob-cli-rb](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`421de94`](https://github.com/bobs-org/bob-cli/commit/421de94dc381f1947e24154d181ef44b6829c86c) | feat(types): add configurable capture type leads | [bob-cli-rb.1](bob-cli-rb.1.md) | 2026-11-27 15:51:41 EST |
