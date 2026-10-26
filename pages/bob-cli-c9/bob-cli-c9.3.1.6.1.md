# Bead: bob-cli-c9.3.1.6.1 — Locked reread recheck for audio units, full scan, and previews

[Bead Pages](../README.md) / [bob-cli-c9.3.1.6](bob-cli-c9.3.1.6.md) / bob-cli-c9.3.1.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.land.md) · **Assignee:** `bob-cli-c9.3.1.6.1` · **Size:** small
**Created:** 2026-10-25 19:48:33 EDT · **Closed:** 2026-10-25 20:00:24 EDT
**Plan:** [202610/ref\_reread\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_reread_landing_fixes.md)

## Description

intake_recheck: stop the locked recheck from refusing audio attach onto __vN readings, add the whole-bundle recheck to the full-scan xlib move path, and make dry-run previews agree.

## Notes

[2026-10-26T00:00:17Z · bob-cli-c9.3.1.6.1] Verified locked reread rechecks now exclude Audio units, the shared whole-bundle occupancy helper covers full-scan queued PDF planning and intake previews, and full scan aborts before any move on a collision. Commands: cargo fmt --all; cargo fmt --check; cargo test --test cli full_scan_aborts_before_moving_any_queued_reread_with_an_occupant (pass); cargo test --test cli queued_reread_occupant (pass); cargo test --test cli intake_only_attaches_audio_to_an_existing_reread (pass); cargo test --test cli full_scan_files_queued_reread_with_lineage (pass); just lint (pass); git diff --check (pass). Epic symbols: `sase bead epic-symbols bob-cli-c9.3.1.6.1` reported no --epic-symbol entries.

[2026-10-26T00:00:24Z · bob-cli-c9.3.1.6.1] Implemented shared locked reread occupancy recheck for PDF intake, full-scan xlib planning, and dry-run previews; audio attach bypasses the PDF birth check. Verified full-scan abort preserves every queued source on collision. Passing: cargo fmt --check; just lint; focused CLI tests for full-scan collision, intake preview collision, reread audio attach, and existing full-scan reread lineage. No --epic-symbol entries for bob-cli-c9.3.1.6.1. reported no --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-c9.3.1.6.2](bob-cli-c9.3.1.6.2.md) ◐ · ⧖ 2026-10-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.6.1/README.md) | [bob-cli-c9.3.1.6.1](bob-cli-c9.3.1.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c192014`](https://github.com/bobs-org/bob-cli/commit/c192014eeede15b4a87079787ade257372ec575c) | fix(ref): recheck locked reread intake occupancy | [bob-cli-c9.3.1.6.1](bob-cli-c9.3.1.6.1.md) | 2026-10-25 20:00:58 EDT |
