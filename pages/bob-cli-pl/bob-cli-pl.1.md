# Bead: bob-cli-pl.1 — Retire the second frontmatter writers on project notes (bob-plugins + vault)

[Bead Pages](../README.md) / [bob-cli-pl](README.md) / bob-cli-pl.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5y.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5y.linker.w1.md) · **Assignee:** `bob-cli-pl.1` · **Size:** medium
**Created:** 2026-11-22 20:56:40 EST
**Plan:** [202611/area\_project\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_cards.md)

## Description

one-writer: remove the bob-project-tasks count writer and the project-creation processFrontMatter call, sweep the retired count keys out of the vault through bob props, and update projects.base and project.md, retiring status waiting.

## Notes

[2026-11-23T02:01:12Z · bob-cli-pl.1] Blocked by epic launch precondition: bob-cli-pf remains in_progress (audited read on 2026-11-23). The plan requires stopping, recording this note, and changing no files until bob-cli-pf is closed. Workspace tree was clean at 3e480e4a.

[2026-11-23T02:09:18Z · bob-cli-pl.1] Launch precondition rechecked: bob-cli-pf is still in_progress. Earlier phase notes confirm no implementation was attempted; this checkout remains clean. Added an explicit dependency on bob-cli-pf and am staging a prerequisite monitor to resume this phase after it closes. No source, vault, or memory files changed.

[2026-11-24T14:52:00Z · bob-cli-pl.1--1] IMPLEMENTATION: pf resolved done. Both plugin writers removed; focused plugin tests pass 59/59. Landed props still protects task_count/open_task_count, so this phase also removes those two obsolete derived roles and tests guarded removal plus byte-exact undo on project, area, and archived notes. This is needed to run the required sweep independently of pl.2; pl.2 still owns the additive legacy flag/grouping. Landed property-editor key is bare +, so docs and vault use + instead of planned =+.

[2026-11-24T14:54:44Z · bob-cli-pl.1--1] CHECKPOINT: All implementation edits are ready; 59 focused plugin tests plus 9 rerun new tests pass, cargo fmt and both diff checks pass. Full npm test, Rust props suites/build, and docs gate are next under a monitor. Apollo deployment succeeded for bob-project-tasks 1.2.0 and bob-navigation-hotkeys 2.107.1 (no force). Audit is in plugins docs/bob-project-tasks.md; no processFrontMatter call remains, snapshot commands/methods preserved exactly. No live note/Base edits or real vault sweep yet: after build, set BOB_BIN to its debug/bob, prove fixture dry-run/apply/idempotence, sweep ~/bob dry-run then apply with before/after byte verification, edit projects.base/project.md per design (bare +), verify Base rendering, recheck epic-symbols and close only pl.1. Earlier installed-bob trial correctly refused retired keys because its role table predates this patch. No follow-up bead needed; remaining work clearly fits one coder.

[2026-11-24T15:26:19Z · bob-cli-pl.1--2] ACCEPTANCE CHECKPOINT: Fresh monitor build located at /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws16-261124_094256/debug/bob. Rust props 54/54 and CLI props 20/20 passed. Real Bob scratch archived CRLF project: dry-run byte-identical; apply removes exactly two count lines; repeat no-op. Live 106 notes/212 keys snapshotted locally under .git/pl1-acceptance/vault-before (including four conflict copies, no archived counts). Initial live preview was interrupted with exit 143 before completion and made no writes; one 30s Bob timeout prompted raising the cleanup subprocess bound to 120s. Guarded full preview/apply with exact local byte checks is prepared in .git/pl1-acceptance/live-cleanup.py, not yet run. Vault projects.base/project.md edits are done and vault-sync owns their commits; bare + is documented. All three Base views verified in isolated real Obsidian on athena: Active WIP only, Closed done/canceled only, All four fixture statuses, no Tasks columns. Highlights commands/methods byte-identical to plugin HEAD b1413ba9. No processFrontMatter calls remain (only explanatory comments). Apollo sync rechecked both changed plugins up to date; athena and Mac still require bob plugins sync. epic-symbols reports none.

## Dependencies

- **Depends on:** [bob-cli-pf](../bob-cli-pf/README.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-pl.9](bob-cli-pl.9.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.1.md) | [bob-cli-pl.1](bob-cli-pl.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1fn--code][1] | Check whether retiring project-note frontmatter writers covers the requirement close Undo guard | 1 |
| read-by | [agent:fx][2] | Research whether the pl epic's dependency on pf is necessary | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.1fn.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.fx/README.md

<!-- sase:referenced-by:end -->
