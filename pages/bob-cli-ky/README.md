# Bead: bob-cli-ky — Walker footers follow the active bracket walk

[Bead Pages](../README.md) / bob-cli-ky

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bu](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bu.md) · **Assignee:** `bob-cli-ky.land`
**Created:** 2026-11-12 12:30:15 EST
**Plan:** [202611/walker\_footers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/walker_footers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/walker_footers.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/walker_footers.md

<!-- sase:links:end -->

## Description

Obsidian's status bar shows exactly one walker footer that matches the persisted bracket walk: the review footer only while `s` is active (with a calm clear state instead of hiding), a new lane footer for `w`, a new links compass for `n`, a quiet review-due dot on the selector's `s` letter, byte-compatible legacy fallbacks, updated docs, and a published Walker Footer glossary term.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ky.1](bob-cli-ky.1.md) | nav api.walkMode v1 and the walk-mode doorbell | ✓ closed | small | 2026-11-12 | 1 | 1 |
| [bob-cli-ky.2](bob-cli-ky.2.md) | Ledger walker-footer host and the gated s panel | ✓ closed | medium | 2026-11-12 | 1 | 1 |
| [bob-cli-ky.3](bob-cli-ky.3.md) | Lane footer for the w walk | ✓ closed | medium | 2026-11-12 | 1 | 1 |
| [bob-cli-ky.4](bob-cli-ky.4.md) | nav links() and the links footer for the n walk | ✓ closed | medium | 2026-11-12 | 1 | 1 |
| [bob-cli-ky.5](bob-cli-ky.5.md) | Review attention dot on the selector's s | ✓ closed | small | 2026-11-12 | 1 | 1 |
| [bob-cli-ky.6](bob-cli-ky.6.md) | Visual previews, e2e, and placement | ◐ in_progress | medium | 2026-11-12 | 1 | 0 |
| [bob-cli-ky.7](bob-cli-ky.7.md) | Docs, memory, and deploy | ◐ in_progress | medium | 2026-11-12 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ky: Walker footers follow the active bracket walk [in_progress]"]
    n1["bob-cli-ky.1: nav api.walkMode v1 and the walk-mode doorbell [closed]"]
    n2["bob-cli-ky.2: Ledger walker-footer host and the gated s panel [closed]"]
    n3["bob-cli-ky.3: Lane footer for the w walk [closed]"]
    n4["bob-cli-ky.4: nav links() and the links footer for the n walk [closed]"]
    n5["bob-cli-ky.5: Review attention dot on the selector's s [closed]"]
    n6["bob-cli-ky.6: Visual previews, e2e, and placement [in_progress]"]
    n7["bob-cli-ky.7: Docs, memory, and deploy [in_progress]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n1 -.-> n2
    n2 -.-> n3
    n3 -.-> n4
    n4 -.-> n5
    n5 -.-> n6
    n6 -.-> n7
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ky.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.1/README.md) | [bob-cli-ky.1](bob-cli-ky.1.md) | 1 |
| [bbugyi200.athena.bob-cli-ky.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.2/README.md) | [bob-cli-ky.2](bob-cli-ky.2.md) | 1 |
| [bbugyi200.athena.bob-cli-ky.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.3/README.md) | [bob-cli-ky.3](bob-cli-ky.3.md) | 1 |
| [bbugyi200.athena.bob-cli-ky.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ky.4.md) | [bob-cli-ky.4](bob-cli-ky.4.md) | 1 |
| [bbugyi200.athena.bob-cli-ky.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.5/README.md) | [bob-cli-ky.5](bob-cli-ky.5.md) | 1 |
| [bbugyi200.athena.bob-cli-ky.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.6/README.md) | [bob-cli-ky.6](bob-cli-ky.6.md) | 0 |
| [bbugyi200.athena.bob-cli-ky.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.7/README.md) | [bob-cli-ky.7](bob-cli-ky.7.md) | 0 |
| [bbugyi200.athena.bob-cli-ky.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ky.land/README.md) | [bob-cli-ky](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d36acba`](https://github.com/bobs-org/bob-plugins/commit/d36acba1b09d1ae19868a467ad56c8b9e4ea9e0f) | feat(nav-hotkeys): add api.walkMode v1 and the walk-mode doorbell | [bob-cli-ky.1](bob-cli-ky.1.md) | 2026-11-12 12:47:01 EST |
| bob-plugins | [`bob-plugins@83d4a9f`](https://github.com/bobs-org/bob-plugins/commit/83d4a9f06e9489cd6f454118dd2599b0497f5b48) | feat(ledger-tools): route walker footer by bracket walk with gated s panel | [bob-cli-ky.2](bob-cli-ky.2.md) | 2026-11-12 13:10:48 EST |
| bob-plugins | [`bob-plugins@394b793`](https://github.com/bobs-org/bob-plugins/commit/394b793ea7be226c090c9654c3c3af8bec2bc040) | feat(ledger-tools): add bracket walk lane footer | [bob-cli-ky.3](bob-cli-ky.3.md) | 2026-11-12 13:56:06 EST |
| bob-plugins | [`bob-plugins@3fc55c9`](https://github.com/bobs-org/bob-plugins/commit/3fc55c911cecca84be0e9a80ddf7a26180ab5894) | feat(walker-footer): add links compass panel | [bob-cli-ky.4](bob-cli-ky.4.md) | 2026-11-12 14:51:26 EST |
| bob-plugins | [`bob-plugins@c7a500e`](https://github.com/bobs-org/bob-plugins/commit/c7a500e43207df63c4c80246f6a5d23e711e54cb) | feat(navigation): add review attention dot to walk selector | [bob-cli-ky.5](bob-cli-ky.5.md) | 2026-11-12 15:03:30 EST |
