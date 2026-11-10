# Bead: bob-cli-j5.3 — Correct archive link repair

[Bead Pages](../README.md) / [bob-cli-j5](README.md) / bob-cli-j5.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1ai](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1ai.md) · **Assignee:** `bob-cli-j5.3` · **Size:** medium
**Created:** 2026-11-09 11:04:08 EST · **Closed:** 2026-11-09 16:31:02 EST
**Plan:** [202611/done\_notes\_archiving\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/done_notes_archiving_fixes.md)

## Description

link-repair: carry renamed block IDs into local links, qualify same-note heading links, skip code, follow the shared case rules, and hold blocks with duplicate IDs instead of silently skipping their repair.

## Notes

[2026-11-09T21:30:12Z · bob-cli-j5.3] followup_note -m --body docs-check-fails

[2026-11-09T21:30:20Z · bob-cli-j5.3] Levinas

[2026-11-09T21:30:40Z · bob-cli-j5.3] PROPOSED-FOLLOWUP-docs-json-budget

[2026-11-09T21:30:51Z · bob-cli-j5.3] PROPOSED FOLLOW-UP: trim json-outputs docs over budget 6143 vs 6000 cap

[2026-11-09T21:31:02Z · bob-cli-j5.3] link-repair done: renamed IDs rewrite self links, duplicates held with exit 1, heading links qualified, skip code true, case-insensitive basenames; 125 collect_done lib tests pass, full lib 6128 pass, lint clean, docs updated

## Dependencies

- **Depends on:** [bob-cli-j5.2](bob-cli-j5.2.md) ✓ · ⧖ 2026-11-09
- **Blocks:** [bob-cli-j5.4](bob-cli-j5.4.md) ✓ · ⧖ 2026-11-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-j5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.3/README.md) | [bob-cli-j5.3](bob-cli-j5.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a846a23`](https://github.com/bobs-org/bob-cli/commit/a846a23b73a07956bdf2bd4ca0026f8d20ca2d9d) | feat(archive)!: correct archive link repair | [bob-cli-j5.3](bob-cli-j5.3.md) | 2026-11-09 16:32:51 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j5.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-j5.3/README.md

<!-- sase:referenced-by:end -->
