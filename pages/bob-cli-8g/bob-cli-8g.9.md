# Bead: bob-cli-8g.9 — Article reading look and live section signals

[Bead Pages](../README.md) / [bob-cli-8g](README.md) / bob-cli-8g.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1o.linker.w0.md) · **Assignee:** `bob-cli-8g.9` · **Size:** medium
**Created:** 2026-10-16 10:53:04 EDT · **Closed:** 2026-10-16 15:59:06 EDT
**Plan:** [202610/article\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/article_notes.md)

## Description

look: scoped article typography, muted tabular section numbers in Live Preview and Reading view, hanging numbers on wide panes, debounced stale-number hints, and the section status-bar item.

## Notes

[2026-10-16T19:58:48Z · bob-cli-8g.9] PROPOSED FOLLOW-UP: npm test in bob-plugins still fails identically on clean origin/master — four unblocked-glyph cases (bob-cli-6v), Keep counts once (bob-cli-6w), forward-promotion BLOCKS re-key (bob-cli-7i), and occasional stage-ranker 16ms flake (bob-cli-3w). Article look tests and validate pass.

[2026-10-16T19:59:06Z · bob-cli-8g.9] look complete in bob-plugins bob-articles 0.2.0: scoped .bob-article typography (40rem measure, serif/theme setting, muted tabular .bob-secno, hanging numbers via container query on wide Reading panes, inline in LP/narrow/print), Live Preview CM marks from outline line+written mapped through txs, Reading post-processor wrap, 400ms stale-hint dry-run (desktop, IME skip, one in-flight, drop old versions, is-stale tooltip), § status bar from computed numbers. Verified: 17 article tests (decoration ranges, section-at-line, debounce/in-flight, wrapping), npm run validate, bob plugins sync --no-pull -p bob-articles --repo <linked>, epic-symbols none. Reload Obsidian to see the look. Live light/dark/narrow/200%/PDF visual pass not available in this agent. Pre-existing npm test failures recorded as PROPOSED FOLLOW-UP (bob-cli-6v/6w/7i/3w).

## Dependencies

- **Depends on:** [bob-cli-8g.8](bob-cli-8g.8.md) ✓ · ⧖ 2026-10-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-8g.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8g.9/README.md) | [bob-cli-8g.9](bob-cli-8g.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@5bc2d9d`](https://github.com/bobs-org/bob-plugins/commit/5bc2d9d1676237f2185a90d4e578e4838ca0578d) | feat(bob-articles): add reading look and live section signals | [bob-cli-8g.9](bob-cli-8g.9.md) | 2026-10-16 16:01:10 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8g.9][1] | Need phase notes and remaining work from earlier agents | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-8g.9/README.md

<!-- sase:referenced-by:end -->
