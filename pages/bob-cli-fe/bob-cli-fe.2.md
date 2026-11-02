# Bead: bob-cli-fe.2 — Capture lands by merging (bob-cli)

[Bead Pages](../README.md) / [bob-cli-fe](README.md) / bob-cli-fe.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c4.md) · **Assignee:** `bob-cli-fe.2` · **Size:** medium
**Created:** 2026-11-01 16:00:42 EST
**Plan:** [202611/merged\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merged_pomodoros.md)

## Description

capture-link-merge: make named capture links, ref today, and #type markers merge the task's type into the destination name; retire type_marker_conflict; report the merge in JSON and human output.

## Notes

[2026-11-02T00:50:48Z · bob-cli-fe.2] PROPOSED FOLLOW-UP: Full cli suite shows unrelated flakes (articles::article_note_completion_shows_section_count, capture::complete_themes::configured_shell_describes_never_used_and_unconfigured_create fail singly across full runs but pass in isolation); consider flake task bead

## Dependencies

- **Depends on:** [bob-cli-fe.1](bob-cli-fe.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.10](bob-cli-fe.10.md) ◐ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.9](bob-cli-fe.9.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fe.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.2/README.md) | [bob-cli-fe.2](bob-cli-fe.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d712168`](https://github.com/bobs-org/bob-cli/commit/d712168f88c4240340115d61f45d424c7f45c066) | feat(capture)!: land named captures by merging types | [bob-cli-fe.2](bob-cli-fe.2.md) | 2026-11-01 20:22:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f9.land][1] | Check whether fe.2 scope covers untyped tasks landing in typed Pomodoros | 1 |
| read-by | [agent:bob-cli-fe.5][2] | Check whether capture-link-merge explains pre-existing retype test failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f9.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.5/README.md

<!-- sase:referenced-by:end -->
