# Bead: bob-cli-ji.7.1.1 — Complete event-note fixtures and the Swift process contract

[Bead Pages](../README.md) / [bob-cli-ji.7.1](bob-cli-ji.7.1.md) / bob-cli-ji.7.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.md) · **Assignee:** `bob-cli-ji.7.1.1` · **Size:** medium
**Created:** 2026-11-10 10:29:45 EST · **Closed:** 2026-11-10 11:20:21 EST
**Plan:** [202611/mac\_event\_note\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_event_note_mode.md)

## Description

contract: produce full normalized bob-cli JSON fixtures, expose structured effective buffer reasons and effective fields on show, then add typed CaptureCore responses and isolated gcal-note client methods using decodeReport. Copy the fixtures into fake-bob and cover exit-2 reports, compatibility, argv, and overlapping UTF-8 spans. Read the Contract section.

## Notes

[2026-11-10T16:05:48Z · bob-cli-ji.7.1.1] PROPOSED FOLLOW-UP: just docs-check still fails on the clean base with six unchanged reference pages over the 6000-word cap (json-outputs 6050, Mac Capture panel/previews/keyboard/protocol, and bob-ledger-tools); reproduced after restoring docs/gcal-notes.md and already tracked by bob-cli-ji.2 note #1.

[2026-11-10T16:20:21Z · bob-cli-ji.7.1.1] Implemented Bob's effective buffer-reason JSON and documented it; added normalized full JSON contract fixtures and occurrence/series precedence coverage. Added the typed Mac Capture gcal-note wire models and Bob process operations with fake-bob fixtures. Verified cargo fmt --check, cargo test --test gcal_note_cli (15 passed), and just portable-check on Athena (2,419 passed, 1 skipped). epic-symbols had no leftovers. just docs-check still has the six clean-base reference word-budget failures already tracked by bob-cli-ji.2 note #1; macOS-only targets could not run because the Mac host is offline.

## Dependencies

- **Blocks:** [bob-cli-ji.7.1.2](bob-cli-ji.7.1.2.md) ◐ · ⧖ 2026-11-10
- **Blocks:** [bob-cli-ji.7.1.3](bob-cli-ji.7.1.3.md) ◐ · ⧖ 2026-11-10

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.7.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.7.1.1/README.md) | [bob-cli-ji.7.1.1](bob-cli-ji.7.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8e2b93c`](https://github.com/bobs-org/bob-cli/commit/8e2b93c7d0ed6bee06cb5b19b5ce95bc8f09115e) | feat(gcal): expose effective buffer reasons in note JSON | [bob-cli-ji.7.1.1](bob-cli-ji.7.1.1.md) | 2026-11-10 11:21:54 EST |
