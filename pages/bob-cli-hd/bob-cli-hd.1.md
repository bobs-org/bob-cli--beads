# Bead: bob-cli-hd.1 — Fix the Obsidian rename regression and the Task Card live-link lookup

[Bead Pages](../README.md) / [bob-cli-hd](README.md) / bob-cli-hd.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5q.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5q.linker.w0.md) · **Assignee:** `bob-cli-hd.1` · **Size:** medium
**Created:** 2026-11-05 10:26:34 EST · **Closed:** 2026-11-05 10:52:53 EST
**Plan:** [202611/pomodoro\_names\_follow\_task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/pomodoro_names_follow_task_types.md)

## Description

plugin-writer-bugs: in bob-navigation-hotkeys, make Pomodoro rename (commit and preview) retype linked tasks again, and make the Task Card type, inbox route, and note-move live-link lookup search open entries only, by vault path plus block ID.

## Notes

[2026-11-05T15:52:53Z · bob-cli-hd.1--1] Fixed Pomodoro rename preview and commit to use explicit task retyping, scoped Task Card and note-move live-link lookup to open entries by vault path and block ID, and kept inbox lookup unique among open task rows. Verified npm run build, npm run build:check, focused rename/Task Card/inbox scripts, git diff --check, bob plugins sync, and no remaining epic symbols.

## Dependencies

- **Blocks:** [bob-cli-hd.3](bob-cli-hd.3.md) ✓ · ⧖ 2026-11-05
- **Blocks:** [bob-cli-hd.7](bob-cli-hd.7.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-hd.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hd.1.md) | [bob-cli-hd.1](bob-cli-hd.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@811f650`](https://github.com/bobs-org/bob-plugins/commit/811f6508eec5781a1c824e8e1afc66f3c0e92bbe) | fix(navigation): repair pomodoro type rename and live-link lookup | [bob-cli-hd.1](bob-cli-hd.1.md) | 2026-11-05 10:54:39 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hd.1--1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-hd.1.md

<!-- sase:referenced-by:end -->
