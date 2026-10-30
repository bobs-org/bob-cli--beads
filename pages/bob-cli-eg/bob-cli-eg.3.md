# Bead: bob-cli-eg.3 — Guided setup, account choice, self-healing check, and summary

[Bead Pages](../README.md) / [bob-cli-eg](README.md) / bob-cli-eg.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.165](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.165.md) · **Assignee:** `bob-cli-eg.3` · **Size:** medium
**Created:** 2026-10-30 09:42:40 EDT · **Closed:** 2026-10-30 12:13:53 EDT
**Plan:** [202610/gcal\_login\_redesign.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gcal_login_redesign.md)

## Description

experience: guided client setup with ~/Downloads discovery, the account picker and shared resolver, self-healing stale grants, the in-place Calendar-API retry, the summary, additive JSON fields, and doctor alignment.

## Notes

[2026-10-30T16:02:15Z · bob-cli-eg.3--1] PROPOSED FOLLOW-UP: Resolve the prose-table snapshot layout regression already tracked by bob-cli-87 — the exact table_layout_records_prose_tables_on_snapshot_route test fails on clean base 3c9536a7 at profile.rs:2070 with “frontmatter grid keeps the prose table a grid”; bob-cli-87 note #13 records the same failure on the current tree. No dedicated task bead matches this test.

[2026-10-30T16:13:53Z · bob-cli-eg.3--1] Completed guided gcal client setup, account resolution, stale-grant recovery, API retry, summary, additive JSON fields, and doctor alignment. `sase tool run check` passed formatting and clippy and all test targets except the exact table_layout_records_prose_tables_on_snapshot_route failure at profile.rs:2070. That same failure reproduces on clean base 3c9536a7 and is recorded as a PROPOSED FOLLOW-UP pointing to bob-cli-87. `sase bead epic-symbols bob-cli-eg.3` reported no leftovers.

## Dependencies

- **Depends on:** [bob-cli-eg.2](bob-cli-eg.2.md) ✓ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-eg.4](bob-cli-eg.4.md) ◐ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-eg.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-eg.3.md) | [bob-cli-eg.3](bob-cli-eg.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`18d3f97`](https://github.com/bobs-org/bob-cli/commit/18d3f97a36059ae331d4529f380c847e3dcab5d1) | feat(gcal): guide Calendar login setup and recovery | [bob-cli-eg.3](bob-cli-eg.3.md) | 2026-10-30 12:15:22 EDT |
