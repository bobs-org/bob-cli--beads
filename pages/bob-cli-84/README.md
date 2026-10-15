# Bead: bob-cli-84 — Bob Refs Tabs filter — a Highlights tab switcher

[Bead Pages](../README.md) / bob-cli-84

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.7w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7w.md) · **Assignee:** `bob-cli-84.land`
**Created:** 2026-10-15 17:50:48 EDT
**Plan:** [202610/highlights\_tabs\_switcher.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/highlights_tabs_switcher.md)

## Description

In Bob Mac Capture's Bob Refs panel, ⇧⌘O pressed while Highlights is frontmost (or ⌘T inside the panel) shows a "Tabs" filter. It lists every document open in Highlights, matched to its reference note where one exists, with the current tab first and the previous tab pre-selected. ↵ switches to that existing tab without touching the vault or the open log. Bob Mac Capture installs with a stable signing identity, so the Accessibility grant the feature needs survives every `just install`.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-84.1](bob-cli-84.1.md) | Stable signing identity and Accessibility status | ✓ closed | small | 2026-10-15 | 1 | 1 |
| [bob-cli-84.2](bob-cli-84.2.md) | RefsCore tab snapshot, matcher, ordering, and session | ◐ in_progress | medium | 2026-10-15 | 1 | 0 |
| [bob-cli-84.3](bob-cli-84.3.md) | Highlights-only Accessibility reader | ◐ in_progress | medium | 2026-10-15 | 1 | 0 |
| [bob-cli-84.4](bob-cli-84.4.md) | Panel model Tabs filter, switching, and states | ◐ in_progress | medium | 2026-10-15 | 1 | 0 |
| [bob-cli-84.5](bob-cli-84.5.md) | Tabs rendering, keys, and design tests | ◐ in_progress | medium | 2026-10-15 | 1 | 0 |
| [bob-cli-84.6](bob-cli-84.6.md) | ⇧⌘O entry point, live wiring, settings, and docs | ◐ in_progress | medium | 2026-10-15 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-84: Bob Refs Tabs filter — a Highlights tab switcher [in_progress]"]
    n1["bob-cli-84.1: Stable signing identity and Accessibility status [closed]"]
    n2["bob-cli-84.2: RefsCore tab snapshot, matcher, ordering, and session [in_progress]"]
    n3["bob-cli-84.3: Highlights-only Accessibility reader [in_progress]"]
    n4["bob-cli-84.4: Panel model Tabs filter, switching, and states [in_progress]"]
    n5["bob-cli-84.5: Tabs rendering, keys, and design tests [in_progress]"]
    n6["bob-cli-84.6: ⇧⌘O entry point, live wiring, settings, and docs [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n3
    n1 -.-> n6
    n2 -.-> n3
    n2 -.-> n4
    n3 -.-> n6
    n4 -.-> n5
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-84.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.1/README.md) | [bob-cli-84.1](bob-cli-84.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-84.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-84.2.md) | [bob-cli-84.2](bob-cli-84.2.md) | 0 |
| [bbugyi200.apollo.bob-cli-84.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.3/README.md) | [bob-cli-84.3](bob-cli-84.3.md) | 0 |
| [bbugyi200.apollo.bob-cli-84.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.4/README.md) | [bob-cli-84.4](bob-cli-84.4.md) | 0 |
| [bbugyi200.apollo.bob-cli-84.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.5/README.md) | [bob-cli-84.5](bob-cli-84.5.md) | 0 |
| [bbugyi200.apollo.bob-cli-84.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.6/README.md) | [bob-cli-84.6](bob-cli-84.6.md) | 0 |
| [bbugyi200.apollo.bob-cli-84.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-84.land/README.md) | [bob-cli-84](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1cd958e`](https://github.com/bobs-org/bob-mac-capture/commit/1cd958e4c96a1f75f6b14f29f72b3c4833a6c22e) | feat(signing): sign with stable self-signed identity with ad-hoc fallback | [bob-cli-84.1](bob-cli-84.1.md) | 2026-10-15 18:06:11 EDT |
