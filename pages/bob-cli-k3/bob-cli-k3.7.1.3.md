# Bead: bob-cli-k3.7.1.3 — Record index cards with folds and date chips

[Bead Pages](../README.md) / [bob-cli-k3.7.1](bob-cli-k3.7.1.md) / bob-cli-k3.7.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-k3.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.7.md) · **Assignee:** `bob-cli-k3.7.1.3` · **Size:** medium
**Created:** 2026-11-11 23:10:17 EST · **Closed:** 2026-11-12 08:46:23 EST
**Plan:** [202611/album\_plugin\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_plugin_ui.md)

## Description

records-cards: implement styled records tally, view-only folding after the first group above twelve rows, record date chips, refresh-safe view state, group-jump integration, and renderer tests.

## Notes

[2026-11-12T13:46:01Z · bob-cli-k3.7.1.3] PROPOSED FOLLOW-UP: Fix baseline strict docs links — BOB_CLI_DIR=<this checkout> npm run docs:check still fails the Bob CLI Zensical build at develop/plugins/validation.md:55 because ../bob-vim-yank-flash.md#verification does not exist. Same clean-base failure recorded on bob-cli-k3.7.1.1/.2 and tracked by bob-cli-kk. Outside records-cards; does not block close.

[2026-11-12T13:46:08Z · bob-cli-k3.7.1.3] PROPOSED FOLLOW-UP: Corroborate baseline ledger test lifecycle and task-tag wiring — npm test hangs because files such as test-ledger-tools-dashboard-parity.cjs, date-marks, day-strip-hosts, and day-strip-lanes leave open handles (timeout 20s after TAP, 0% CPU on epoll). node --test --test-force-exit --test-concurrency=4 completes 6251 tests: 6250 pass, sole failure test-ledger-tools-task-tag-marks.cjs:922 session toggle and onload wiring (2 !== 1). Identical to bob-cli-k3.7.1.2 notes #4/#1; not caused by records-cards.

[2026-11-12T13:46:23Z · bob-cli-k3.7.1.3] Implemented records-cards in bob-plugins: 241r/s/t fragments, Reading/Live Preview paint, view-only folds (first group open; later groups fold iff heading count > 12), WeakMap pane fold state, albumRevealRecordGroup destination-pane expand, visited/watched_on age chips from metadataCache, chrome-skip heading parse, CSS, docs/albums.md, 11 renderer tests. Verified: 11/11 records tests; 34/34 album catalog+data; npm run validate and docs:inventory:check pass; test:perf 5/5; force-exit unit suite 6250/6251 (sole failure is baseline task-tag-marks.cjs:922, same as k3.7.1.2). Fast-forwarded to origin/master (a6f4b03 landed), then descendant bob plugins sync --no-pull -p bob-ledger-tools copied main.js/styles.css without -F. No epic-symbol leftovers. Parent epic left open. Pre-existing docs-check Zensical and test-lifecycle hangs recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-k3.7.1.2](bob-cli-k3.7.1.2.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-k3.7.1.4](bob-cli-k3.7.1.4.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.7.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.7.1.3/README.md) | [bob-cli-k3.7.1.3](bob-cli-k3.7.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ed5e648`](https://github.com/bobs-org/bob-plugins/commit/ed5e64814b1e80f0cbe9ecb8794057b1d884c6de) | feat(ledger-tools): paint record index cards with folds and date chips | [bob-cli-k3.7.1.3](bob-cli-k3.7.1.3.md) | 2026-11-12 08:48:00 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.4b.mus][1] | research record frontmatter Obsidian rendering | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.mus/README.md

<!-- sase:referenced-by:end -->
