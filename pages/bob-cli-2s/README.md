# Bead: bob-cli-2s — Start lean: \`=~\<K\>\` drops queued Task Links as the next Pomodoro starts

[Bead Pages](../README.md) / bob-cli-2s

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.3f](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.3f.md) · **Assignee:** `bob-cli-2s.land`
**Created:** 2026-09-30 08:28:31 EDT
**Plan:** [202609/start\_drop\_queued\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/start_drop_queued_links.md)

## Description

`bob capture '=~2'` starts today's next Pomodoro without queued Task Link 2. It also works as `=<X>~<K>` and `=<X>#name~<K>`, in blank-line batches, and in same-line chains such as `=x =~2`. It is atomic and dry-runnable. Every start shows its numbered lineup, so you can see which number to drop. `capture-parse` and `capture-complete` support the new token, and Bob Mac Capture shows a numbered, drop-aware start card.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-2s.1](bob-cli-2s.1.md) | bob-cli: numbered start lineup and the drop engine | ✓ closed | medium | 2026-09-30 | 1 | 1 |
| [bob-cli-2s.2](bob-cli-2s.2.md) | bob-cli: \`=\[\<X\>\]\[#name\]~\<K\>\` grammar, editor support, and docs | ◐ in_progress | medium | 2026-09-30 | 1 | 1 |
| [bob-cli-2s.3](bob-cli-2s.3.md) | Bob Mac Capture: numbered, drop-aware start card | ◐ in_progress | medium | 2026-09-30 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-2s: Start lean: `=~&lt;K&gt;` drops queued Task Links as the next Pomodoro starts [in_progress]"]
    n1["bob-cli-2s.1: bob-cli: numbered start lineup and the drop engine [closed]"]
    n2["bob-cli-2s.2: bob-cli: `=[&lt;X&gt;][#name]~&lt;K&gt;` grammar, editor support, and docs [in_progress]"]
    n3["bob-cli-2s.3: Bob Mac Capture: numbered, drop-aware start card [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n2
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2s.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2s.1/README.md) | [bob-cli-2s.1](bob-cli-2s.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-2s.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2s.2/README.md) | [bob-cli-2s.2](bob-cli-2s.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-2s.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2s.3/README.md) | [bob-cli-2s.3](bob-cli-2s.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-2s.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2s.land/README.md) | [bob-cli-2s](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0b50af3`](https://github.com/bobs-org/bob-cli/commit/0b50af3cff1c86fc3bc995585b5896ae27a6edf6) | feat(capture): number whole-item start lineup and add plan\_start\_drop engine | [bob-cli-2s.1](bob-cli-2s.1.md) | 2026-09-30 09:06:14 EDT |
| bob-cli | [`1121e06`](https://github.com/bobs-org/bob-cli/commit/1121e06d77f6e8a18a771b4a1b172e36ff7bed83) | feat(capture): start-drop grammar for whole-item starts | [bob-cli-2s.2](bob-cli-2s.2.md) | 2026-09-30 09:44:41 EDT |
