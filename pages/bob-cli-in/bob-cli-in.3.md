# Bead: bob-cli-in.3 — End-to-end acceptance matrix, alias parity, and lint scaffolding

[Bead Pages](../README.md) / [bob-cli-in](README.md) / bob-cli-in.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.19v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.19v.md) · **Assignee:** `bob-cli-in.3` · **Size:** medium
**Created:** 2026-11-08 06:23:52 EST · **Closed:** 2026-11-08 10:06:44 EST
**Plan:** [202611/gmail\_sync\_ii3\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_ii3_completion.md)

## Description

acceptance: add the missing tests/gmail_sync.rs composition coverage, including byte-identical sync versus pull in separate fixed-time fixtures, and remove the stale dead_code allowances left from the command phase.

## Notes

[2026-11-08T15:06:44Z · bob-cli-in.3] Expanded offline sync/pull composition coverage for adoption, lifecycle, limits, failures, contention, Git scope, and byte-identical alias behavior across separate fixed-time fixtures; removed stale sync/route dead_code scaffolding and unused scan/budget APIs, keeping only narrow documented future-consumer allowances. Verified no epic symbols remain; cargo rustc --force-warn dead_code; 397 cargo test -p bob-obsidian --lib gmail:: tests passed after the known lock-contention test passed isolated and on rerun; gmail_sync (20), gmail_shell (61), gmail_pull_attach (2) passed; cargo fmt --all -- --check and just lint passed.

## Dependencies

- **Depends on:** [bob-cli-in.2](bob-cli-in.2.md) ✓ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-in.4](bob-cli-in.4.md) ◐ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-in.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-in.3/README.md) | [bob-cli-in.3](bob-cli-in.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`51d572d`](https://github.com/bobs-org/bob-cli/commit/51d572d59075cc1b9363051ec453b4d3ee3e1ed4) | test(gmail): expand sync acceptance coverage | [bob-cli-in.3](bob-cli-in.3.md) | 2026-11-08 10:08:18 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-in.2][1] | Check sibling phase status to avoid overlap | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-in.2/README.md

<!-- sase:referenced-by:end -->
