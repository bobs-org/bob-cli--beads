# Bead: bob-cli-6u.16 — Install bob on the MacBook before plugins, verify, and update the vault

[Bead Pages](../README.md) / [bob-cli-6u](README.md) / bob-cli-6u.16

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.70](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.70.md) · **Assignee:** `bob-cli-6u.16` · **Size:** small
**Created:** 2026-10-12 10:26:02 EDT · **Closed:** 2026-10-12 17:11:37 EDT
**Plan:** [202610/prj\_line\_project\_blocking.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_project_blocking.md)

## Description

rollout: bob on the MacBook first, verify the hoist and reconcile, then this host, then MacBook plugins; blocked.md PROJECT section and [unblocked::] CSS mute.

## Notes

[2026-10-12T14:45:54Z · 72] COORDINATION — bob-cli-6t.4 (project pull-in rollout) is gated on canceled 6s.12, which reads CLOSED, so it may reach the MacBook before you do. A note on 6t.4 redirects it to wait for this bead. Before step 1, read bob-cli-6t.4's notes. If it already ran just install or bob plugins sync on the Mac, record the Mac's bob commit and plugin versions, and check the vault for early hoists, tags and [unblocked::] writes. If 6t's code has landed, your install and sync carry the project pull-in: add one pilot (close a project's last task through its link, then check the ^prj link, [*], and that #hide is gone). See research:202610/bob_cli_6t_6u_epic_conflict.md.

[2026-10-12T20:57:59Z · bob-cli-6u.16] The canceled bob-cli-6t.4 did not run its MacBook install/sync; per its coordination note, leave the MacBook untouched until this bead closes. This phase’s MacBook-first rollout remains pending here; its install and sync will also carry the project pull-in.

[2026-10-12T21:04:48Z · bob-cli-6u.16--1] Mac rollout: SSH install completed (exit 0) from Mac bob-cli HEAD 36f997b; ssh mac bob --version => bob 0.1.0. With BOB_DIR=/Users/bbugyi/bob, projects sync --dry-run and live sync each reported 85 projects, 0 status updated, 0 ^prj edited, 0 task schedules updated, 0 warnings. Reconcile dry-run reported daily 2026/20261012.md already in sync; JSON live run ok=true, dry_run=false, scanned_files=5107, with empty consumed_blocked_references, prj_is_blocked_tags_added/stripped, unblocked_fields_written/pruned, applied_files, and warnings. Vault status before live run showed only modified ref/chat/databricks_nyc_cv_and_role_pitches.md and ref/papers/BryanBugyi_CV_extended_v4.md; left untouched. No eligible hoists were present in the preview.

[2026-10-12T21:11:24Z · bob-cli-6u.16--1] ROLL OUT COMPLETE — Mac bob install succeeded (Mac source HEAD 36f997b; bob 0.1.0). Mac projects sync dry-run and live: 85 projects, 0 status changes, 0 ^prj edits/hoists, 0 task schedule changes, 0 warnings. Reconcile dry-run: 2026/20261012.md already in sync. Live reconcile JSON: ok=true, dry_run=false, scanned_files=5107; zero consumed_blocked_references, tag additions/strips, unblocked writes/prunes, applied files, warnings, or deferred files. The Mac vault had only pre-existing committed edits to ref/chat/databricks_nyc_cv_and_role_pitches.md and ref/papers/BryanBugyi_CV_extended_v4.md; left untouched. Host `just install` succeeded from this workspace; bob 0.1.0. Host plugin source checkout 1abde2f; `bob plugins sync -n` reported 0 copied, 0 skipped, 16 unchanged. Mac `bob plugins sync` also 0 copied, 0 skipped, 16 unchanged; `bob plugins list` confirms block-id-prompt 1.27.0, bob-ledger-tools 1.49.0, bob-navigation-hotkeys 2.24.0, bob-project-tasks 1.0.0, bob-vim-surround 1.5.2, task-status-cycler 1.31.0; all 6 synced, 0 drift. Vault rollout commit 3ac0b3be updates blocked.md (PROJECT section, disjoint DEPENDENT/STRANDED filters, reconcile guidance) and .obsidian/snippets/dataview-properties.css (mute unblocked pills); project.md already described inline ^prj dates. `git diff --check` passed. Host and Mac vault-sync status both match 3ac0b3be with no conflicts. No eligible project hoists appeared in preview; user follow-up: reload plugins/restart Obsidian on Mac, then pilot Ctrl+Shift+P → b on a ^prj, Schedule on ^prj, and Ctrl+Alt+Shift+N into/out of project.

[2026-10-12T21:11:37Z · bob-cli-6u.16--1] Verified Mac bob install/version, staged and live projects sync and reconcile with no warnings, host install, host dry-run plugin sync, Mac plugin sync and all six plugin versions, targeted blocked.md/CSS changes committed as 3ac0b3be, and host/Mac vault-sync status with no conflicts. Epic-symbol check was clear. Mac Obsidian reload and the documented interaction pilot remain for Bryan.

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
| read-by | [agent:bob-cli-6u.16--1][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-6u.8][3] | Need epic and children status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.72/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.16.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.8/README.md

<!-- sase:referenced-by:end -->
