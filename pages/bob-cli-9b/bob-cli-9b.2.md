# Bead: bob-cli-9b.2 — Retire =x and the =\*/=! shorthands

[Bead Pages](../README.md) / [bob-cli-9b](README.md) / bob-cli-9b.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11i](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11i.md) · **Assignee:** `bob-cli-9b.2` · **Size:** medium
**Created:** 2026-10-18 14:36:56 EDT · **Closed:** 2026-10-18 15:50:32 EDT
**Plan:** [202610/bare\_x\_close.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bare_x_close.md)

## Description

retire: turn the whole-item `=x…`/`=*…`/`=!…` shapes and the link `=*`/`=!` suffix aliases into teaching errors, respell every message, help text, and comment, and migrate the bob-cli test suite to `x…`.

## Notes

[2026-10-18T19:50:18Z · bob-cli-9b.2] PROPOSED FOLLOW-UP: docs phase should quote the retired-form messages verbatim — whole-item: "`=x2!1` is retired: close the running Pomodoro with a bare `x`, without the `=`; write `x2!1`"; link alias: "`=*` is retired: a link or task close spells the `x`; write `=x*`"; `==x` now says "close it with `x`". README.md and docs/*.md still spell the old `=x` close (bob-cli-9b.3).

[2026-10-18T19:50:32Z · bob-cli-9b.2] Retired whole-item =x/=X/=x…/=x#…/=*…/=!… (teaching error naming the bare x rewrite, both parsers, chains, ==x near misses now teach x…) and link =*/=! suffix aliases (teaching error naming =x*/=x!); respelled all messages/help/comments; migrated ~1,500 test occurrences; added retired-form unit + CLI tests. Verified: just check (fmt, clippy gate, 4906 tests) green; dry-run smoke in a scratch vault of x1!2, capture-parse x2, and each retired form + rewrite.

## Dependencies

- **Depends on:** [bob-cli-9b.1](bob-cli-9b.1.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9b.3](bob-cli-9b.3.md) ✓ · ⧖ 2026-10-18
- **Blocks:** [bob-cli-9b.4](bob-cli-9b.4.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9b.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9b.2/README.md) | [bob-cli-9b.2](bob-cli-9b.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6bc432b`](https://github.com/bobs-org/bob-cli/commit/6bc432b297045b3f8b5dc4e866999a18848a35d9) | feat(capture)!: retire =x and the =\*/=! shorthands | [bob-cli-9b.2](bob-cli-9b.2.md) | 2026-10-18 15:51:21 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9b.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9b.2/README.md

<!-- sase:referenced-by:end -->
