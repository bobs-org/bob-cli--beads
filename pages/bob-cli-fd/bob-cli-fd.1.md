# Bead: bob-cli-fd.1 — Bob Mac Capture strips both stamp forms

[Bead Pages](../README.md) / [bob-cli-fd](README.md) / bob-cli-fd.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c3.md) · **Assignee:** `bob-cli-fd.1` · **Size:** small
**Created:** 2026-11-01 15:12:25 EST · **Closed:** 2026-11-01 15:42:02 EST
**Plan:** [202611/work\_log\_timestamps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/work_log_timestamps.md)

## Description

mac-strip: make the close card's Work Log stripper accept stamped and date-only entries strictly, with vector tests and the previews doc, before bob starts emitting stamps.

## Notes

[2026-11-01T20:42:02Z · bob-cli-fd.1] Mac close card stripper renamed to strippedWorkLogStamp; strips YYYY-MM-DD and YYYY-MM-DD HH:MM only (digit positions). Vector tests, stamped decode preview, and capture-previews.md passed just docs-check and athena just portable-check (1917 tests, 0 failures). Did not touch Sources/BobMacCapture*.

## Dependencies

- **Blocks:** [bob-cli-fd.3](bob-cli-fd.3.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fd.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fd.1/README.md) | [bob-cli-fd.1](bob-cli-fd.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@01c753b`](https://github.com/bobs-org/bob-mac-capture/commit/01c753b0e6e045a0cc69b3d3f51302b8423b7e55) | feat(mac-capture): strip stamped Work Log dates on the close card | [bob-cli-fd.1](bob-cli-fd.1.md) | 2026-11-01 15:43:29 EST |
