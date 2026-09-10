# Bead: bob-cli-1z — Capture-driven Obsidian task status toggle (@route+block-id with no other text)

[Bead Pages](../README.md) / bob-cli-1z

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0ir](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.0ir.md) · **Assignee:** `bob-cli-1z.land`
**Created:** 2026-09-10 13:19:08 EDT · **Closed:** 2026-09-10 15:55:59 EDT
**Plan:** [202609/capture\_task\_toggle.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_task_toggle.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202609/capture_task_toggle.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202609/capture_task_toggle.md

<!-- sase:links:end -->

## Description

Submitting a capture draft that is exactly `@route+block-id` (optionally `@route+block-id#pomodoro`) toggles that existing Obsidian task between Ready `[ ]` and Next `[*]` and adds or removes its Pomodoro task link, matching the Obsidian `<ctrl+shift+enter>` keymap's semantics. The `@route+block-id` completion and Add block ID prompt behave exactly as they already do for sub-bullet capture, and Bob Mac Capture makes the mode, the target task, and the exact before/after change obvious before the user commits it.

## Notes

[2026-09-10T19:55:59Z · bob-cli-1z.land] Verified all 6 phases complete: read every child note and confirmed the work in the actual commits — bob-cli fda8627 (grammar), ce9d984 (planners, 27 unit tests), 7d868fb (capture wiring + 5 CLI integration tests), be6eed6 (README/docs), bob-mac-capture 9cce339 (CaptureCore decode + CaptureTogglePresentation + panel wiring) and b979528 (preview/highlighting/README). Re-ran just all on the clean tree at be6eed6: ALL CHECKS PASSED (fmt, clippy, full test suite). macOS 26 CI green on both bob-mac-capture commits; both repos clean and in sync with origin. Integration: no non-epic commits landed in either repo since the epic started (bob-cli 86e6394 and bob-mac-capture cf73955 both predate it), so nothing needed updating. epic-symbols: no entries; no just symvision recipe exists. Follow-ups: bob-cli-1z.6's Linux BobProcessClient test failures corroborated as +1 on existing duplicate bob-cli-1u; bob-cli-1z.5's spoken/notification-copy UX pass filed as task bob-cli-20 (feature, small, ready) because it needs the running macOS app and owner judgment, not a defect in this epic; newly discovered artifact-link event-store corruption (blocks all sase artifact link add writes) filed as task bob-cli-21 (bug, large, ready), and bob-cli-20's intended related-link to its proposing bead recorded as a bead note instead.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-1z.1](bob-cli-1z.1.md) | Capture grammar and completion for the task-toggle item | ✓ closed | medium | 2026-09-10 | 1 | 1 |
| [bob-cli-1z.2](bob-cli-1z.2.md) | Pure toggle planners for the route note and the daily ledger | ✓ closed | medium | 2026-09-10 | 1 | 1 |
| [bob-cli-1z.3](bob-cli-1z.3.md) | Wire the toggle into bob capture, its JSON contract, and its human output | ✓ closed | medium | 2026-09-10 | 1 | 1 |
| [bob-cli-1z.4](bob-cli-1z.4.md) | bob-cli documentation for the task-toggle marker | ✓ closed | small | 2026-09-10 | 1 | 1 |
| [bob-cli-1z.5](bob-cli-1z.5.md) | CaptureCore models, presentation model, and panel wiring | ✓ closed | medium | 2026-09-10 | 1 | 1 |
| [bob-cli-1z.6](bob-cli-1z.6.md) | Bob Mac Capture toggle preview, highlighting, and documentation | ✓ closed | medium | 2026-09-10 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-1z: Capture-driven Obsidian task status toggle (@route+block-id with no other text) [closed]"]
    n1["bob-cli-1z.1: Capture grammar and completion for the task-toggle item [closed]"]
    n2["bob-cli-1z.2: Pure toggle planners for the route note and the daily ledger [closed]"]
    n3["bob-cli-1z.3: Wire the toggle into bob capture, its JSON contract, and its human output [closed]"]
    n4["bob-cli-1z.4: bob-cli documentation for the task-toggle marker [closed]"]
    n5["bob-cli-1z.5: CaptureCore models, presentation model, and panel wiring [closed]"]
    n6["bob-cli-1z.6: Bob Mac Capture toggle preview, highlighting, and documentation [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n3
    n2 -.-> n3
    n3 -.-> n4
    n3 -.-> n5
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-1z.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.1/README.md) | [bob-cli-1z.1](bob-cli-1z.1.md) | 1 |
| [bbugyi200.athena.bob-cli-1z.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.2/README.md) | [bob-cli-1z.2](bob-cli-1z.2.md) | 1 |
| [bbugyi200.athena.bob-cli-1z.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.3/README.md) | [bob-cli-1z.3](bob-cli-1z.3.md) | 1 |
| [bbugyi200.athena.bob-cli-1z.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.4/README.md) | [bob-cli-1z.4](bob-cli-1z.4.md) | 1 |
| [bbugyi200.athena.bob-cli-1z.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.5/README.md) | [bob-cli-1z.5](bob-cli-1z.5.md) | 1 |
| [bbugyi200.athena.bob-cli-1z.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.6/README.md) | [bob-cli-1z.6](bob-cli-1z.6.md) | 1 |
| [bbugyi200.athena.bob-cli-1z.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-1z.land/README.md) | [bob-cli-1z](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fda8627`](https://github.com/bobs-org/bob-cli/commit/fda8627d7181e20457ea5e299e2033d5c0a8744d) | feat(capture): add task\_toggle capture grammar phase | [bob-cli-1z.1](bob-cli-1z.1.md) | 2026-09-10 14:10:12 EDT |
| bob-cli | [`ce9d984`](https://github.com/bobs-org/bob-cli/commit/ce9d98419a797eb5d03cfaa293667352b1ac6e70) | feat(capture-task-toggle): add pure route-note and Pomodoro-ledger toggle planners | [bob-cli-1z.2](bob-cli-1z.2.md) | 2026-09-10 14:47:02 EDT |
| bob-cli | [`7d868fb`](https://github.com/bobs-org/bob-cli/commit/7d868fbc55ee5180beda21d96bb36d72154afca3) | feat(capture): wire task toggle execution | [bob-cli-1z.3](bob-cli-1z.3.md) | 2026-09-10 15:05:31 EDT |
| bob-cli | [`be6eed6`](https://github.com/bobs-org/bob-cli/commit/be6eed6a18d19aca920684a7d9abfac7e44b8606) | docs(capture): document task toggle marker | [bob-cli-1z.4](bob-cli-1z.4.md) | 2026-09-10 15:13:58 EDT |
| bob-mac-capture | [`bob-mac-capture@9cce339`](https://github.com/bobs-org/bob-mac-capture/commit/9cce339ab8608eada48447bca5d90f20efeeac5d) | feat(capture-core): decode task\_toggle fields, add CaptureTogglePresentation, wire panel/notification | [bob-cli-1z.5](bob-cli-1z.5.md) | 2026-09-10 15:31:24 EDT |
| bob-mac-capture | [`bob-mac-capture@b979528`](https://github.com/bobs-org/bob-mac-capture/commit/b979528f2764d211ecd5c58c478ebb2110f6ed5e) | feat(capture): render task toggle previews | [bob-cli-1z.6](bob-cli-1z.6.md) | 2026-09-10 15:44:27 EDT |
| bob-cli--plans | [`bob-cli--plans@0915418`](https://github.com/bobs-org/bob-cli--plans/commit/0915418b375d5590ac4954abf973f00e94be5c15) | docs(plans): mark capture\_task\_toggle epic plan done after landing bob-cli-1z | [bob-cli-1z](README.md) | 2026-09-10 15:56:41 EDT |
