# Bead: bob-cli-kx.2.1.2 — Positive closed-task and saved-message evidence

[Bead Pages](../README.md) / [bob-cli-kx.2.1](bob-cli-kx.2.1.md) / bob-cli-kx.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.md) · **Assignee:** `bob-cli-kx.2.1.2` · **Size:** medium
**Created:** 2026-11-12 11:37:45 EST · **Closed:** 2026-11-12 13:55:16 EST
**Plan:** [202611/gmail\_archive\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_core.md)

## Description

evidence: Add a strict archive-specific task scan including done/, reuse watch placement and identity resolution, hold merge tombstones, and capture parsed saved-message IDs. Implement section 2 and its tests.

## Notes

[2026-11-12T18:54:45Z · bob-cli-kx.2.1.2] PROPOSED FOLLOW-UP: Full just check flakes under parallel load, all green in isolation on both trees — subprocess_runner pipe-drain bounds tests (raw_run_ and run_ variants) and capture::complete_themes shell tests; themes already tracked by bob-cli-g8

[2026-11-12T18:55:16Z · bob-cli-kx.2.1.2] Section 2 evidence lands: scan_archive_evidence reuses watch placement/identity across live notes and done/, keeps unknown statuses as vetoes, holds configured merge labels plus fallback merged into and Cancel Log section tombstones, freezes sha256-pinned saved message IDs, and refuses missing/duplicate/damaged/mismatched/ambiguous/unreadable evidence. 20 new temp-vault tests (C2-C5/C17) green; all 511 gmail lib tests, 41 gmail sync/shell integration tests, and existing watch tests unchanged and green; cargo fmt clean; full just check green except load-dependent flakes recorded as PROPOSED FOLLOW-UP (themes tracked by bob-cli-g8)

## Dependencies

- **Depends on:** [bob-cli-kx.2.1.1](bob-cli-kx.2.1.1.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kx.2.1.3](bob-cli-kx.2.1.3.md) ◐ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.2/README.md) | [bob-cli-kx.2.1.2](bob-cli-kx.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`92b52e4`](https://github.com/bobs-org/bob-cli/commit/92b52e4f66d619109f9b49c37ecf24931361d972) | feat(gmail)!: add strict archive evidence scan | [bob-cli-kx.2.1.2](bob-cli-kx.2.1.2.md) | 2026-11-12 13:58:04 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.2/README.md

<!-- sase:referenced-by:end -->
