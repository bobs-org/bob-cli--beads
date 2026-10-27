# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2 — Refuse ! and N! on a generated BLOCKS line with the BLOCKS notice

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2` · **Size:** small
**Created:** 2026-10-26 08:32:07 EDT · **Closed:** 2026-10-26 08:59:42 EDT
**Plan:** [202610/backlog\_batch12\_perf\_baseline\_fakenode\_daystrip\_blocks\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch12_perf_baseline_fakenode_daystrip_blocks_notice.md)

## Description

blocks-line-bang-notice: resolve bob-cli-8z by making the bob-navigation-hotkeys ! / N! handler show BLOCKS_GENERATED_LINE_NOTICE on a generated BLOCKS line, with a test and a bob plugins sync deploy.

## Notes

[2026-10-26T12:59:42Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2--1] Implemented the generated BLOCKS-line guard for ! and N!, showing BLOCKS_GENERATED_LINE_NOTICE and making no write; added regression coverage, with ordinary link toggles preserved. Confirmed Ctrl+Shift+Enter already refuses BLOCKS lines. Rebased onto origin/master; npm run build, npm test (3,684 passed, 0 failed), and npm run validate all passed. Deployed via bob plugins sync --repo <this checkout> --no-pull -p bob-navigation-hotkeys; verified deployed main.js and manifest match source, version 2.56.4. epic-symbols was empty. Left bob-cli-8z for epic lander closure.

## Dependencies

- **Blocks:** [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.4.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d9823d1`](https://github.com/bobs-org/bob-plugins/commit/d9823d13179828cb2ea035b5e1bbb333de6e6288) | feat(bob-navigation-hotkeys): refuse generated BLOCKS transclusion | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2.md) | 2026-10-26 09:00:11 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2--1][1] | Need the phase scope, design file, and prior work notes before closing | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.2.md

<!-- sase:referenced-by:end -->
