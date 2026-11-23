# Bead: bob-cli-on.11.1.3 — Render and stage requirement verdicts in the successor picker

[Bead Pages](../README.md) / [bob-cli-on.11.1](bob-cli-on.11.1.md) / bob-cli-on.11.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.md) · **Assignee:** `bob-cli-on.11.1.3` · **Size:** medium
**Created:** 2026-11-22 14:59:31 EST · **Closed:** 2026-11-22 16:56:39 EST
**Plan:** [202611/obsidian\_requirement\_close\_card.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_requirement_close_card.md)

## Description

picker_v6: add requirement groups, contextual keys and reasons, branch folds, navigation-only pins, and reqs results to the navigation successor picker v6.

## Notes

[2026-11-22T21:54:14Z · bob-cli-on.11.1.3--2] PROPOSED FOLLOW-UP: full-suite npm test unit flake in scripts/test-ledger-tools-event-link-times.cjs (not ok 2080, 25 ms wall-clock) and scripts/test-ledger-tools-frees-marks.cjs (not ok 2089, synthetic build 37 ms / budget 25 ms) under suite load on monitors hw3pan53kfay and 9c2ds6n5ngb3; files and ledger-tools sources are unchanged from parent 1e38521; isolated rerun 40/40 (event-link 4.0 ms, frees-marks 19 ms); already tracked by bob-cli-km and bob-cli-io

[2026-11-22T21:56:39Z · bob-cli-on.11.1.3--2] picker_v6 landed in 289c7f6 (requirement groups, keys, folds, pins, reqs results, api.successors v6). Verified: picker/verdict 87/87, isolated event-link-times+frees-marks 40/40 (4.0 ms / 19 ms), npm validate, plugin docs:check, just docs-check. Full npm test load-flaked the known 25ms walls on monitors hw3pan53kfay and 9c2ds6n5ngb3 (bob-cli-km, bob-cli-io). Deployed bob-navigation-hotkeys via descendant sync of 3fbe993 (no -F): 3 unchanged, stamp clean at 3fbe993. No epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-on.11.1.2](bob-cli-on.11.1.2.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-on.11.1.6](bob-cli-on.11.1.6.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.11.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.11.1.3.md) | [bob-cli-on.11.1.3](bob-cli-on.11.1.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`513ec47`](https://github.com/bobs-org/bob-cli/commit/513ec47889893245cd0aacf7f67895efcc253817) | docs(task-dependencies): mark picker v6 requirement consumer | [bob-cli-on.11.1.3](bob-cli-on.11.1.3.md) | 2026-11-22 16:04:56 EST |
| bob-plugins | [`bob-plugins@289c7f6`](https://github.com/bobs-org/bob-plugins/commit/289c7f6108a4055b29962f52502e452962b0f27e) | feat(navigation): add requirement verdict picker | [bob-cli-on.11.1.3](bob-cli-on.11.1.3.md) | 2026-11-22 16:31:34 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.11.1.4][1] | Need picker_v6 close status before retrying cycler sync | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.11.1.4/README.md

<!-- sase:referenced-by:end -->
