# Bead: bob-cli-j5.1 — Safe archive selection

[Bead Pages](../README.md) / [bob-cli-j5](README.md) / bob-cli-j5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ai](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ai.md) · **Assignee:** `bob-cli-j5.1` · **Size:** medium
**Created:** 2026-11-09 11:04:08 EST · **Closed:** 2026-11-09 12:07:32 EST
**Plan:** [202611/done\_notes\_archiving\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/done_notes_archiving_fixes.md)

## Description

selection: restrict archiving to area and project notes, never move ^prj lines or roots with open subtasks or open parents, ignore fences, comments, and frontmatter, read closed statuses from Tasks settings, and start the docs/task-archive.md contract.

## Notes

[2026-11-09T17:00:04Z · bob-cli-j5.1] PROPOSED FOLLOW-UP: just docs-check lint fails on untouched mounted mac-capture pages over the 6000-word cap (capture-panel 6020, capture-previews 6314, keyboard 6029, protocol 6062) — already tracked by bob-cli-h9

[2026-11-09T17:07:32Z · bob-cli-j5.1] Archive selection now only moves closed #task roots from grouping-eligible area/project notes (grandfathered untyped notes that already own a paired archive). ^prj lines and closed tasks under open parents stay; closed roots with an open #task descendant are held as path:line; fences, comments, and frontmatter are ignored; closed/open come from Tasks settings; finished projects are skipped. docs/task-archive.md started. just check (fmt, lint, workspace tests including collect_done and mg18) passed. just docs-gen passed. just docs-check fails only on untouched mac-capture budgets already tracked by bob-cli-h9. epic-symbols empty.

## Dependencies

- **Blocks:** [bob-cli-j5.2](bob-cli-j5.2.md) ◐ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j5.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.1/README.md) | [bob-cli-j5.1](bob-cli-j5.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f1ee393`](https://github.com/bobs-org/bob-cli/commit/f1ee393db4cfe49a78e75af68b3e1a5e3b5b61fd) | feat(archive): select only area and project notes for done/ | [bob-cli-j5.1](bob-cli-j5.1.md) | 2026-11-09 12:08:49 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j5.1][1] | Need the phase scope, notes, and design file after compaction | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.1/README.md

<!-- sase:referenced-by:end -->
