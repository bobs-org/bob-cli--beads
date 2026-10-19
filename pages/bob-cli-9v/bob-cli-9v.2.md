# Bead: bob-cli-9v.2 — Near-full-screen panel, wide inspector, larger thumbnail

[Bead Pages](../README.md) / [bob-cli-9v](README.md) / bob-cli-9v.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11v.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11v.w0.md) · **Size:** medium
**Created:** 2026-10-19 12:32:44 EDT · **Closed:** 2026-10-19 13:56:18 EDT
**Plan:** [202610/refs\_reading\_room.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_reading_room.md)

## Description

big-panel: wire the new geometry into the panel and column split, add the wide inspector layout (hero with a 150 × 194 thumbnail beside the facts, readable 720 pt column, body typography), render thumbnails at the new size behind a versioned cache, let Ctrl+D reveal while the disclosure row is visible, and refresh fixtures and README.

## Notes

[2026-10-19T17:56:18Z · bob-cli-9v.2--3] big-panel phase done: portable-check green incl lint (1431 tests, 0 failures); mac scratch bundle.sh plus just typecheck-tests GREEN on fresh dir /tmp/bobmac-bigpanel.fix1; new tests: containsRow units, hosted disclosure-reveal test, v2-cache tests, 1344-pt fixtures; XCTest/CI runs only on origin push so land step must check CI and review new 1344-pt PNGs in render-fixtures artifact

## Dependencies

- **Depends on:** [bob-cli-9v.1](bob-cli-9v.1.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-9v.3](bob-cli-9v.3.md) ◐ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9v.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9v.2.md) | [bob-cli-9v.2](bob-cli-9v.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@1d7242a`](https://github.com/bobs-org/bob-mac-capture/commit/1d7242a7295d3d0e792e69994b992ec795d029da) | feat(refs): near-full-screen panel, wide inspector, larger thumbnails | [bob-cli-9v.2](bob-cli-9v.2.md) | 2026-10-19 13:57:37 EDT |
