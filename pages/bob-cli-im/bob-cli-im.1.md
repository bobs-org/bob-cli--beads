# Bead: bob-cli-im.1 — Signed \`\<X\>\` grammar, later clock, contracts, and link starts in bob-cli

[Bead Pages](../README.md) / [bob-cli-im](README.md) / bob-cli-im.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5x.linker.w0.md) · **Assignee:** `bob-cli-im.1` · **Size:** medium
**Created:** 2026-11-08 05:50:21 EST · **Closed:** 2026-11-08 06:54:11 EST
**Plan:** [202611/start\_timing\_later\_offset.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/start_timing_later_offset.md)

## Description

signed_timing: extend `<X>` from `[D][-[N]]` to `[D][±[N]]` in bob-cli. Add `later_units` to the start spec and summary, move the start later in `start_block_minute`, refuse `+0` and two signs, accept every leading-`+` form (`=+3`, `=3+2`, `=+fix`, `=3+1#deep-work`, `@foo:bar=+3`, `^foo:bar=3+`), carry the sign into fit drafts and the human parse line, teach `x=3+`/`x=+`, bump the grammar revision, extend the shared MEET vectors, and document it. Trailing `+` after a bare name stays a name byte until bare_plus.

## Notes

[2026-11-08T11:54:11Z · bob-cli-im.1] Implemented signed later Pomodoro offsets and grammar 17 across parsing, capture, links, MEET timing, JSON and human output, and docs; verified just check, just docs-gen, and just docs-check.

## Dependencies

- **Blocks:** [bob-cli-im.2](bob-cli-im.2.md) ◐ · ⧖ 2026-11-08
- **Blocks:** [bob-cli-im.4](bob-cli-im.4.md) ✓ · ⧖ 2026-11-08

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-im.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-im.1/README.md) | [bob-cli-im.1](bob-cli-im.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f9601b7`](https://github.com/bobs-org/bob-cli/commit/f9601b704b23f6857cb26cef45a2c870afbdd1b6) | feat(capture): add signed later Pomodoro starts | [bob-cli-im.1](bob-cli-im.1.md) | 2026-11-08 06:55:19 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-im.1][1] | Need the phase scope, design file, prior notes, and DECISIONS before completing the assigned work | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-im.1/README.md

<!-- sase:referenced-by:end -->
