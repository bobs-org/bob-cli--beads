# Bead: bob-cli-h4.1 — bob emits landing blocks for transfers (target, tombstones, moved tasks, sections)

[Bead Pages](../README.md) / [bob-cli-h4](README.md) / bob-cli-h4.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.188](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.188.md) · **Assignee:** `bob-cli-h4.1` · **Size:** medium
**Created:** 2026-11-04 14:57:18 EST
**Plan:** [202611/transfer\_previews.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/transfer_previews.md)

## Description

bob-landing-blocks: make every capture `>` transfer report batch-level `task_blocks` with new roles `merge_target`, `merge_source`, and `moved`. Moved blocks carry `moved_from` and a before-image taken from the source note. Add a batch-level `section_blocks` array for section merges. All JSON is additive.

## Dependencies

- **Blocks:** [bob-cli-h4.5](bob-cli-h4.5.md) ◐ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h4.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h4.1/README.md) | [bob-cli-h4.1](bob-cli-h4.1.md) | 0 |
