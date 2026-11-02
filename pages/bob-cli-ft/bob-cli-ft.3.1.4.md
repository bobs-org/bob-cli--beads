# Bead: bob-cli-ft.3.1.4 — Real-Obsidian harness, screenshots, and rendering integration

[Bead Pages](../README.md) / [bob-cli-ft.3.1](bob-cli-ft.3.1.md) / bob-cli-ft.3.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ft.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ft.3.md) · **Assignee:** `bob-cli-ft.3.1.4` · **Size:** medium
**Created:** 2026-11-02 07:34:44 EST · **Closed:** 2026-11-02 10:14:25 EST
**Plan:** [202611/block\_marks\_editor.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/block_marks_editor.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:1e6f25d72fdcdf875563ea3f | attached via sase artifact create --bead |
| related | file:explicit:5d9f761d447fd13b27f53432 | attached via sase artifact create --bead |
| related | file:explicit:64a3d017b3e42416ee68330b | attached via sase artifact create --bead |
| related | file:explicit:71ebe3b9f364e6676b19c7d2 | attached via sase artifact create --bead |
| related | file:explicit:7eed42958ba72df8a7db81d1 | attached via sase artifact create --bead |
| related | file:explicit:acb89c2e675f266bfe609510 | attached via sase artifact create --bead |
| related | file:explicit:c0c2f36fd16a819537d7f00e | attached via sase artifact create --bead |
| related | file:explicit:ee8f976abf31be54c7612c4b | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

obsidian_e2e: add an isolated scratch-vault CDP harness and offline self-test, exercise BM source-note vectors in both themes and views, verify real hover/click/toggle behavior, inspect screenshots against the accepted mockup, and fix integration defects within this rendering scope.

## Notes

[2026-11-02T15:02:19Z · bob-cli-ft.3.1.4] PROPOSED FOLLOW-UP: 5 bob-plugins node failures reproduce identically on clean base 2ead3a8 (stash verified) and are unrelated to block marks: test-ledger-tools-freshness-namespace "reload event fires only when the due key set changes", test-ledger-tools-keep-inbox "forced check feedback follows the bob refresh result", test-ledger-tools-note-ready "startup storm is linear", test-ledger-tools-relation-index "relationIndex registers after layout-ready", test-navigation-hotkeys-schedule-work-log "future scheduling on Pending marks Blocked". Repro: npm --prefix <bob-plugins> test on base shows the same 5; plus test-block-id-prompt-task-wikilink-index-performance "warm snapshot 50ms" flakes only under full-suite load (passes in isolation on both trees). Witness: .tmp-bm-e2e/npm-test.log (6 fail/5076) and base rerun (same 5).

[2026-11-02T15:14:25Z · bob-cli-ft.3.1.4] obsidian_e2e done: real-Obsidian harness scripts/obsidian-block-marks-e2e.cjs + offline wrapper (npm test) pass; full run exit 0 with all BM vectors marked in Live Preview+reading x light/dark, pips, nested independence, embeds/hover/Dataview evidence, toggle removal+restoration with unchanged row height, identical click status on/off, and real hover tooltip text. Fixed 2 integration defects: shared fence guard now matches live hmd-codeblock (pinned by editor test), fixture uses dataview taskFormat so Tasks parses [id::]. Screenshots reviewed vs mockup; report+screens stored as artifacts on this bead (file:explicit:ee8f976abf31be54c7612c4b + 7 shots). Contract docs/blocked-marks.md updated (fence guard, verified vectors). Gates: build:check, validate, docs:check, just docs-check pass; full npm test 5070/5076 with 5 pre-existing base-identical failures + 1 load flake recorded as PROPOSED FOLLOW-UP (base 2ead3a8 verified via stash). bob plugins sync clean; vault still runs landed 1.89.0 — workspace 1.90.0 deployment belongs to the land agent stitch+sync.

## Dependencies

- **Depends on:** [bob-cli-ft.3.1.3](bob-cli-ft.3.1.3.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.4/README.md) | [bob-cli-ft.3.1.4](bob-cli-ft.3.1.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a7931a6`](https://github.com/bobs-org/bob-cli/commit/a7931a649ef2e73e17b44a37bbadd11ae6581664) | docs(blocked-marks): record obsidian\_e2e verification and fence-guard mechanism | [bob-cli-ft.3.1.4](bob-cli-ft.3.1.4.md) | 2026-11-02 10:16:15 EST |
| bob-plugins | [`bob-plugins@bded172`](https://github.com/bobs-org/bob-plugins/commit/bded17231b45afeaf83f0d5b8164fba109f91226) | feat(block-marks): add real-Obsidian e2e harness and fix fenced-code guard | [bob-cli-ft.3.1.4](bob-cli-ft.3.1.4.md) | 2026-11-02 10:16:37 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ft.3.1.4][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.3.1.4/README.md

<!-- sase:referenced-by:end -->
