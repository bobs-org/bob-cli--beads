# Bead: bob-cli-bz.1 — New Day strip look — facts line, time-mix line, no buttons, hostile-CSS preview

[Bead Pages](../README.md) / [bob-cli-bz](README.md) / bob-cli-bz.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.143](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.143.md) · **Assignee:** `bob-cli-bz.1` · **Size:** medium
**Created:** 2026-10-25 07:46:43 EDT · **Closed:** 2026-10-25 08:17:58 EDT
**Plan:** [202610/day\_strip\_under\_the\_badges.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/day_strip_under_the_badges.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:0b12378c25e4f0603aecb5ea | attached via sase artifact create --bead |
| related | file:explicit:13e66a43322e3181dfbbab51 | attached via sase artifact create --bead |
| related | file:explicit:2d117cff354bea79bb09c5f0 | attached via sase artifact create --bead |
| related | file:explicit:4f1db5badbda4a18235f6422 | attached via sase artifact create --bead |
| related | file:explicit:b882f6dde57f606f63265cd2 | attached via sase artifact create --bead |
| related | file:explicit:cd075d163c52bd9b50e3c6c7 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

strip-look: in bob-plugins' bob-ledger-tools, redesign the Day strip model, painter, and CSS into the two-line layout of the design contract. Use LABEL-value facts, then a time-mix row with `so far · HH:MM`. Drop the history marks, the collapse chevron, and `Stats ↗`. Use no `<button>` elements. Rebuild the preview matrix so it applies Obsidian's baseline button and link rules, places the strip under mock plan badges, and fails on overflow, overlap, a skeleton height mismatch, or a busted budget. Rewrite the model and painter tests, then sync.

## Notes

[2026-10-25T11:55:27Z · bob-cli-bz.1] Gap proven: rebuilt preview harness (Obsidian 30px button baseline, mock plan badges, 410/540/700 x light/dark, 13 states + Reading cell) run against the current painter FAILs with 96 failures — strip contains <button>, strip height 141.8px vs 48px budget, today/wide-values wrap to 0 fact rows at 540/700, hover/focus facts not focusable. Screenshot /tmp/bob-day-strip-gap/day-strip-410-light.png reproduces the filed issue: 30px buttons clip labels/values/marks over the mix bar and Stats link.

[2026-10-25T12:17:58Z · bob-cli-bz.1] strip-look done in bob-plugins: model renamed tiles->facts (no marks/kind/collapse, added mix.title + metaText), painter emits span[role=link] DOM with zero <button>, styles replaced with two-line Visual-contract CSS, collapse removed (registry/mount/hosts), preview harness rebuilt with Obsidian 30px-button baseline + mock plan badges + 410/540/700 x light/dark + 14 states and assertions (a)-(h), wideValues fixture added. Gap proven first (96 failures vs old painter, screenshot reproduced the 30px-button clipping). Gates: npm run build, npm test (3648 pass), npm run validate, npm run docs:check, preview matrix (84 cells, 0 failures, no overflow). bob plugins sync deployed (vault main.js/styles.css verified). 6 final PNGs attached as artifacts. Manifest untouched (mount contract unchanged, no bump). No --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-bz.2](bob-cli-bz.2.md) ✓ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-bz.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-bz.1/README.md) | [bob-cli-bz.1](bob-cli-bz.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d77503c`](https://github.com/bobs-org/bob-plugins/commit/d77503c4ebd350cec00e73b26800249ae3369b75) | feat(ledger-tools): simplify day strip to two calm label-value lines | [bob-cli-bz.1](bob-cli-bz.1.md) | 2026-10-25 08:19:42 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bz.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-bz.1/README.md

<!-- sase:referenced-by:end -->
