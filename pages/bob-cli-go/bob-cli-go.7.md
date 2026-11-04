# Bead: bob-cli-go.7 — Obsidian Ctrl+Shift+T split — JS twin and cursor gestures

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.7` · **Size:** medium
**Created:** 2026-11-03 16:11:31 EST · **Closed:** 2026-11-03 20:23:50 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

nav-split: port the split planner to JS against the copied vectors, then register Ctrl+Shift+T for the cursor, counted, and visual-selection splits, with one-transaction undo, cursor landing, notices, and the Undo-close-tab rebind.

## Notes

[2026-11-04T01:23:30Z · bob-cli-go.7] PROPOSED FOLLOW-UP: bob-plugins npm run docs:check generated-drift fails because the fetched bob-cli context has sase/memory/glossary/task-merge.md without front matter; identical on the clean tree, owned by closeout (accepted memory_glossary_strands), already routed per the parent epic note

[2026-11-04T01:23:36Z · bob-cli-go.7] PROPOSED FOLLOW-UP: full npm test shows 6 pre-existing failures identical on the clean tree, all already tracked (bob-cli-ej perf flake, bob-cli-eh startup slots, bob-cli-f1 headless DOM, bob-cli-et real-date family); 5401/5407 pass including all 12 new task-split tests

[2026-11-04T01:23:50Z · bob-cli-go.7] nav-split landed: planSplitBullets twin passes all 30 vectors byte-for-byte; Ctrl+Shift+T cursor/counted/selection splits with one-transaction undo, cursor landing, and Undo notice; hotkeys.json rebind added; manifest 2.73.2; npm test 5401/5407 with 6 pre-existing failures verified identical on clean tree (all tracked); docs:check drift pre-existing on clean tree (closeout owns the memory strands); bob plugins sync deployed nav-hotkeys

## Dependencies

- **Depends on:** [bob-cli-go.3](bob-cli-go.3.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.8](bob-cli-go.8.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.7/README.md) | [bob-cli-go.7](bob-cli-go.7.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@60045f2`](https://github.com/bobs-org/bob-plugins/commit/60045f279de3dc35337c5fbee4ab0646dd3863e0) | feat(nav-split): port split planner to JS and register Ctrl+Shift+T | [bob-cli-go.7](bob-cli-go.7.md) | 2026-11-03 20:25:18 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.7][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-go.7/README.md

<!-- sase:referenced-by:end -->
