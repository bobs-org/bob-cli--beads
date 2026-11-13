# Bead: bob-cli-kx.2.1.5 — Archive eligibility and digest-confirmed batch planning

[Bead Pages](../README.md) / [bob-cli-kx.2.1](bob-cli-kx.2.1.md) / bob-cli-kx.2.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.md) · **Assignee:** `bob-cli-kx.2.1.5` · **Size:** medium
**Created:** 2026-11-12 11:37:45 EST · **Closed:** 2026-11-12 19:42:09 EST
**Plan:** [202611/gmail\_archive\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_core.md)

## Description

preview: Implement read-only archive planning, deterministic digests, historical backlog and whole-burst confirmation, -c/-n parsing, and lock-free dry-run projection. Implement section 5 and its tests.

## Notes

[2026-11-13T00:41:42Z · bob-cli-kx.2.1.5] PROPOSED FOLLOW-UP: docs-check lychee fails on the clean tree too — reference/mac-capture/event-notes link from docs/gcal-notes.md and docs/guides/plan-events-you-dont-own.md resolves nowhere in the built site; untouched by this phase.

[2026-11-13T00:41:53Z · bob-cli-kx.2.1.5] PROPOSED FOLLOW-UP: 45 lib unit failures (capture_complete/capture_parse/records/bank/gcal/completion) plus cli help::root_help and completion::vault::records_update_completion fail identically on the clean base tree (6785 passed/45 failed clean vs 6798 passed/45 failed with this phase); needs triage into task beads, not a phase-5 blocker.

[2026-11-13T00:42:09Z · bob-cli-kx.2.1.5] Section 5 preview lands: archive_preview planner with ordered first-failure reasons, frozen A/U sets, canonical order-independent digest, and backlog/burst/-c gate; -c/--confirm and -n/--no-archive on sync (pull alias untouched); dry-run projection after filing with rows/digest/pause-exit-1 and zero writes; report archive[]/archive_digest/summary.archived. Verified: 13 new unit tests, 3 new e2e tests, 546 gmail lib tests, gmail_sync/transport/shell/turns/send/draft suites, cli gmail/help suites, fmt, just lint all green; only pre-existing failures remain (45 lib, 2 cli, docs-check link), each reproduced on the clean tree and recorded as follow-ups.

## Dependencies

- **Depends on:** [bob-cli-kx.2.1.4](bob-cli-kx.2.1.4.md) ✓ · ⧖ 2026-11-12
- **Blocks:** [bob-cli-kx.2.1.6](bob-cli-kx.2.1.6.md) ◐ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.5/README.md) | [bob-cli-kx.2.1.5](bob-cli-kx.2.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0b806ae`](https://github.com/bobs-org/bob-cli/commit/0b806ae83fc4285c60eee2e631ee5678c757b732) | feat(gmail)!: add digest-confirmed archive batch planning preview | [bob-cli-kx.2.1.5](bob-cli-kx.2.1.5.md) | 2026-11-12 19:45:47 EST |
