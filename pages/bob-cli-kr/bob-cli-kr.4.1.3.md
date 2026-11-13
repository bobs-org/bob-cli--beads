# Bead: bob-cli-kr.4.1.3 — Album and record entry points and YAML return

[Bead Pages](../README.md) / [bob-cli-kr.4.1](bob-cli-kr.4.1.md) / bob-cli-kr.4.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-kr.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-kr.4.md) · **Assignee:** `bob-cli-kr.4.1.3` · **Size:** medium
**Created:** 2026-11-12 13:46:53 EST · **Closed:** 2026-11-12 15:54:29 EST
**Plan:** [202611/album\_schema\_card\_editor.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_schema_card_editor.md)

## Description

schema-entrypoints: add palette and Command Mode surface entry points, the album-only Task Card chord fallback, and a pane-scoped YAML excursion with validated Done.

## Notes

[2026-11-12T20:53:21Z · bob-cli-kr.4.1.3] PROPOSED FOLLOW-UP: Pre-existing plugin test failures unrelated to schema-entrypoints — test-navigation-period-links walkMode.links, test-navigation-bracket-repeat walkMode api versioned + null-plugin degrade, and test-ledger-tools-task-tag-marks session toggle/onload wiring all fail identically on clean base a57994a; perf 25ms-budget failures pass in isolation in both trees (full-suite load flakes).

[2026-11-12T20:53:41Z · bob-cli-kr.4.1.3] PROPOSED FOLLOW-UP: bob-cli docs:check offline-lychee failure is pre-existing on the untouched tree — gcal-notes page links to missing target/docs/site/reference/mac-capture/event-notes; unrelated to album schema docs.

[2026-11-12T20:53:55Z · bob-cli-kr.4.1.3] PROPOSED FOLLOW-UP: Plugin sync is partial for the land agent — bob-ledger-tools deployed, but bob-command-mode and bob-navigation-hotkeys refused (uncommitted builds from ws11 e0053cd-era/4d987b7 and ws14 e0053cd still deployed; protecting commits unlanded per git log HEAD..@{upstream}); no -F used per repo policy.

[2026-11-12T20:54:29Z · bob-cli-kr.4.1.3] schema-entrypoints done: Edit album schema palette command with shared album/record resolver (scalar/list/wikilink + legacy nouns; missing/cyclic/ambiguous/non-album parents teach), Command Mode Vault surface row, Ctrl+Shift+P album-only fallback after Task Card priority with no second registration, per-leaf YAML excursion with accessible Done (save + forced fresh report; schema errors keep Source mode on the diagnostic line, warnings pass, file/leaf change clears). Verified: npm run build, build:check, validate, docs:inventory:check pass; 4 new test files (18 tests) pass; related suites pass (133 tests: album header/data/update/catalog/records, sheet, parent-album-record); full test:unit 6398/6407 with only pre-existing failures (walkMode x3, task-tag session toggle x1 reproduce on clean base a57994a; perf-budget flakes pass in isolation); test:perf 5/5; docs:check lychee failure pre-existing on untouched tree. ledger-tools synced to vault; command-mode/nav-hotkeys sync refused by other checkouts' uncommitted deploys (no -F per policy) — see bead notes.

## Dependencies

- **Depends on:** [bob-cli-kr.4.1.2](bob-cli-kr.4.1.2.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kr.4.1.4](bob-cli-kr.4.1.4.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-kr.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-kr.4.1.3/README.md) | [bob-cli-kr.4.1.3](bob-cli-kr.4.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6050124`](https://github.com/bobs-org/bob-plugins/commit/60501241910be77c9cccadbbf584cd219088010c) | feat(albums): add schema entry points and YAML return | [bob-cli-kr.4.1.3](bob-cli-kr.4.1.3.md) | 2026-11-12 15:56:42 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kr.4.1.3][1] | Need full phase scope | 2 |
| read-by | [agent:bob-cli-kr.4.1.4][2] | Check deployment evidence recorded by the prior phase | 2 |
| read-by | [agent:bob-cli-kr.4.1.land][3] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-kr.4.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-kr.4.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-kr.4.1.land.md

<!-- sase:referenced-by:end -->
