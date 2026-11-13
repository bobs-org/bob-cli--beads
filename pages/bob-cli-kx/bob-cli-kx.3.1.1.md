# Bead: bob-cli-kx.3.1.1 — Project authoritative archive receipts for readers

[Bead Pages](../README.md) / [bob-cli-kx.3.1](bob-cli-kx.3.1.md) / bob-cli-kx.3.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.3.md) · **Assignee:** `bob-cli-kx.3.1.1` · **Size:** medium
**Created:** 2026-11-13 08:02:47 EST · **Closed:** 2026-11-13 08:41:27 EST
**Plan:** [202611/gmail\_archive\_receipts.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_receipts.md)

## Description

receipt_projection: add shared body-free receipt projections, offline list JSON, and recent_archive sync JSON with deterministic timezone and ownership semantics.

## Notes

[2026-11-13T13:41:02Z · bob-cli-kx.3.1.1] PROPOSED FOLLOW-UP: Resolve the existing docs-check offline lychee failure for docs/gcal-notes.md:22 -> ../reference/mac-capture/event-notes.md (already tracked by bob-cli-l7). This tree reached link checking and reported the missing target; clean-base just docs-check stops earlier on existing reference word budgets of 6136 and 6055, so it could not reach lychee.

[2026-11-13T13:41:27Z · bob-cli-kx.3.1.1] Implemented body-free archive receipt projections, offline list JSON diagnostics, and timezone-safe recent_archive sync JSON with account/thread/generation ownership semantics. Verified cargo check, formatting, DST and generation projection tests, gmail_shell list (13), gmail_archive_apply (30), gmail_archive_preview (4), gmail_sync (41) plus unsafe-history case. docs-check lint/build/published URL checks passed; offline lychee hits existing bob-cli-l7 issue, recorded as a proposed follow-up. Clean-base docs-check stops earlier on pre-existing reference word budgets.

## Dependencies

- **Blocks:** [bob-cli-kx.3.1.2](bob-cli-kx.3.1.2.md) ◐ · ⧖ 2026-11-13

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.3.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.3.1.1/README.md) | [bob-cli-kx.3.1.1](bob-cli-kx.3.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c994cfb`](https://github.com/bobs-org/bob-cli/commit/c994cfbd1d0d0a8271b5b27c3db5b6d6d73b0795) | feat(gmail): project archive receipts for readers | [bob-cli-kx.3.1.1](bob-cli-kx.3.1.1.md) | 2026-11-13 08:43:19 EST |
