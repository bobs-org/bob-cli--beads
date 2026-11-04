# Bead: bob-cli-gl.5.1.2 — Link moved tasks and integrate project offers

[Bead Pages](../README.md) / [bob-cli-gl.5.1](bob-cli-gl.5.1.md) / bob-cli-gl.5.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-gl.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.md) · **Assignee:** `bob-cli-gl.5.1.2` · **Size:** medium
**Created:** 2026-11-03 16:14:53 EST · **Closed:** 2026-11-03 19:12:29 EST
**Plan:** [202611/capture\_move\_execution.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_move_execution.md)

## Description

move_links_offers: Execute colon moves and selected moved offers through existing-task link semantics in draft order with new tasks. Preserve followed links, dependency drops, scheduling and project guards, offer identity, and complete move reports.

## Notes

[2026-11-04T00:10:16Z · bob-cli-gl.5.1.2] PROPOSED FOLLOW-UP: bob-obsidian catalog shape tests fail on clean base (69 vs 67) — native::catalog::tests::document_shape and catalog::protocol_1_parses_with_schema_version_one fail identically with and without 5.1.2 changes; needs owner triage outside move_links_offers scope

[2026-11-04T00:12:20Z · bob-cli-gl.5.1.2] PROPOSED FOLLOW-UP (routed): catalog failures duplicate closed bob-cli-de, corroborated with +1 --verified-after-close; no new bead per phase policy

[2026-11-04T00:12:29Z · bob-cli-gl.5.1.2] move_links_offers complete: colon moves + selected moved offers link via existing-task semantics in draft order (MV4/MV5/MV9-colon/MV16, mixed ordering, all/none/subset, moved_from). Verified: focused regressions 347 passed/0 failed; just fmt clean; epic-symbols clean. Full just check shows no new failures — only 2 bob-obsidian catalog shape failures (document_shape + protocol_1 CLI, 69 vs 67) reproducing identically on clean base; duplicate of closed bob-cli-de, corroborated via +1.

## Dependencies

- **Depends on:** [bob-cli-gl.5.1.1](bob-cli-gl.5.1.1.md) ✓ · ⧖ 2026-11-03
- **Blocks:** [bob-cli-gl.5.1.3](bob-cli-gl.5.1.3.md) ✓ · ⧖ 2026-11-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gl.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.2.md) | [bob-cli-gl.5.1.2](bob-cli-gl.5.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`14a5773`](https://github.com/bobs-org/bob-cli/commit/14a577321f81119ccb24dc41c81caa9aa9af8650) | feat(capture): link moved tasks and integrate project offers | [bob-cli-gl.5.1.2](bob-cli-gl.5.1.2.md) | 2026-11-03 19:29:57 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gl.5.1.2--1][1] | Confirm closed bead needs no reopen after known base failure | 2 |
| read-by | [agent:bob-cli-go.4.1.1--2][2] | Check whether the catalog shape count mismatch is already tracked | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gl.5.1.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-go.4.1.1.md

<!-- sase:referenced-by:end -->
