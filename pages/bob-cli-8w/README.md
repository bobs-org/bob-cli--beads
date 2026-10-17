# Bead: bob-cli-8w — Bob Mac Capture Control-Return: capture, then land on it in Obsidian

[Bead Pages](../README.md) / bob-cli-8w

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.8q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.8q.md) · **Assignee:** `bob-cli-8w.land`
**Created:** 2026-10-17 15:54:14 EDT
**Plan:** [202610/ctrl\_enter\_capture\_and\_open.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_enter_capture_and_open.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/ctrl_enter_capture_and_open.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ctrl_enter_capture_and_open.md

<!-- sase:links:end -->

## Description

In Bob Mac Capture, Control-Return captures the draft, then brings Obsidian forward with every note the capture changed open in its own tab. The caret sits on the exact line that changed, which gets a short highlight. bob decides what to open, so the app stays a thin client. One Obsidian URL carries the whole list, so tabs never replace each other. The panel shows beforehand what Control-Return will open.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-8w.1](bob-cli-8w.1.md) | bob reports which notes a capture should open | ◐ in_progress | medium | 2026-10-17 | 1 | 0 |
| [bob-cli-8w.2](bob-cli-8w.2.md) | Obsidian handler that opens several notes and lands on each | ✓ closed | medium | 2026-10-17 | 1 | 1 |
| [bob-cli-8w.3](bob-cli-8w.3.md) | Portable open plan and URL builder in CaptureCore | ◐ in_progress | small | 2026-10-17 | 1 | 0 |
| [bob-cli-8w.4](bob-cli-8w.4.md) | Control-Return gesture and the open pipeline | ◐ in_progress | medium | 2026-10-17 | 1 | 0 |
| [bob-cli-8w.5](bob-cli-8w.5.md) | Footer hint, hold-to-reveal destinations, and picker hints | ◐ in_progress | medium | 2026-10-17 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-8w: Bob Mac Capture Control-Return: capture, then land on it in Obsidian [in_progress]"]
    n1["bob-cli-8w.1: bob reports which notes a capture should open [in_progress]"]
    n2["bob-cli-8w.2: Obsidian handler that opens several notes and lands on each [closed]"]
    n3["bob-cli-8w.3: Portable open plan and URL builder in CaptureCore [in_progress]"]
    n4["bob-cli-8w.4: Control-Return gesture and the open pipeline [in_progress]"]
    n5["bob-cli-8w.5: Footer hint, hold-to-reveal destinations, and picker hints [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n1 -.-> n3
    n2 -.-> n3
    n3 -.-> n4
    n4 -.-> n5
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8w.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8w.1/README.md) | [bob-cli-8w.1](bob-cli-8w.1.md) | 0 |
| [bbugyi200.apollo.bob-cli-8w.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-8w.2.md) | [bob-cli-8w.2](bob-cli-8w.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-8w.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8w.3/README.md) | [bob-cli-8w.3](bob-cli-8w.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-8w.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8w.4/README.md) | [bob-cli-8w.4](bob-cli-8w.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-8w.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8w.5/README.md) | [bob-cli-8w.5](bob-cli-8w.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-8w.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8w.land/README.md) | [bob-cli-8w](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3e359a6`](https://github.com/bobs-org/bob-plugins/commit/3e359a6d92d11194c507cd1e56f4efb7aad31cd2) | feat(bob-navigation-hotkeys): add open notes URI handler | [bob-cli-8w.2](bob-cli-8w.2.md) | 2026-10-17 16:16:15 EDT |
