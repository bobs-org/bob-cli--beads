# Bead: bob-cli-is — Close-outcome letter aliases (x → !, s → \*) in Bob Mac Capture

[Bead Pages](../README.md) / bob-cli-is

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3r.linker.w0.md) · **Assignee:** `bob-cli-is.land`
**Created:** 2026-11-08 11:42:40 EST
**Plan:** [202611/close\_outcome\_x\_s\_typing\_aliases.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/close_outcome_x_s_typing_aliases.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/close_outcome_x_s_typing_aliases.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/close_outcome_x_s_typing_aliases.md

<!-- sase:links:end -->

## Description

In the Bob Mac Capture editor, a plain lowercase `x` typed where a close selection accepts an outcome marker becomes `!`, and a plain lowercase `s` becomes `*`. Examples: `xx` → `x!`, `xs` → `x*`, `x1s` → `x1*`, `x=1=s` → `x=1=*`, and `@r:id=xx` → `@r:id=x!`. Bob's `capture-rewrite` alone decides where the alias fires. `bob capture`, `capture-parse`, paste, and CLI text keep the letters. Typing speed never changes the outcome: keys typed before Bob answers are held and replayed, and a fast Return never files the literal draft.

## Notes

[2026-11-08T23:10:56Z · bob-cli-iu.land] DISCOVERED ISSUE: bob-cli-iu land triage of bob-cli-iu.2 PROPOSED FOLLOW-UP notes #3/#5 independently compared macOS CI base run 42523594058 (2a39c2f, https://github.com/bobs-org/bob-mac-capture/actions/runs/42523594058) and dot snapshot run 42531359678 (https://github.com/bobs-org/bob-mac-capture/actions/runs/42531359678). Snapshot has 16 failing test methods: 14 CaptureSeparatorToggleTests (blank slash; close comma parity; close repeat/modifier/IME guards; close emoji; old-Bob warning; native undo/redo; picker-accepted-ID plus; caret-ID plus; plus undo; seal key; subsequent typing; hash/move/slash undo), CapturePanelModelTests.testPlusCommitsPartialCachedRouteCompletionAndOpensTaskPicker, CapturePanelAgendaLayoutTests.testClearWhilePreviewFinishingKeepsGeometryValid. All 16 fail in the base run (which has 19 failing methods); all 17 new dot tests pass. The phase note incorrectly calls all 16 separator tests and calls the sets identical. Source 2a39c2f adds the eager captureRewrite(xx) capability probe; legacy failures include observed rewrite count 2 vs 1 and unexpected nonempty logs. Your is.3 notes #2-4 already identify and repair that lifecycle/count/agenda cluster. Route this to the active causal epic; no new task and no +1 to h7/f3 for these different failures. Recheck against your repaired snapshot before closing.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-is.1](bob-cli-is.1.md) | Bob capture-rewrite close-outcome alias | ✓ closed | medium | 2026-11-08 | 1 | 1 |
| [bob-cli-is.2](bob-cli-is.2.md) | Mac type-ahead hold for meaning-changing rewrite aliases | ✓ closed | medium | 2026-11-08 | 1 | 1 |
| [bob-cli-is.3](bob-cli-is.3.md) | Mac forwards x/s to Bob's close-outcome alias | ◐ in_progress | medium | 2026-11-08 | 1 | 2 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-is: Close-outcome letter aliases (x → !, s → *) in Bob Mac Capture [in_progress]"]
    n1["bob-cli-is.1: Bob capture-rewrite close-outcome alias [closed]"]
    n2["bob-cli-is.2: Mac type-ahead hold for meaning-changing rewrite aliases [closed]"]
    n3["bob-cli-is.3: Mac forwards x/s to Bob's close-outcome alias [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n1 -.-> n3
    n2 -.-> n3
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-is.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-is.1/README.md) | [bob-cli-is.1](bob-cli-is.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-is.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-is.2.md) | [bob-cli-is.2](bob-cli-is.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-is.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-is.3.md) | [bob-cli-is.3](bob-cli-is.3.md) | 2 |
| [bbugyi200.apollo.bob-cli-is.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-is.land/README.md) | [bob-cli-is](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`23217c1`](https://github.com/bobs-org/bob-cli/commit/23217c1d78cafa2fe3a78ce5199653306169cca2) | feat(capture): alias x and s to close outcomes while typing | [bob-cli-is.1](bob-cli-is.1.md) | 2026-11-08 12:30:09 EST |
| bob-mac-capture | [`bob-mac-capture@03392a5`](https://github.com/bobs-org/bob-mac-capture/commit/03392a55eb87577ac8bd1b69c381949cc9e2024b) | feat(mac-capture): hold type-ahead keys during dash rewrite | [bob-cli-is.2](bob-cli-is.2.md) | 2026-11-08 15:16:44 EST |
| bob-mac-capture | [`bob-mac-capture@2a39c2f`](https://github.com/bobs-org/bob-mac-capture/commit/2a39c2ffac859a2d1594171ef835b8d6a7b9c6f3) | feat(mac-capture): alias x and s to close outcomes | [bob-cli-is.3](bob-cli-is.3.md) | 2026-11-08 16:07:25 EST |
| bob-mac-capture | [`bob-mac-capture@0f6753b`](https://github.com/bobs-org/bob-mac-capture/commit/0f6753bf429b9b1b86454fb8d95a17ce965a8f1c) | fix(mac-capture): verify close aliases and isolate probe and replay races | [bob-cli-is.3](bob-cli-is.3.md) | 2026-11-08 18:18:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-is.3][1] | epic scope for phase 3 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-is.3.md

<!-- sase:referenced-by:end -->
