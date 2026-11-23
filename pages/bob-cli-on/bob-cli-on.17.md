# Bead: bob-cli-on.17 — Memory records for task requirements

[Bead Pages](../README.md) / [bob-cli-on](README.md) / bob-cli-on.17

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ex](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ex.md) · **Assignee:** `bob-cli-on.17` · **Size:** small
**Created:** 2026-11-21 11:13:27 EST · **Closed:** 2026-11-23 01:25:35 EST
**Plan:** [202611/task\_requirements.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_requirements.md)

## Description

memory: apply the accepted memory decisions (decision record and supersession mark, Task Drawer strand, Task Requirement strand) with /sase_memory_write, then regenerate the glossary page.

## Notes

[2026-11-23T06:25:35Z · bob-cli-on.17] Recorded decisions:task-reqs-are-met-with-their-task (notes_drawer_birth = with_first_note), marked decisions:capture-bullets-mirror-the-task-block superseded-in-part, rewrote glossary:task-drawer (NOTES / @foo+bar#notes, NOTES birth, REQUIREMENTS retired), added glossary:task-requirement. Ran sase memory init, regenerated docs/reference/glossary.md and docs/develop/decisions.md, just docs-check passed, epic-symbols empty.

## Dependencies

- **Depends on:** [bob-cli-on.12](bob-cli-on.12.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-on.16](bob-cli-on.16.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-on.8](bob-cli-on.8.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.17](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.17/README.md) | [bob-cli-on.17](bob-cli-on.17.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2b626d0`](https://github.com/bobs-org/bob-cli/commit/2b626d01ebf6f0f474537264e69f216ca9023285) | docs(memory): record that task requirements are met with their task | [bob-cli-on.17](bob-cli-on.17.md) | 2026-11-23 01:26:54 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.12][1] | Need epic and children phases | 1 |
| read-by | [agent:research.5u.cld][2] | Check whether in-flight req card/memory phases render or record the hash run glyph, for display redesign timing | 1 |
| read-by | [agent:research.5u.gem][3] | Inspect display-related and remaining phases of bob-cli-on | 1 |
| read-by | [agent:research.5x.gem][4] | Inspect remaining in-progress phases of bob-cli-on relevant to drawers and promotion | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.12/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.cld/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5u.gem/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.5x.gem/README.md

<!-- sase:referenced-by:end -->
