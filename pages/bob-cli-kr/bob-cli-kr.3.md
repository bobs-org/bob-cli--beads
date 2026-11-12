# Bead: bob-cli-kr.3 — Collapsed schema summary, chip view, and read-only Schema Card

[Bead Pages](../README.md) / [bob-cli-kr](README.md) / bob-cli-kr.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4b.linker.w0.md) · **Assignee:** `bob-cli-kr.3` · **Size:** medium
**Created:** 2026-11-12 07:00:44 EST · **Closed:** 2026-11-12 11:45:45 EST
**Plan:** [202611/album\_schema\_render\_and\_edit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_schema_render_and_edit.md)

## Description

header-reshape: reshape the album header's schema surface into a collapsed-by-default summary line, an expandable chip view with usage counts, a read-only Schema Card modal, and a YAML jump with lint marks from bob's issues.

## Notes

[2026-11-12T12:50:49Z · bob-cli-kr.3] WAITING: header-reshape cannot edit bob-plugins fragments until child epic bob-cli-k3.7.1 closes. Audited 2026-11-12: bob-cli-k3.7.1 is in_progress (assignee bob-cli-k3.7.1.land); .3 records-cards, .4 album-header, and .5 album-navigation are still in_progress. .4 depends on .3. Linked bob-plugins currently has album-data (241l/241m) and owner-cards (241o/241p/241q) only — no album header fragments yet. Will reshape whatever .4 ships (collapsed summary + chips + read-only Schema Card); will not duplicate the header.

[2026-11-12T16:44:01Z · bob-cli-kr.3--1] PROPOSED FOLLOW-UP: npm test task-tag-marks session toggle 2!==1 reproduces on this tree and is already tracked by bob-cli-kw

[2026-11-12T16:44:13Z · bob-cli-kr.3--1] PROPOSED FOLLOW-UP: 200-link Live Preview timing budgets (event-link-times 41.7ms, frees-marks 30ms, off-clock-link-chips 51.9ms vs 25ms) match the known load flakes already tracked by bob-cli-ki and bob-cli-ju

[2026-11-12T16:44:25Z · bob-cli-kr.3--1] PROPOSED FOLLOW-UP: docs-check strict Zensical warning develop/plugins/validation.md:55 -> ../bob-vim-yank-flash.md#verification is the known clean-base failure tracked by bob-cli-kk

[2026-11-12T16:44:37Z · bob-cli-kr.3--1] PROPOSED FOLLOW-UP: test-command-mode-sheet-sequence-dom fails here with CI requires Chromium on PATH or CHROMIUM_PATH; environment, not caused by header-reshape

[2026-11-12T16:45:45Z · bob-cli-kr.3--1] k3.7.1 closed done; header-reshape shipped in bob-plugins: collapsed-by-default schema summary, expandable chips with counts, read-only Schema Card, y YAML jump, lint marks, scoped record-property hide, preserved copy/breadcrumb, mobile degrade. Header tests 13/13; albums-data additive decode; npm validate 11/11; bob plugins sync copied main.js and styles.css. Known clean-base npm test/docs-check failures recorded as PROPOSED FOLLOW-UP (kw/ki/ju/kk + Chromium env).

## Dependencies

- **Depends on:** [bob-cli-k3.7.1](../bob-cli-k3/bob-cli-k3.7.1.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-kr.1](bob-cli-kr.1.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kr.4](bob-cli-kr.4.md) ◐ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-kr.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-kr.3.md) | [bob-cli-kr.3](bob-cli-kr.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f714fee`](https://github.com/bobs-org/bob-plugins/commit/f714fee11fefd5f4ac868e6a61ac8504ac377e7d) | feat(albums): reshape schema header into summary, chips, and Schema Card | [bob-cli-kr.3](bob-cli-kr.3.md) | 2026-11-12 11:47:51 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kr.3--1][1] | Need phase scope, notes, and final DECISIONS | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-kr.3.md

<!-- sase:referenced-by:end -->
