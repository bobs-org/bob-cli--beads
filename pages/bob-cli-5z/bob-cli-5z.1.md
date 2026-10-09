# Bead: bob-cli-5z.1 — Lex, parse, and describe the \`==\` token family

[Bead Pages](../README.md) / [bob-cli-5z](README.md) / bob-cli-5z.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.61.w1.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.61.w1.w0.md) · **Assignee:** `bob-cli-5z.1` · **Size:** medium
**Created:** 2026-10-09 13:24:48 EDT · **Closed:** 2026-10-09 13:50:26 EDT
**Plan:** [202610/pomodoro\_override.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_override.md)

## Description

override-grammar: teach the capture language the `==` family (`==`, `==<X>`, `==[<X>]#name`, `…~<K>`) with `=`-identical claim rules, prose protection for Obsidian highlights, teaching near-miss errors, chain support, the additive capture-parse `override: true` spec flag, editor needs, and `==#` name-completion offsets.

## Notes

[2026-10-09T17:50:14Z · bob-cli-5z.1] PROPOSED FOLLOW-UP: 9 highlights_ref::return_links lib tests fail identically on the clean base tree (verified via stash: 16 passed, 9 failed with changes stashed); unrelated to the == grammar work, needs a separate triage bead

[2026-10-09T17:50:26Z · bob-cli-5z.1] override-grammar done: == family lexes/parses with =-identical claim rules, prose protection (==foo/== foo/===/==xyz/==important==/Plan ==3 stay tasks), teaching errors (==#bugs=3->==3#bugs, ==~2#bugs->==#bugs~2, ==x/==X1/==*/==!2 never-close, ==# /==~ incompletes), chains (==#bugs +2, =x ==), additive override:true spec flag, editor needs (==# pomodoro_name, ==~ pomodoro_start_task) and ==# completion offsets, capture-parse JSON+human spell ==, docs/capture.md flag. Verified: cargo fmt clean, clippy clean, lib 286 capture_language + 27 capture_parse pass, all CLI capture suites pass (1213 cli tests), idle smoke ==3#bugs starts like =3#bugs. 9 highlights_ref::return_links failures reproduce identically on clean base (recorded as PROPOSED FOLLOW-UP). No epic-symbol leftovers.

## Dependencies

- **Blocks:** [bob-cli-5z.2](bob-cli-5z.2.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-5z.4](bob-cli-5z.4.md) ✓ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-5z.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5z.1/README.md) | [bob-cli-5z.1](bob-cli-5z.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`90214f1`](https://github.com/bobs-org/bob-cli/commit/90214f13815ee31ec5f5e8418b1ef06373e3553d) | feat(capture): lex, parse, and describe the == Pomodoro override token family | [bob-cli-5z.1](bob-cli-5z.1.md) | 2026-10-09 13:51:27 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5z.1][1] | Need phase scope notes history | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-5z.1/README.md

<!-- sase:referenced-by:end -->
