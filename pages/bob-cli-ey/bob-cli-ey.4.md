# Bead: bob-cli-ey.4 — bob-cli ^prj drawers resolve to project-note H2 sections

[Bead Pages](../README.md) / [bob-cli-ey](README.md) / bob-cli-ey.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2x.linker.w0.md) · **Assignee:** `bob-cli-ey.4` · **Size:** medium
**Created:** 2026-10-31 12:52:04 EDT · **Closed:** 2026-11-01 03:28:13 EST
**Plan:** [202610/capture\_drawers\_and\_directives.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_drawers_and_directives.md)

## Description

cli-project-drawers: on a project note's own `^prj` line, resolve `#drawer` against the note's eligible `##` sections, appending or creating `## Title Case` the way promotion does; list those sections in the drawer menu; extend the Task Drawer glossary strand.

## Notes

[2026-11-01T08:28:13Z · bob-cli-ey.4] cli-project-drawers done: ^prj #drawer resolves against eligible H2s with exact drawer key rules (match appends after last nonblank line; missing appends ## Title Case at EOF via promotion casing); structural/reserved/ambiguous/near-duplicate refusals; separate #type and --drawer work on ^prj; drawer menu and capture-drawers list H2s with entry_count and 'Adds to ## X' consequence; Task Drawer strand extended. Verified: 9 new tests/cli/capture/prj_drawers.rs pass, full just check green (all suites 0 failed), just docs-check green, epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-ey.2](bob-cli-ey.2.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.4/README.md) | [bob-cli-ey.4](bob-cli-ey.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ffc5f1f`](https://github.com/bobs-org/bob-cli/commit/ffc5f1f99fe5c25f0d660e4e1d3c63c054b3e406) | feat(capture): resolve ^prj drawers against project-note H2 sections | [bob-cli-ey.4](bob-cli-ey.4.md) | 2026-11-01 03:29:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.4/README.md

<!-- sase:referenced-by:end -->
