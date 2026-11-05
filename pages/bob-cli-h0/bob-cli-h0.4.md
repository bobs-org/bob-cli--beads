# Bead: bob-cli-h0.4 — move\_choice report, \`-m/--move-in\`, answer resolution, and refusals

[Bead Pages](../README.md) / [bob-cli-h0](README.md) / bob-cli-h0.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.37.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.37.linker.w0.md) · **Assignee:** `bob-cli-h0.4` · **Size:** medium
**Created:** 2026-11-04 08:50:24 EST · **Closed:** 2026-11-04 12:30:46 EST
**Plan:** [202611/move\_choice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/move_choice.md)

## Description

cli-report: build the `move_choice` report from the staged parent, add `-m/--move-in`, resolve answers to rows, emit every write-free refusal in order, and print the numbered terminal list; answered runs still refuse until cli-execute.

## Notes

[2026-11-04T17:30:12Z · bob-cli-h0.4] Timing (§3.11): warm dry-run on 76-root parent (cash.md) — with - ^^ avg 173.6 ms, without - ^^ avg 42.3 ms, diff 131.3 ms (under 150 ms budget). Measured 5 runs each via bob capture --dry-run, BOB_NOW=2026-09-20 14:31:07 TZ=UTC0.

[2026-11-04T17:30:46Z · bob-cli-h0.4] cli-report done: move_choice report with rows/mints/locks/disabled/consequence, -m/--move-in parsing and resolution, write-free refusals in order (unasked/empty/required/conflict/stale/refused/unused + unavailable interim), numbered terminal list and hint. Verified: 6 new choice tests pass, 1622 capture tests pass, lib kinds test fixed, fixtures updated, docs-gen capture.md updated, timing diff 131ms under 150ms. Full cli 2 flaky failures pass alone; docs-check blocked by pre-existing memory strand front-matter.

## Dependencies

- **Depends on:** [bob-cli-h0.2](bob-cli-h0.2.md) ✓ · ⧖ 2026-11-04
- **Depends on:** [bob-cli-h0.3](bob-cli-h0.3.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h0.5](bob-cli-h0.5.md) ✓ · ⧖ 2026-11-04
- **Blocks:** [bob-cli-h0.7](bob-cli-h0.7.md) ✓ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-h0.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.4/README.md) | [bob-cli-h0.4](bob-cli-h0.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cf2e3c9`](https://github.com/bobs-org/bob-cli/commit/cf2e3c9f8b1b61a7bd20e9886e08446ef65ccd81) | feat(capture): add move\_choice report, -m/--move-in and refusals | [bob-cli-h0.4](bob-cli-h0.4.md) | 2026-11-04 12:58:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h0.4][1] | Need the phase scope and design file | 3 |
| read-by | [agent:bob-cli-h0.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-h0.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-h0.land.md

<!-- sase:referenced-by:end -->
