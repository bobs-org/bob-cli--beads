# Bead: bob-cli-6u.16 — Install bob on the MacBook before plugins, verify, and update the vault

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.16

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.16` · **Size:** small
**Created:** 2026-10-12 10:26:02 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

rollout: bob on the MacBook first, verify the hoist and reconcile, then this host, then MacBook plugins; blocked.md PROJECT section and [unblocked::] CSS mute.

## Notes

[2026-10-12T14:45:54Z · 72] COORDINATION — bob-cli-6t.4 (project pull-in rollout) is gated on canceled 6s.12, which reads CLOSED, so it may reach the MacBook before you do. A note on 6t.4 redirects it to wait for this bead. Before step 1, read bob-cli-6t.4's notes. If it already ran just install or bob plugins sync on the Mac, record the Mac's bob commit and plugin versions, and check the vault for early hoists, tags and [unblocked::] writes. If 6t's code has landed, your install and sync carry the project pull-in: add one pilot (close a project's last task through its link, then check the ^prj link, [*], and that #hide is gone). See research:202610/bob_cli_6t_6u_epic_conflict.md.

[2026-10-12T20:57:59Z · bob-cli-6u.16] The canceled bob-cli-6t.4 did not run its MacBook install/sync; per its coordination note, leave the MacBook untouched until this bead closes. This phase’s MacBook-first rollout remains pending here; its install and sync will also carry the project pull-in.

[2026-10-12T21:04:48Z · bob-cli-6u.16--1] Mac rollout: SSH install completed (exit 0) from Mac bob-cli HEAD 36f997b; ssh mac bob --version => bob 0.1.0. With BOB_DIR=/Users/bbugyi/bob, projects sync --dry-run and live sync each reported 85 projects, 0 status updated, 0 ^prj edited, 0 task schedules updated, 0 warnings. Reconcile dry-run reported daily 2026/20261012.md already in sync; JSON live run ok=true, dry_run=false, scanned_files=5107, with empty consumed_blocked_references, prj_is_blocked_tags_added/stripped, unblocked_fields_written/pruned, applied_files, and warnings. Vault status before live run showed only modified ref/chat/databricks_nyc_cv_and_role_pitches.md and ref/papers/BryanBugyi_CV_extended_v4.md; left untouched. No eligible hoists were present in the preview.

## Dependencies

- **Depends on:** [bob-cli-6u.14](bob-cli-6u.14.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.15](bob-cli-6u.15.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.4](bob-cli-6u.4.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.6](bob-cli-6u.6.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.7](bob-cli-6u.7.md) ✓ · ⧖ 2026-10-12
- **Depends on:** [bob-cli-6u.9](bob-cli-6u.9.md) ✓ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.16](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.16.md) | [bob-cli-6u.16](bob-cli-6u.16.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:72][1] | Assess 6u phase state and deps for conflict analysis with 6t | 1 |
| read-by | [agent:bob-cli-6u.8][2] | Need epic and children status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
