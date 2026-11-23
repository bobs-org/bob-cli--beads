# Bead: bob-cli-pf.4.1.7.1 — In-flight write safety, Esc, and YAML escape

[Bead Pages](../README.md) / [bob-cli-pf.4.1.7](bob-cli-pf.4.1.7.md) / bob-cli-pf.4.1.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.4.1.land.md) · **Assignee:** `bob-cli-pf.4.1.7.1` · **Size:** medium
**Created:** 2026-11-23 03:09:55 EST · **Closed:** 2026-11-23 03:32:32 EST
**Plan:** [202611/property\_editor\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_editor_landing_repairs.md)

## Description

write-safety: make cancel/close/undo during a pending write safe, register modal sessions for generation and rename events, narrow old-bob detection, route Esc through the close ladder, and close the modal on y/Ctrl+E from the originating leaf.

## Notes

[2026-11-23T08:32:32Z · bob-cli-pf.4.1.7.1] write-safety done in bob-plugins: 298c serializes writes (write-busy, close/gen defer, no mid-write invalidation, unknown stays unknown); 298n adds outermost save guards, onEscapeKey ladder, lock-wait status plus Esc stopWaiting, session register/unregister; 298f closes modal first on y/Ctrl+E, species = handoff, Saving notices, stale copy removed; 298d narrows old-bob to typed needs-bob, path-scoped modify, rename/delete close modal plus clear dead Done; 298m origin-leaf preference. Verified: 17 new tests pass, all 91 property tests pass, adjacent suites pass, build:check plus validate exit 0, bob plugins sync ok. Full unit 8982/8989 with only tracked load flakes bob-cli-km (event-link-times) and bob-cli-pg (taskLinks p95), each green in isolation.

## Dependencies

- **Blocks:** [bob-cli-pf.4.1.7.2](bob-cli-pf.4.1.7.2.md) ◐ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.4.1.7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.4.1.7.1/README.md) | [bob-cli-pf.4.1.7.1](bob-cli-pf.4.1.7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@dcc6820`](https://github.com/bobs-org/bob-plugins/commit/dcc68207ceba6cc8d86c6a9ee347350df84b6cb9) | feat(bob-ledger-tools): property editor write safety and session hardening | [bob-cli-pf.4.1.7.1](bob-cli-pf.4.1.7.1.md) | 2026-11-23 03:33:52 EST |
