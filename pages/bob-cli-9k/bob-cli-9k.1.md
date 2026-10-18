# Bead: bob-cli-9k.1 — Shared homes resolver, rollup switch, contract, and vault config

[Bead Pages](../README.md) / [bob-cli-9k](README.md) / bob-cli-9k.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4t.linker.w0.md) · **Assignee:** `bob-cli-9k.1` · **Size:** medium
**Created:** 2026-10-18 16:35:49 EDT · **Closed:** 2026-10-18 17:22:43 EDT
**Plan:** [202610/pomodoro\_homes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes.md)

## Description

homes-core: build the one Rust resolver for task homes, session links, review sessions, splitting, labels, chips, and hues. Parse and lint `rollup` and area `color`. Write the normative docs/pomodoro-homes.md and the shared conformance vectors, show the rollup flag in `bob projects list`, and configure sase.md and the six top-level area notes.

## Notes

[2026-10-18T21:22:43Z · bob-cli-9k.1--1] homes-core landed: shared Rust resolver (facts/resolve/session/label/palette/json), docs/pomodoro-homes.md plus conformance vectors, rollup tag on bob projects list, and live vault rollup/color frontmatter. Verified just check (exit 0), just install, bob projects list shows 'sase rollup', and disk-source smoke on 2026/20261018.md (BLOG=sase, HACK=bob · dev +1). No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-9k.2](bob-cli-9k.2.md) ◐ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9k.4](bob-cli-9k.4.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9k.5](bob-cli-9k.5.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.1.md) | [bob-cli-9k.1](bob-cli-9k.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9ec332c`](https://github.com/bobs-org/bob-cli/commit/9ec332c81def3014a559e088124ef93e3bb15ae7) | feat(homes): add shared Pomodoro home resolver and rollup contract | [bob-cli-9k.1](bob-cli-9k.1.md) | 2026-10-18 17:23:52 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9k.1][1] | Confirm remaining phase requirements before final verification | 2 |
| read-by | [agent:bob-cli-9k.1--1][1] | Need the phase scope, notes, and design file after just check passed | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.1.md

<!-- sase:referenced-by:end -->
