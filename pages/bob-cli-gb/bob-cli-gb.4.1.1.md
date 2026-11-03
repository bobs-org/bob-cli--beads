# Bead: bob-cli-gb.4.1.1 — Parse and render explicit Google clock tags without losing ownership

[Bead Pages](../README.md) / [bob-cli-gb.4.1](bob-cli-gb.4.1.md) / bob-cli-gb.4.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-gb.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gb.4.md) · **Assignee:** `bob-cli-gb.4.1.1` · **Size:** medium
**Created:** 2026-11-02 18:52:59 EST · **Closed:** 2026-11-02 20:50:48 EST
**Plan:** [202611/gcal\_clock\_tags.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_clock_tags.md)

## Description

explicit-clock-tags: replace gcal's explicit clock boolean with the shared ClockTag vocabulary, preserve title/description alias provenance, recognize #on in directive lines, render only explicit #off/#on, migrate untouched legacy spans, and compare normalized none/off/on values for kept_off_clock. Extend the shared event-buffer vectors additively and verify parsing, rendering, migration, and flip behavior.

## Notes

[2026-11-03T01:50:48Z · bob-cli-gb.4.1.1--3] Implemented explicit Google #off/#on parsing, canonical badge migration, alias normalization, and clock flip handling; extended shared event-buffer vectors and lifecycle/list/sync coverage. Full just check passed (monitor 07nrjfnz3560, 2026-11-03). epic-symbols had no unresolved entries.

## Dependencies

- **Blocks:** [bob-cli-gb.4.1.2](bob-cli-gb.4.1.2.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gb.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gb.4.1.1.md) | [bob-cli-gb.4.1.1](bob-cli-gb.4.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4d5a61d`](https://github.com/bobs-org/bob-cli/commit/4d5a61de6a5f2437a5db97a95d444f9d055fb327) | feat(gcal): parse and render explicit clock tags | [bob-cli-gb.4.1.1](bob-cli-gb.4.1.1.md) | 2026-11-02 21:09:07 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-gb.4.1.1--3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gb.4.1.1.md

<!-- sase:referenced-by:end -->
