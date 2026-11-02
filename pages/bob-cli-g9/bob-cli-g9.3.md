# Bead: bob-cli-g9.3 — bob-ledger-tools config, decide, and mark parity

[Bead Pages](../README.md) / [bob-cli-g9](README.md) / bob-cli-g9.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.32.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.32.linker.w0.md) · **Assignee:** `bob-cli-g9.3` · **Size:** medium
**Created:** 2026-11-02 15:55:42 EST · **Closed:** 2026-11-02 17:52:04 EST
**Plan:** [202611/task\_decay\_ladder.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_decay_ladder.md)

## Description

ledger-mirror: mirror the per-rung config and lane decide in bob-ledger-tools against the new vectors, show the decay mark on lane rows only when navigation's card capability is at least 3, count lane decisions in the footer, and bump the freshness namespace.

## Notes

[2026-11-02T22:51:48Z · bob-cli-g9.3] PROPOSED FOLLOW-UP: five bob-plugins unit tests fail identically on the clean base tree (verified via git stash + rebuild): the reload-event due-key test in test-ledger-tools-freshness-namespace, production-sheet DOM test, note-ready startup-storm linearity, relation-index layout-ready replay, and nav future-scheduling-on-Pending Work Log test — triage as flakes/env or file task beads

[2026-11-02T22:52:04Z · bob-cli-g9.3] ledger-mirror done: per-rung decay config (pending/next/ready vs keeps fallback, false=never-ask) and lane decide mirrored from Rust schema-15 vectors C14-C21/D8-D18; lane leaf gated on nav card v3+ with counting-only pips below; freshness namespace v12->v13 with perRungDecay; ledger-tools manifest 1.94.0; docs/freshness.md 11/12 + bob-ledger-tools.md updated. Verified: focused freshness suites 279/280 (only pre-existing reload-event failure, confirmed on clean tree), bob-plugins docs:check pass, bob-cli just docs-check pass (447), bob plugins sync ok

## Dependencies

- **Depends on:** [bob-cli-g9.2](bob-cli-g9.2.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-g9.4](bob-cli-g9.4.md) ◐ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-g9.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-g9.3/README.md) | [bob-cli-g9.3](bob-cli-g9.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b4a17e8`](https://github.com/bobs-org/bob-cli/commit/b4a17e86622bc3cf6145f7fb105b1f985f6ce621) | docs(freshness): document lane decay marks and per-rung keeps wording | [bob-cli-g9.3](bob-cli-g9.3.md) | 2026-11-02 17:54:03 EST |
