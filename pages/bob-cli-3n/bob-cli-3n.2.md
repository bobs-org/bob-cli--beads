# Bead: bob-cli-3n.2 — Rust dependency-line parser, promotion edges, and parser guards

[Bead Pages](../README.md) / [bob-cli-3n](README.md) / bob-cli-3n.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vl.md) · **Assignee:** `bob-cli-3n.2` · **Size:** medium
**Created:** 2026-10-02 16:54:34 EDT · **Closed:** 2026-10-02 19:26:38 EDT
**Plan:** [202610/task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links.md)

## Description

hooks-edges: add the bob-cli task_dependencies module (parse, canonical format, link form, shared id encoder, legacy children). Promotion edges come from Depends-On links plus legacy children, and #^ref embeds stop being edges. Guard the capture close, section, log, and placement parsers, and fix move-done-tasks pathless links.

## Notes

[2026-10-02T23:26:38Z · bob-cli-3n.2] hooks-edges done: task_dependencies module (DP/DW vectors green), dep-line+R8 promotion edges, capture guards (close/section/log/placement), move-done-tasks pathless repair, fixtures+CLI tests updated, docs+README+help updated; just all passes (fmt/lint/test). 9 dead-code warnings on format.rs writer helpers, wired next in hooks-reconcile.

## Dependencies

- **Depends on:** [bob-cli-3n.1](bob-cli-3n.1.md) ✓ · ⧖ 2026-10-02
- **Blocks:** [bob-cli-3n.3](bob-cli-3n.3.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.2/README.md) | [bob-cli-3n.2](bob-cli-3n.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2d4d508`](https://github.com/bobs-org/bob-cli/commit/2d4d50835ef449d971920c911903436fe78b0907) | feat(hooks): Rust dependency-line parser, promotion edges, and parser guards | [bob-cli-3n.2](bob-cli-3n.2.md) | 2026-10-02 19:27:39 EDT |
