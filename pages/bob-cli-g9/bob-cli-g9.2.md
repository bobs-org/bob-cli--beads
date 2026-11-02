# Bead: bob-cli-g9.2 — Rust config, decide, and reconcile contract

[Bead Pages](../README.md) / [bob-cli-g9](README.md) / bob-cli-g9.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.32.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.32.linker.w0.md) · **Assignee:** `bob-cli-g9.2` · **Size:** medium
**Created:** 2026-11-02 15:55:42 EST · **Closed:** 2026-11-02 16:46:30 EST
**Plan:** [202611/task\_decay\_ladder.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_decay_ladder.md)

## Description

rust-contract: parse per-rung allowances (pending_keeps, next_keeps, ready_keeps with keeps fallback), widen decide to the PENDING and NEXT tiers, make reconcile lane raises clear [keeps::], pin with a test that a stepped-down former prerequisite is not re-raised, bump freshness JSON to schema 15, extend the shared vectors, and update the bob-cli contract docs.

## Notes

[2026-11-02T21:46:30Z · bob-cli-g9.2] Verified rust-contract: per-rung pending_keeps/next_keeps/ready_keeps (0–999 or false, keeps fallback, default 3); decide_for on due PENDING/NEXT plus Ready ROTTEN/TICKLER at AskAt(L), never on is_today, unblocked, PROJECTS, recurring, or checklists; reconcile MarkNext/MarkInProgress/Unblock(Next|InProgress) strip [keeps::] while Unblock(Ready) preserves; Adjustment 1 hand-set Ready stays Ready after blocked consume; freshness JSON schema 15 with decay.limits; equal-rung header 'keeps N' and mixed 'keeps WIP X · Next Y · Ready Z'; C1–C13/K* byte-stable, C14–C21 and D8–D18 added; docs §2a/4/7/10a plus vault-format, configuration, json-outputs, contracts.yml. Tests: 152 freshness lib, 33 freshness CLI, targeted reconcile CLI, docs tutorial schema 15, README table snapshot. Epic-symbols empty. Memory not edited.

## Dependencies

- **Blocks:** [bob-cli-g9.3](bob-cli-g9.3.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-g9.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-g9.2.md) | [bob-cli-g9.2](bob-cli-g9.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6086791`](https://github.com/bobs-org/bob-cli/commit/6086791f76b2564e37bd282bd63ea5ef7d2a07a8) | feat(freshness)!: bump freshness JSON to schema 15 with per-rung decay limits | [bob-cli-g9.2](bob-cli-g9.2.md) | 2026-11-02 17:25:48 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-g9.2--1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-g9.2.md

<!-- sase:referenced-by:end -->
