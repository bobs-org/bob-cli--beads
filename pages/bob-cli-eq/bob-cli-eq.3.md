# Bead: bob-cli-eq.3 — Warm vault task index

[Bead Pages](../README.md) / [bob-cli-eq](README.md) / bob-cli-eq.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b5.md) · **Assignee:** `bob-cli-eq.3` · **Size:** medium
**Created:** 2026-10-30 16:10:20 EDT · **Closed:** 2026-10-30 17:39:24 EDT
**Plan:** [202610/obsidian\_task\_wikilinks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/obsidian_task_wikilinks.md)

## Description

index: an incrementally maintained, mtime-validated vault task index with live-editor overlays, streaming cold builds, and performance budgets.

## Notes

[2026-10-30T21:39:24Z · bob-cli-eq.3] Index phase done: src/036-task-wikilink-index.js (TaskWikilinkIndex store + Obsidian adapter: chunked cold build, event maintenance, mtime-validated snapshot with live overlays, taskBearingDocuments/refreshPaths, bounded warnings) plus unit + performance tests, all wired (fragments, exports, package.json) and built. Ranks 032 as well (indexOf tiers, hoisted terms, fused scorer, indexed loops, single-pass locator+target) with semantics pinned by vector parity + a new randomized differential test. Verified: build --check, validate 8/8, model+unit+perf 38/38 green repeatedly; full npm test 4466/4469 with only flakes that reproduce on the clean tree (relation-index startup timing, already tracked by task bead bob-cli-eh and noted on eq.2) or box-load timing. decision_record follow-up already recorded on eq.1. bob plugins sync refused (sibling workspace bob-cli_15 has an uncommitted block-id-prompt deployment; must not force) — land agent to sync after merge.

## Dependencies

- **Depends on:** [bob-cli-eq.1](bob-cli-eq.1.md) ✓ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-eq.4](bob-cli-eq.4.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eq.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.3/README.md) | [bob-cli-eq.3](bob-cli-eq.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@4ef761a`](https://github.com/bobs-org/bob-plugins/commit/4ef761a6ec491e607c405ee4d7bf0a1867c1a145) | feat(block-id-prompt): warm vault task index for the (( picker | [bob-cli-eq.3](bob-cli-eq.3.md) | 2026-10-30 17:40:44 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eq.3][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.3/README.md

<!-- sase:referenced-by:end -->
