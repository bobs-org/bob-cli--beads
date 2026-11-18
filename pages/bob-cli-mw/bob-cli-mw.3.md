# Bead: bob-cli-mw.3 — Headline row at the top of the Mac idle agenda

[Bead Pages](../README.md) / [bob-cli-mw](README.md) / bob-cli-mw.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1dq](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1dq.md) · **Assignee:** `bob-cli-mw.3` · **Size:** medium
**Created:** 2026-11-17 17:23:40 EST · **Closed:** 2026-11-17 18:39:11 EST
**Plan:** [202611/daily\_headline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/daily_headline.md)

## Description

mac: decode the snapshot `headline`, add a fixed headline row under the Today title, measure, plan, and draw it, cover it with tests and a design render, update docs, and gate on macOS CI.

## Notes

[2026-11-17T23:39:11Z · bob-cli-mw.3] Mac headline row done: snapshot decodes trimmed headline (absent/null/blank->nil); fixed headline row under Today title (title->headline->budget->warning->state), 2-line clamp, semibold primary, .help + 'Today''s headline' VoiceOver; never on yesterday (Loading today...), stays on stale same-day, shows with .noOpen. Verified: swift build ok, swift test 2556 tests 0 failures, just docs-check passed (447 passed). Fixture Tests/Fixtures/agenda-headline.json added; design tests render it. Glossary strand already existed from cli phase, no edit needed. macOS CI run not watched this turn (push lands via host finalizer); macOS-only targets still need the exact-SHA run to green.

## Dependencies

- **Depends on:** [bob-cli-mw.1](bob-cli-mw.1.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mw.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mw.3/README.md) | [bob-cli-mw.3](bob-cli-mw.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@18de389`](https://github.com/bobs-org/bob-mac-capture/commit/18de389ef75541ba76144470e5fb0426cccbf57b) | feat(agenda): show Daily Headline row under Today title | [bob-cli-mw.3](bob-cli-mw.3.md) | 2026-11-17 18:42:17 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mw.3][1] | check full bead details | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mw.3/README.md

<!-- sase:referenced-by:end -->
