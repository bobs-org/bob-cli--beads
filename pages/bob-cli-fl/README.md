# Bead: bob-cli-fl — Off-Clock Pomodoros, recorded and counted on their own clock

[Bead Pages](../README.md) / bob-cli-fl

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2z.linker.w0.md) · **Assignee:** `bob-cli-fl.land`
**Created:** 2026-11-01 21:46:35 EST
**Plan:** [202611/off\_clock\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_clock_pomodoros.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/off_clock_pomodoros.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/off_clock_pomodoros.md

<!-- sase:links:end -->

## Description

Sessions spent on #offclock tasks (lunch, the gym, school pickup) keep their time as [off:: Nm] Off-Clock Pomodoros instead of vanishing; a Pomodoro goes off the clock exactly when every Task Link it keeps targets an #offclock task; bob stats and the Stats dash gain a Worked · Off-clock · Total clock while every glanceable work signal stays Worked; ended off-clock events settle on their own; and one dashed visual language marks off-clock time everywhere.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-fl.1](bob-cli-fl.1.md) | bob-cli: \[off:: Nm\] ledger key, #offclock tag, and the off-clock vocabulary | ✓ closed | medium | 2026-11-01 | 1 | 1 |
| [bob-cli-fl.2](bob-cli-fl.2.md) | bob-cli: a session is off the clock iff every Task Link it keeps is #offclock | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fl.3](bob-cli-fl.3.md) | bob-cli: bob stats -k worked\|off-clock\|total and the clock JSON contract | ◐ in_progress | large | 2026-11-01 | 1 | 0 |
| [bob-cli-fl.4](bob-cli-fl.4.md) | bob-cli: bob task reconcile settles ended off-clock Event Tasks | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fl.5](bob-cli-fl.5.md) | bob-plugins: \[off::\] writers, Obsidian start/close rule, Event marks, home chips | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |
| [bob-cli-fl.6](bob-cli-fl.6.md) | bob-plugins: Worked · Off-clock · Total control in the Stats dash and the Day strip hint | ◐ in_progress | large | 2026-11-01 | 1 | 0 |
| [bob-cli-fl.7](bob-cli-fl.7.md) | bob-mac-capture: off-clock vocabulary, fallback decoding, and the title chip | ◐ in_progress | medium | 2026-11-01 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-fl: Off-Clock Pomodoros, recorded and counted on their own clock [in_progress]"]
    n1["bob-cli-fl.1: bob-cli: [off:: Nm] ledger key, #offclock tag, and the off-clock vocabulary [closed]"]
    n2["bob-cli-fl.2: bob-cli: a session is off the clock iff every Task Link it keeps is #offclock [in_progress]"]
    n3["bob-cli-fl.3: bob-cli: bob stats -k worked|off-clock|total and the clock JSON contract [in_progress]"]
    n4["bob-cli-fl.4: bob-cli: bob task reconcile settles ended off-clock Event Tasks [in_progress]"]
    n5["bob-cli-fl.5: bob-plugins: [off::] writers, Obsidian start/close rule, Event marks, home chips [in_progress]"]
    n6["bob-cli-fl.6: bob-plugins: Worked · Off-clock · Total control in the Stats dash and the Day strip hint [in_progress]"]
    n7["bob-cli-fl.7: bob-mac-capture: off-clock vocabulary, fallback decoding, and the title chip [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n2
    n1 -.-> n3
    n1 -.-> n4
    n2 -.-> n5
    n2 -.-> n7
    n3 -.-> n6
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fl.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fl.1.md) | [bob-cli-fl.1](bob-cli-fl.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-fl.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.2/README.md) | [bob-cli-fl.2](bob-cli-fl.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-fl.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.3/README.md) | [bob-cli-fl.3](bob-cli-fl.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-fl.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.4/README.md) | [bob-cli-fl.4](bob-cli-fl.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-fl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.5/README.md) | [bob-cli-fl.5](bob-cli-fl.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-fl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.6/README.md) | [bob-cli-fl.6](bob-cli-fl.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-fl.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.7/README.md) | [bob-cli-fl.7](bob-cli-fl.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-fl.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fl.land/README.md) | [bob-cli-fl](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8a9ec68`](https://github.com/bobs-org/bob-cli/commit/8a9ec685ed9c727a0d7338c9c7072b7e285c975e) | feat(off-clock): add off-clock Pomodoro ledger support | [bob-cli-fl.1](bob-cli-fl.1.md) | 2026-11-02 01:10:48 EST |
