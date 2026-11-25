# Bead: bob-cli-q7 — @route^id Go To: open a task by its exact address from Bob Capture

[Bead Pages](../README.md) / bob-cli-q7

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1g6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1g6.md) · **Assignee:** `bob-cli-q7.land`
**Created:** 2026-11-25 15:25:24 EST
**Plan:** [202611/caret\_address\_goto\_capture.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/caret_address_goto_capture.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/caret_address_goto_capture.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/caret_address_goto_capture.md

<!-- sase:links:end -->

## Description

A capture draft that is exactly one bare `@route^block-id` token resolves read-only to that block's line and, on Return, opens it in Obsidian through the same `obsidian://bob-goto-task` landing the `/` picker uses. The panel shows the destination before Return, typing `@route^` browses that note's IDs as Go rows, misses are calm did-you-mean states, nothing is ever written, and every other caret form keeps today's meaning byte for byte.

## Notes

[2026-11-25T23:09:11Z · bob-cli-pl.6.1.land] DISCOVERED ISSUE: Landing bob-cli-pl.6.1 found bob-cli just docs-check failing at 9dd67c62 on two reference pages that phase bob-cli-q7.1 commit 4d930129 (feat(capture): treat whole-draft @route^id as read-only Go To) pushed over the 6000-word reference cap. Measured with tools/docs bob_docs.markdown.count_words per commit: docs/reference/capture-syntax.md d67a5b7b=5998 -> 4d930129=6058; docs/reference/json-outputs.md d67a5b7b=6000 -> 4d930129=6007. Earlier crossings by bob-cli-pl.6.1.1 (json-outputs) and bob-cli-ph.6.1.3 (capture-syntax) had already been trimmed back under the cap (28e23886, d67a5b7b) before 4d930129. No existing task tracks either page (searched capture-syntax / json-outputs across all task statuses plus the last-week sweep). The docs closeout (bob-cli-q7.6) should trim both pages under 6000 while preserving the Go To and props-contract rows.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-q7.1](bob-cli-q7.1.md) | bob-cli: claim, resolve, and refuse the bare caret address | ✓ closed | medium | 2026-11-25 | 1 | 1 |
| [bob-cli-q7.2](bob-cli-q7.2.md) | bob-cli: Go rows for @route^ completion, mint-collision copy, and /route^id search | ✓ closed | medium | 2026-11-25 | 1 | 1 |
| [bob-cli-q7.3](bob-cli-q7.3.md) | bob-plugins: any-line block fallback in the Go To re-find ladder | ✓ closed | small | 2026-11-25 | 1 | 0 |
| [bob-cli-q7.4](bob-cli-q7.4.md) | Mac: Go To destination card and Return dispatch | ◐ in_progress | medium | 2026-11-25 | 1 | 0 |
| [bob-cli-q7.5](bob-cli-q7.5.md) | Mac: Go rows in the block-ID card | ◐ in_progress | medium | 2026-11-25 | 1 | 0 |
| [bob-cli-q7.6](bob-cli-q7.6.md) | End-to-end verification and docs closeout | ◐ in_progress | small | 2026-11-25 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-q7: @route^id Go To: open a task by its exact address from Bob Capture [in_progress]"]
    n1["bob-cli-q7.1: bob-cli: claim, resolve, and refuse the bare caret address [closed]"]
    n2["bob-cli-q7.2: bob-cli: Go rows for @route^ completion, mint-collision copy, and /route^id search [closed]"]
    n3["bob-cli-q7.3: bob-plugins: any-line block fallback in the Go To re-find ladder [closed]"]
    n4["bob-cli-q7.4: Mac: Go To destination card and Return dispatch [in_progress]"]
    n5["bob-cli-q7.5: Mac: Go rows in the block-ID card [in_progress]"]
    n6["bob-cli-q7.6: End-to-end verification and docs closeout [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n2
    n1 -.-> n4
    n2 -.-> n5
    n3 -.-> n6
    n4 -.-> n5
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q7.1.md) | [bob-cli-q7.1](bob-cli-q7.1.md) | 1 |
| [bbugyi200.athena.bob-cli-q7.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q7.2/README.md) | [bob-cli-q7.2](bob-cli-q7.2.md) | 1 |
| [bbugyi200.athena.bob-cli-q7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q7.3/README.md) | [bob-cli-q7.3](bob-cli-q7.3.md) | 0 |
| [bbugyi200.athena.bob-cli-q7.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q7.4.md) | [bob-cli-q7.4](bob-cli-q7.4.md) | 0 |
| [bbugyi200.athena.bob-cli-q7.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q7.5/README.md) | [bob-cli-q7.5](bob-cli-q7.5.md) | 0 |
| [bbugyi200.athena.bob-cli-q7.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q7.6/README.md) | [bob-cli-q7.6](bob-cli-q7.6.md) | 0 |
| [bbugyi200.athena.bob-cli-q7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q7.land/README.md) | [bob-cli-q7](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4d93012`](https://github.com/bobs-org/bob-cli/commit/4d93012907c8d8048e2a6498450f4a803763c66a) | feat(capture): treat whole-draft @route^id as read-only Go To | [bob-cli-q7.1](bob-cli-q7.1.md) | 2026-11-25 17:10:47 EST |
| bob-cli | [`d883e56`](https://github.com/bobs-org/bob-cli/commit/d883e564ecac1aecc9c3b6d4a1c72517cae87379) | feat(capture): scoped browse block\_id.goto with archive rows, mint-collision hint, route^block-id search | [bob-cli-q7.2](bob-cli-q7.2.md) | 2026-11-25 18:16:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q7.3][1] | Need parent epic DECISIONS and phase notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q7.3/README.md

<!-- sase:referenced-by:end -->
