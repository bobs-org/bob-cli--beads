# Bead: bob-cli-iz.3 — Name every skipped event and stop re-tombstoning

[Bead Pages](../README.md) / [bob-cli-iz](README.md) / bob-cli-iz.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1aa](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1aa.md) · **Assignee:** `bob-cli-iz.3` · **Size:** medium
**Created:** 2026-11-09 07:12:09 EST · **Closed:** 2026-11-09 08:36:29 EST
**Plan:** [202611/gcal\_sync\_race\_force\_and\_skip\_reasons.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_sync_race_force_and_skip_reasons.md)

## Description

skip_reasons: bob-cli. One shared skip vocabulary for sync and list; sync lists every left-out event with reason and hint, reports in-sync counts, stops re-tombstoning gone rows every run, and revives a tombstoned row pasted back. See plan section "Phase skip_reasons".

## Notes

[2026-11-09T13:36:29Z · bob-cli-iz.3] skip_reasons landed: new src/native/gcal/skip.rs shared vocabulary (declined, cancelled, awaiting_reply, event_type, outside_day, invalid_time, removed_by_you, removed_in_google) used by sync and list; journal fold gains gone_at/gone_reason and a later gcal.row revives a tombstone; planner skips a gone row whose line is still missing (no re-tombstone, rerun unchanged, appends nothing) and adopts a pasted-back row; sync lists every left-out event (human + JSON skipped[], in_sync, rows[].detail) with '· N in sync · M skipped' on every summary form; list VAULT/skip/footer share the words; docs/gcal.md updated. Verified: cargo fmt --check, cargo test --lib (5973 pass), all tests/gcal_*.rs suites pass, just docs-check passes. Note: the removed_by_you hint names 'bob gcal sync -F' per the plan; the flag itself lands in bob-cli-iz.4. Also fixed a latent list bug where URL-less context rows read 'removed by you'.

## Dependencies

- **Depends on:** [bob-cli-iz.1](bob-cli-iz.1.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-iz.4](bob-cli-iz.4.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-iz.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-iz.3/README.md) | [bob-cli-iz.3](bob-cli-iz.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a449193`](https://github.com/bobs-org/bob-cli/commit/a449193baa2ecd454b62e924e291d0745fbad614) | feat(gcal): name every skipped event and stop re-tombstoning | [bob-cli-iz.3](bob-cli-iz.3.md) | 2026-11-09 08:37:19 EST |
