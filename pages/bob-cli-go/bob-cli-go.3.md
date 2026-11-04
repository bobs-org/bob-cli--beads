# Bead: bob-cli-go.3 — Rust split planner and \`bob task split\`

[Bead Pages](../README.md) / [bob-cli-go](README.md) / bob-cli-go.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.36.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.36.linker.w0.md) · **Assignee:** `bob-cli-go.3` · **Size:** medium
**Created:** 2026-11-03 16:11:30 EST · **Closed:** 2026-11-03 19:53:40 EST
**Plan:** [202611/task\_move\_merge\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_move_merge_split.md)

## Description

split-cli: implement the pure plan_task_split that passes every split vector byte-for-byte, extract the task-move command shell for reuse, and ship `bob task split` with candidate listing, dry-run parity, scoped commits, and JSON.

## Notes

[2026-11-04T00:53:02Z · bob-cli-go.3--7] PROPOSED FOLLOW-UP: Repair or document the docs generator handling of legacy glossary strands without front matter; `just docs-check` currently passes lint but fails generated drift at sase/memory/glossary/task-merge.md for missing front matter.

[2026-11-04T00:53:40Z · bob-cli-go.3--7] Verified the task split conformance test ran once and passed all 30 vectors; cargo run --quiet -- task split --help exposes the command and generated CLI references include it. just docs-check passes lint but fails generated drift because existing sase/memory/glossary/task-merge.md lacks front matter; recorded a PROPOSED FOLLOW-UP without editing memory. git diff --check passes; epic-symbol check has no leftovers.

## Dependencies

- **Depends on:** [bob-cli-go.1](bob-cli-go.1.md) ✓ · ⧖ 2026-11-03
- **Depends on:** [bob-cli-go.2](bob-cli-go.2.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.5](bob-cli-go.5.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-go.7](bob-cli-go.7.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-go.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.3.md) | [bob-cli-go.3](bob-cli-go.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`734214e`](https://github.com/bobs-org/bob-cli/commit/734214e92c5495fa34a9d02818b9e820d21f004f) | feat(task): add task split planner and CLI | [bob-cli-go.3](bob-cli-go.3.md) | 2026-11-03 19:54:52 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-go.3--7][1] | Need phase scope, design file, notes, and completion state | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.3.md

<!-- sase:referenced-by:end -->
