# Bead: bob-cli-66.3 — In-memory agenda store, refresh triggers, path-filtered watcher, count from snapshot

[Bead Pages](../README.md) / [bob-cli-66](README.md) / bob-cli-66.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.48.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.48.linker.w0.md) · **Assignee:** `bob-cli-66.3` · **Size:** medium
**Created:** 2026-10-09 17:42:23 EDT · **Closed:** 2026-10-09 19:42:35 EDT
**Plan:** [202610/idle\_capture\_pomodoro\_agenda.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/idle_capture_pomodoro_agenda.md)

## Description

mac-agenda-store: add the pure refresh state machine and relevance filter in CaptureCore, and the @MainActor `CaptureAgendaStore` that refreshes on launch, filtered vault events, show, submit, wake, unlock, and midnight. It replaces the per-show capture-pomodoros spawn, derives the close-comma count from the snapshot, passes FSEvents paths through the watcher, and falls back for an old bob.

## Notes

[2026-10-09T23:42:19Z · bob-cli-66.3--2] CI run https://github.com/bobs-org/bob-mac-capture/actions/runs/38004444446 green at SHA 3d36a02 (plus Linux: swift test 972 tests pass, incl. CaptureAgendaRefreshFilter/State/Models tests)

[2026-10-09T23:42:35Z · bob-cli-66.3--2] store/refresh/filter/watcher/count wired and verified: CI 38004444446 green at SHA 3d36a02 plus Linux swift test 972 pass incl. CaptureAgendaRefreshFilter/State/Models

## Dependencies

- **Depends on:** [bob-cli-66.2](bob-cli-66.2.md) ✓ · ⧖ 2026-10-09
- **Blocks:** [bob-cli-66.5](bob-cli-66.5.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-66.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.3.md) | [bob-cli-66.3](bob-cli-66.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@aaa2d9b`](https://github.com/bobs-org/bob-mac-capture/commit/aaa2d9bba8164fd075c7d3ff958383afb862bfc4) | feat(agenda): in-memory store, refresh triggers, filtered watcher, count | [bob-cli-66.3](bob-cli-66.3.md) | 2026-10-09 19:15:41 EDT |
| bob-mac-capture | [`bob-mac-capture@3d36a02`](https://github.com/bobs-org/bob-mac-capture/commit/3d36a023e0de319c5eea21ae206e71797eef975c) | fix(capture): avoid dynamic Self capture in FSEventStream callback | [bob-cli-66.3](bob-cli-66.3.md) | 2026-10-09 19:26:34 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-66.3][1] | Need phase notes and remaining work check | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-66.3.md

<!-- sase:referenced-by:end -->
