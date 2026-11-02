# Bead: bob-cli-fv.4 — Separator, badge-duplicate, and vendor boilerplate filter

[Bead Pages](../README.md) / [bob-cli-fv](README.md) / bob-cli-fv.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5o.linker.w0.md) · **Assignee:** `bob-cli-fv.4` · **Size:** medium
**Created:** 2026-11-02 09:28:51 EST · **Closed:** 2026-11-02 10:52:38 EST
**Plan:** [202611/gcal\_description\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_description_bullets.md)

## Description

boilerplate-filter: drop separators, lines that only repeat the 📹 or 📍 target, and fenced or header-anchored Meet, Zoom, Teams, and Webex blocks. Keep a join link only when the row has no 📹 badge.

## Notes

[2026-11-02T15:52:38Z · bob-cli-fv.4] boilerplate-filter done: new description/boilerplate.rs runs separator, fenced-region, header-run, and badge-duplicate passes in filter_source_lines with the one kept Join-link bullet; 14-case boilerplate.json vectors plus keep-label unit tests pass; event_buffer/vectors.json green; just check green (fmt+clippy+full tests)

## Dependencies

- **Depends on:** [bob-cli-fv.3](bob-cli-fv.3.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-fv.6](bob-cli-fv.6.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fv.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fv.4/README.md) | [bob-cli-fv.4](bob-cli-fv.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cba88d0`](https://github.com/bobs-org/bob-cli/commit/cba88d0d785aa47c1ba3720c035f4cab4b7786bb) | feat(gcal): filter vendor boilerplate from event descriptions | [bob-cli-fv.4](bob-cli-fv.4.md) | 2026-11-02 10:54:17 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fv.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fv.4/README.md

<!-- sase:referenced-by:end -->
