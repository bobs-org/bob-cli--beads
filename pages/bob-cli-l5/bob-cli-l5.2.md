# Bead: bob-cli-l5.2 — Unacked row tag reconciliation and sync/list surfaces

[Bead Pages](../README.md) / [bob-cli-l5](README.md) / bob-cli-l5.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1c2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1c2.md) · **Assignee:** `bob-cli-l5.2` · **Size:** medium
**Created:** 2026-11-12 16:39:08 EST · **Closed:** 2026-11-12 20:16:25 EST
**Plan:** [202611/gcal\_external\_event\_ack.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_external_event_ack.md)

## Description

tag: teach split_suffix the warning-tag marker, reconcile the tag through the want/present/last table in the sync planner (including the delete-the-tag inferred ack), journal the additive unacked row field, and surface warnings in sync and list human and JSON output.

## Notes

[2026-11-13T01:15:47Z · bob-cli-l5.2] PROPOSED FOLLOW-UP: lib test sync_args_read_last_n_days_aliases_and_default_to_none fails on clean base too (expects ["today","tomorrow"], gets ["tomorrow"]) — unrelated to ack work, needs owner triage

[2026-11-13T01:15:58Z · bob-cli-l5.2] PROPOSED FOLLOW-UP: just docs-check fails on clean base (sase/memory/glossary/event-ack.md has no front matter, filed by l5.1) — likely belongs to the docs phase l5.4 which owns the glossary strand via mem_glossary_term

[2026-11-13T01:16:08Z · bob-cli-l5.2] PROPOSED FOLLOW-UP: 44 workspace test failures (capture/bank/albums/etc.) reproduce identically on the clean base tree — environment or pre-existing breakage outside gcal scope, needs owner triage

[2026-11-13T01:16:25Z · bob-cli-l5.2] Tag phase done: split_suffix marker + add/strip helpers (lifecycle.rs); additive unacked journal field + AckStatus/status_for/ack JSON (journal.rs); render gate for open unacked rows; want/present/last reconcile with inferred ack (via row), close/cancel lifts, off-mode removal (plan.rs/refile.rs); sync human marks + footer hint + counts.unacked + row ack objects; list dim marks + footer + counts + row ack objects; note preview anticipates the save-ack. Verified: new unit tests (lifecycle marker/round-trip/escape-collision, journal flag round-trip + status states) and 10 sync + 1 lifecycle + 1 list integration tests cover the full table (add/remove/infer/hand-close/Bryan-tag/off/kept-edit/no-false-badges/born-done/context/tombstone/revive/-F/close/cancel/JSON); full gcal suites green (sync 94, lifecycle 45, list 14, notes 21, note_cli 39, cli 6, lib gcal 282). Failing sets identical to clean base (46 pre-existing incl. 1 gcal cli day-alias + docs-check strand front matter, filed as PROPOSED FOLLOW-UP notes).

## Dependencies

- **Depends on:** [bob-cli-l5.1](bob-cli-l5.1.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-l5.3](bob-cli-l5.3.md) ◐ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-l5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.2/README.md) | [bob-cli-l5.2](bob-cli-l5.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8adc1be`](https://github.com/bobs-org/bob-cli/commit/8adc1bee41985181660580164b6cad9f57fab673) | feat(gcal): reconcile the unacked row tag and surface ack warnings | [bob-cli-l5.2](bob-cli-l5.2.md) | 2026-11-12 20:22:12 EST |
