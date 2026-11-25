# Bead: bob-cli-pw.5.1.2 — Ingest a meeting dossier with its event re-root in one commit

[Bead Pages](../README.md) / [bob-cli-pw.5.1](bob-cli-pw.5.1.md) / bob-cli-pw.5.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pw.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.5.md) · **Assignee:** `bob-cli-pw.5.1.2` · **Size:** medium
**Created:** 2026-11-24 15:14:21 EST · **Closed:** 2026-11-24 19:08:05 EST
**Plan:** [202611/ref\_meet\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_meet_cli.md)

## Description

first-filing: add create/meet_route.rs using the prepared request, meeting PDF profile, marker, source store, and shared intake. Extend the locked intake transaction for a checked in-place event-root edit and structured outcomes. Verify fresh filing, source preservation, queued drain, status, scoped commits, and failure paths.

## Notes

[2026-11-25T00:08:05Z · bob-cli-pw.5.1.2] Implemented create/meet_route.rs filing prepared dossiers via meeting PDF profile, marker, source store, and shared intake with producer bob ref meet; extended locked intake with typed EventRootEdit (verify exact row, inbox/missing transition, identity recheck, dirty guard, set_row_metadata, scoped commit bob ref meet: ingest meetings/<stem>); verified with 8 new route tests (fresh filing, re-root with badge preservation, ordinary override, stale queue, dirty preservation, queued drain, transcript/status variants, scoped commit and one-commit revert) plus existing intake, meeting-birth, and meet prepare suites green; epic-symbols clean

## Dependencies

- **Depends on:** [bob-cli-pw.5.1.1](bob-cli-pw.5.1.1.md) ✓ · ⧖ 2026-11-24
- **Blocks:** [bob-cli-pw.5.1.3](bob-cli-pw.5.1.3.md) ◐ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pw.5.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pw.5.1.2/README.md) | [bob-cli-pw.5.1.2](bob-cli-pw.5.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bf30944`](https://github.com/bobs-org/bob-cli/commit/bf309445934ef16924565c4f48134400c038b7c7) | feat(meet): ingest meeting dossier with event re-root in one commit | [bob-cli-pw.5.1.2](bob-cli-pw.5.1.2.md) | 2026-11-24 19:09:20 EST |
