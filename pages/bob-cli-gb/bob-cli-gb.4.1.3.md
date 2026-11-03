# Bead: bob-cli-gb.4.1.3 — Report Google clock deprecations and document the completed contract

[Bead Pages](../README.md) / [bob-cli-gb.4.1](bob-cli-gb.4.1.md) / bob-cli-gb.4.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-gb.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-gb.4.md) · **Assignee:** `bob-cli-gb.4.1.3` · **Size:** medium
**Created:** 2026-11-02 18:52:59 EST · **Closed:** 2026-11-02 23:12:09 EST
**Plan:** [202611/gcal\_clock\_tags.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_clock_tags.md)

## Description

clock-diagnostics: produce one warning per deprecated occurrence per run and structured deprecations in sync and list, including unchanged and dry-run results; report canonical-tag conflicts, root-only drop suggestions, and on-wins copy. Complete the gcal and JSON documentation, regression matrix, and documentation generation/checks. Record final evidence for the child epic land agent.

## Notes

[2026-11-03T04:12:09Z · bob-cli-gb.4.1.3] clock-diagnostics done: new gcal/diagnostics.rs (one warning per occurrence, structured deprecations with calendar_id/event_id/title/token/where/replacement/drop_suggested/on_wins; canonical conflict warns clock_tag_conflict). Sync threads diagnostics through written/unchanged/retry/dry-run/waiting with quiet-safe stderr warnings and JSON arrays; list adds top-level warnings/deprecations plus stderr warnings. Tests: tests/gcal_diagnostics.rs 4 passed (matrix, lifecycle/quiet/waiting, inherited abby->love.md advice, empty canonical); lib native::gcal 207 passed; gcal_lifecycle 40, gcal_list 8, gcal_sync 49 passed; cargo fmt clean; clippy gate exit 0; just docs-gen + docs-check passed (447 passed). No epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-gb.4.1.2](bob-cli-gb.4.1.2.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-gb.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-gb.4.1.3/README.md) | [bob-cli-gb.4.1.3](bob-cli-gb.4.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f9f4c70`](https://github.com/bobs-org/bob-cli/commit/f9f4c7067f98e4c48c09c981f457f2c635ae8c47) | feat(gcal): report Google clock deprecations and document the completed contract | [bob-cli-gb.4.1.3](bob-cli-gb.4.1.3.md) | 2026-11-02 23:13:36 EST |
