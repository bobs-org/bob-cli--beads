# Bead: bob-cli-eg.2 — Bob-owned sign-in through gog's two-step remote flow

[Bead Pages](../README.md) / [bob-cli-eg](README.md) / bob-cli-eg.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.165](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.165.md) · **Assignee:** `bob-cli-eg.2` · **Size:** medium
**Created:** 2026-10-30 09:42:40 EDT · **Closed:** 2026-10-30 11:16:13 EDT
**Plan:** [202610/gcal\_login\_redesign.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gcal_login_redesign.md)

## Description

signin: replace the inherited-stdio `gog auth add` with gog's remote step 1/2, a loopback listener plus browser opener, a validated paste prompt, flow auto-selection, a success page, and the new step renderer.

## Notes

[2026-10-30T15:15:58Z · bob-cli-eg.2--1] PROPOSED FOLLOW-UP: Pre-existing lib failure table_layout_records_prose_tables_on_snapshot_route fails identically on clean HEAD 2ca76ca0 (frontmatter grid keeps the prose table a grid) — already recorded on bob-cli-eg.1

[2026-10-30T15:16:13Z · bob-cli-eg.2--1] Implemented bob-owned sign-in: gog remote step 1/2, loopback browser listener plus opener, validated paste prompt, flow auto-selection, HTML outcome pages, stderr step renderer, inherit_stdio removed. Verified: gcal_auth 35 passed (browser, paste, SSH, denied, stale state); just check compiled/clipped clean with 4086 lib tests passing. Remaining table_layout_records_prose_tables_on_snapshot_route failure reproduces on clean HEAD 2ca76ca0 (same as bob-cli-eg.1) and is recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-eg.1](bob-cli-eg.1.md) ✓ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-eg.3](bob-cli-eg.3.md) ◐ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-eg.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-eg.2.md) | [bob-cli-eg.2](bob-cli-eg.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`00c44ab`](https://github.com/bobs-org/bob-cli/commit/00c44ab4b481ecc00f4a882ae873a6fc6d28fde6) | feat(gcal): bob-owned login sign-in with browser and paste flows | [bob-cli-eg.2](bob-cli-eg.2.md) | 2026-10-30 11:17:32 EDT |
