# Bead: bob-cli-on.3 — The task block layout module and requirement line writers

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.3` · **Size:** medium
**Created:** 2026-11-21 11:13:26 EST · **Closed:** 2026-11-21 13:31:16 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

block-layout: add task_block_layout (zones, insertion slots, tidy planning, the NOTES rule) and the pure drop/restore/toggle/first-requirement writers with RL and RW vectors, then route ensure_drawer and capture note placement through it.

## Notes

[2026-11-21T18:30:45Z · bob-cli-on.3] PROPOSED FOLLOW-UP: docs-check still fails on the clean base (lint budget caps on docs/develop/plugins/plugin-apis.md, docs/reference/plugins/bob-navigation-hotkeys.md, docs/reference/vault-format.md; strict build anchor task-dependencies.md#1224-js--jump-successor-contract-and-vectors does not exist) — already noted by bob-cli-oe.2; block-layout docs add no new docs-lint finding

[2026-11-21T18:30:51Z · bob-cli-on.3] PROPOSED FOLLOW-UP: flaky test — tests/cli albums_update::completion_offers_update_stems_and_input_files failed once inside a full parallel `cargo test --test cli` run and passed alone and on the next two full runs, unrelated to this phase

[2026-11-21T18:30:55Z · bob-cli-on.3] PROPOSED FOLLOW-UP: capture-reqs should surface implicit NOTES filing in bob capture JSON — block-layout routes a note on a req-owning task into NOTES via task_block_layout::note_home, but notes[].drawer and the top-level drawer stay null for that implicit route (the task_blocks diff already shows the NOTES lines)

[2026-11-21T18:31:16Z · bob-cli-on.3] Added src/native/task_block_layout (zones, insertion slots, layout_violations, plan_tidy, NOTES rule/note_home, drop/restore/toggle/insert req writers) with RL1-RL52 (layout.json) and RW1-RW53 (writes.json) vectors; routed ensure_drawer, capture sub-bullet note placement and its dry-run preview through it; fixed Depends-On adoption slots (reconcile child_slot, capture cancel_log_aware_slot) that landed between a Cancel Log marker and its entries. Verified: just lint clean, cargo fmt clean, cargo test --workspace passes (7567 lib, 3902 cli), just docs-gen clean; docs-check/docs-lint fail only on the same 3 pre-existing over-budget pages as the clean base.

## Dependencies

- **Depends on:** [bob-cli-on.1](bob-cli-on.1.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.10](bob-cli-on.10.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.4](bob-cli-on.4.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.6](bob-cli-on.6.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-on.7](bob-cli-on.7.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.3/README.md) | [bob-cli-on.3](bob-cli-on.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ca07094`](https://github.com/bobs-org/bob-cli/commit/ca070941c05b42840a40d87f0e4f6a6e0aab6090) | feat(task-reqs): add task block layout and req line writers | [bob-cli-on.3](bob-cli-on.3.md) | 2026-11-21 13:32:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.3][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-on.4][2] | See prior PROPOSED FOLLOW-UP notes about docs-check and the albums completion flake to cite them | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.4/README.md

<!-- sase:referenced-by:end -->
