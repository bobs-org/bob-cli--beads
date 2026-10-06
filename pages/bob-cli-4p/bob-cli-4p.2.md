# Bead: bob-cli-4p.2 — Task Card and priority notices reuse the glyph

[Bead Pages](../README.md) / [bob-cli-4p](README.md) / bob-cli-4p.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0xf](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0xf.md) · **Assignee:** `bob-cli-4p.2` · **Size:** small
**Created:** 2026-10-06 13:50:51 EDT · **Closed:** 2026-10-06 14:23:19 EDT
**Plan:** [202610/priority\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/priority_marks.md)

## Description

card-glyph: bob-navigation-hotkeys renders the shared mark through `api.priorityMarks` v1 in the Task Card level chips and in the priority notice header, and falls back to today's rendering when the api is absent. Then test, document, build, and sync.

## Notes

[2026-10-06T18:23:19Z · bob-cli-4p.2] card-glyph done: Task Card level chips and priority notice headers render the shared mark via api.priorityMarks v1 (decorative+inheritColor) with Lucide fallback; nav 2.7.2->2.8.0. Verified: npm run build ok, npm test 1910/1910 pass, npm run validate 6/6 ok, bob plugins sync deployed nav (vault main.js verified), bob-cli just lint ok, no epic-symbol leftovers. Live Obsidian checklist still pending for Bryan.

## Dependencies

- **Depends on:** [bob-cli-4p.1](bob-cli-4p.1.md) ✓ · ⧖ 2026-10-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-4p.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-4p.2/README.md) | [bob-cli-4p.2](bob-cli-4p.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ce54258`](https://github.com/bobs-org/bob-cli/commit/ce54258121bd567344f603311a4792299cd05185) | docs(projects): record Task Card and notice reuse of priority marks | [bob-cli-4p.2](bob-cli-4p.2.md) | 2026-10-06 14:24:41 EDT |
