# Bead: bob-cli-h8.3 — Fix archived-task minutes and multi-link splitting in the periods brief

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.3` · **Size:** medium
**Created:** 2026-11-04 16:39:09 EST · **Closed:** 2026-11-04 17:04:31 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

brief-attribution: in src/native/periods/brief.rs, resolve original and done/ archive paths to one task identity (bob-cli-gs), and split a multi-link Pomodoro's minutes with the stats root_parent splitter so task rows never outrank their root (bob-cli-gt). Land this before the 2026-11-09 Review.

## Notes

[2026-11-04T22:04:31Z · bob-cli-h8.3] brief-attribution done: archive identity plus split_minutes in src/native/periods/brief.rs with docs/periods.md contract note; focused periods::brief_* (6) and periods::* (24) pass, docs-check passes; live W43 bob root lists archived tasks and W41 no task outranks root; just check clippy still red in untouched capture_language files owned by h2/h0

## Dependencies

- **Blocks:** [bob-cli-h8.9](bob-cli-h8.9.md) ○ · ⧖ 2026-11-04

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.3/README.md) | [bob-cli-h8.3](bob-cli-h8.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-h8.3][1] | Need phase notes and remaining work check | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.3/README.md

<!-- sase:referenced-by:end -->
