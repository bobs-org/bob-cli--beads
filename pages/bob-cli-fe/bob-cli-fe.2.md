# Bead: bob-cli-fe.2 — Capture lands by merging (bob-cli)

[Bead Pages](../README.md) / [bob-cli-fe](README.md) / bob-cli-fe.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.c4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.c4.md) · **Assignee:** `bob-cli-fe.2` · **Size:** medium
**Created:** 2026-11-01 16:00:42 EST · **Closed:** 2026-11-01 20:23:26 EST
**Plan:** [202611/merged\_pomodoros.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/merged_pomodoros.md)

## Description

capture-link-merge: make named capture links, ref today, and #type markers merge the task's type into the destination name; retire type_marker_conflict; report the merge in JSON and human output.

## Notes

[2026-11-02T00:50:48Z · bob-cli-fe.2] PROPOSED FOLLOW-UP: Full cli suite shows unrelated flakes (articles::article_note_completion_shows_section_count, capture::complete_themes::configured_shell_describes_never_used_and_unconfigured_create fail singly across full runs but pass in isolation); consider flake task bead

[2026-11-02T01:23:26Z · bob-cli-fe.2] Closed by explicit `sase stitch create -B close` after create_commit landed d712168f ("feat(capture)!: land named captures by merging types"). The commit author requested bead completion after verifying the bead scope. Reopen with `sase bead open bob-cli-fe.2` if more work remains.

[2026-11-02T01:53:35Z · bob-cli-fb.2.1.land--1] DISCOVERED ISSUE: 5 named-link retype CLI failures reproduced on 5ac2fbc2 clean base (!perf context: capture_named_pomodoro_updates_both_notes, capture_named_pomodoro_dry_run, project_note_task_links_write_worked_example, offer_named_pomodoro_created_only_when_pick_lands, task_theme_writes_type_without_shown_suggestion) still expect [type::] retype after routing-core made land default to merge. Verified fixed by d712168f (fe.2 merge landing) on merged tree d712168f + fb.2.1 repairs: 5/5 pass. No new task; owned here.

## Dependencies

- **Depends on:** [bob-cli-fe.1](bob-cli-fe.1.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.10](bob-cli-fe.10.md) ✓ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-fe.9](bob-cli-fe.9.md) ✓ · ⧖ 2026-11-01

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
| read-by | [agent:bob-cli-fb.2.1.land--1][2] | Need fe.2 scope to attribute typeless failures | 3 |
| read-by | [agent:bob-cli-fe.2][3] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-fe.5][4] | Check whether capture-link-merge explains pre-existing retype test failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f9.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fb.2.1.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.2/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-fe.5/README.md

<!-- sase:referenced-by:end -->
