# Bead: bob-cli-k7 — Keep-moving marks — show \`⏭ N\` after a Task Link whose close will keep its project moving

[Bead Pages](../README.md) / bob-cli-k7

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1b8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1b8.md) · **Assignee:** `bob-cli-k7.land`
**Created:** 2026-11-11 07:57:57 EST
**Plan:** [202611/keep\_moving\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/keep_moving_link_marks.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/keep_moving_link_marks.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/keep_moving_link_marks.md

<!-- sase:links:end -->

## Description

In today's ledger, a quiet `⏭ N` mark after a Task Link forecasts the `Keep ‹N› moving` successor picker that closing that task will really open: N is exactly the number of rows that group will offer, it appears only on the link whose close triggers the group, and it is silent whenever that cannot be proven. Keep-moving first stops skipping standalone top-level projects (only umbrella projects are skipped), so the screenshot's `job_email_recruiters` link shows `⏭ 4` and Ctrl+Enter then offers those same four tasks.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-k7.1](bob-cli-k7.1.md) | Umbrella rule in the contract, memory, and Rust | ✓ closed | medium | 2026-11-11 | 1 | 1 |
| [bob-cli-k7.2](bob-cli-k7.2.md) | Umbrella rule and \`\_generated/\` fix in the Obsidian cycler | ◐ in_progress | small | 2026-11-11 | 1 | 0 |
| [bob-cli-k7.3](bob-cli-k7.3.md) | Keep-moving mark display contract | ◐ in_progress | small | 2026-11-11 | 1 | 0 |
| [bob-cli-k7.4](bob-cli-k7.4.md) | Pure keep-moving mark core and cross-plugin parity | ◐ in_progress | medium | 2026-11-11 | 1 | 0 |
| [bob-cli-k7.5](bob-cli-k7.5.md) | Live Preview, Reading view, look, and liveness | ◐ in_progress | medium | 2026-11-11 | 1 | 0 |
| [bob-cli-k7.6](bob-cli-k7.6.md) | Real-vault audit against capture and the picker | ◐ in_progress | small | 2026-11-11 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-k7: Keep-moving marks — show `⏭ N` after a Task Link whose close will keep its project moving [in_progress]"]
    n1["bob-cli-k7.1: Umbrella rule in the contract, memory, and Rust [closed]"]
    n2["bob-cli-k7.2: Umbrella rule and `_generated/` fix in the Obsidian cycler [in_progress]"]
    n3["bob-cli-k7.3: Keep-moving mark display contract [in_progress]"]
    n4["bob-cli-k7.4: Pure keep-moving mark core and cross-plugin parity [in_progress]"]
    n5["bob-cli-k7.5: Live Preview, Reading view, look, and liveness [in_progress]"]
    n6["bob-cli-k7.6: Real-vault audit against capture and the picker [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n2
    n1 -.-> n3
    n2 -.-> n4
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k7.1.md) | [bob-cli-k7.1](bob-cli-k7.1.md) | 1 |
| [bbugyi200.athena.bob-cli-k7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k7.2/README.md) | [bob-cli-k7.2](bob-cli-k7.2.md) | 0 |
| [bbugyi200.athena.bob-cli-k7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k7.3/README.md) | [bob-cli-k7.3](bob-cli-k7.3.md) | 0 |
| [bbugyi200.athena.bob-cli-k7.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k7.4/README.md) | [bob-cli-k7.4](bob-cli-k7.4.md) | 0 |
| [bbugyi200.athena.bob-cli-k7.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k7.5/README.md) | [bob-cli-k7.5](bob-cli-k7.5.md) | 0 |
| [bbugyi200.athena.bob-cli-k7.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k7.6/README.md) | [bob-cli-k7.6](bob-cli-k7.6.md) | 0 |
| [bbugyi200.athena.bob-cli-k7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k7.land/README.md) | [bob-cli-k7](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b2c3697`](https://github.com/bobs-org/bob-cli/commit/b2c3697e8c57c5c2091b1df207d9bed3b38382f3) | feat(keep-moving): skip only umbrella projects, not every root | [bob-cli-k7.1](bob-cli-k7.1.md) | 2026-11-11 08:44:49 EST |
