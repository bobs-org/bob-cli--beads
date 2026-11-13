# Bead: bob-cli-l5.3.1.4 — Finish stale notices, doctor diagnostics, and CLI verification

[Bead Pages](../README.md) / [bob-cli-l5.3.1](bob-cli-l5.3.1.md) / bob-cli-l5.3.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-l5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-l5.3.md) · **Assignee:** `bob-cli-l5.3.1.4` · **Size:** medium
**Created:** 2026-11-12 20:43:26 EST · **Closed:** 2026-11-13 02:05:44 EST
**Plan:** [202611/gcal\_ack\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_ack_cli.md)

## Description

diagnostics: integrate event-scope stale notices into gcal list and the shared JSON surfaces, add doctor ack diagnostics, complete help and generated CLI references, and verify the full bob-cli-l5.3 acceptance matrix. Leave enclosing-bead closure to this child epic's land agent.

## Notes

[2026-11-13T06:06:21Z · bob-cli-l5.3.1.4] PROPOSED FOLLOW-UP: Repair glossary:event-ack front matter in docs phase bob-cli-l5.4 — both just docs-gen and just docs-check fail during bob-docs generated drift with “memory strand has no front matter”; reproduced on clean base 307616aea9167577805a8e525dc4dd0ea0f9190d (owner: bob-cli-l5.4). This phase has no memory-edit authorization.

[2026-11-13T06:25:53Z · bob-cli-l5.3.1.4--1] PROPOSED FOLLOW-UP: Fix the pre-existing sync day-alias unit failure. Command: cargo test --lib native::gcal (also reproduced with cargo test --lib native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none); failing test native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none at src/native/gcal/cli.rs:1032 reports expected ["today", "tomorrow"], got ["tomorrow"]. Reproduced on clean base 307616aea9167577805a8e525dc4dd0ea0f9190d. Existing owner: bob-cli-l2, corroborated by bob-cli-l5.3.1.3 note #1 and bob-cli-kx.2.1.7 note #2. This failure predates diagnostics and does not block this phase.

[2026-11-13T07:05:44Z · bob-cli-l5.3.1.4--3] Verification: fresh-target just all ran 6861 passed, 3 failed, 3 ignored. The native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none failure is the documented clean-base failure assigned to bob-cli-l2 (base 307616aea9167577805a8e525dc4dd0ea0f9190d). The two subprocess_runner pipe-drain failures passed in an isolated rerun (6/6) and a full library rerun (6863 passed, only the documented gcal failure, 3 ignored). epic-symbols reported no entries. glossary:event-ack docs-gen/docs-check remains assigned to bob-cli-l5.4.

## Dependencies

- **Depends on:** [bob-cli-l5.3.1.3](bob-cli-l5.3.1.3.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-l5.3.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-l5.3.1.4.md) | [bob-cli-l5.3.1.4](bob-cli-l5.3.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6bcc97a`](https://github.com/bobs-org/bob-cli/commit/6bcc97aeae39c13197755e1e482c90d740cc5479) | feat(gcal): add ack diagnostics and stale notices | [bob-cli-l5.3.1.4](bob-cli-l5.3.1.4.md) | 2026-11-13 02:07:55 EST |
