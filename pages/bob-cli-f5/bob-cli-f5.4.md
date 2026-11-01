# Bead: bob-cli-f5.4 — Real-Obsidian e2e, docs, version, and sync

[Bead Pages](../README.md) / [bob-cli-f5](README.md) / bob-cli-f5.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16q](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16q.md) · **Assignee:** `bob-cli-f5.4` · **Size:** medium
**Created:** 2026-11-01 09:24:21 EST · **Closed:** 2026-11-01 11:22:07 EST
**Plan:** [202611/task\_link\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_link_marks.md)

## Description

landing: prove the feature in a real Obsidian scratch vault (LP, Reading, cross-note status changes, toggle, line height, light/dark screenshots), fix what it finds, finish the plugin docs and manifest, bump the version, and sync to the vault.

## Notes

[2026-11-01T16:21:55Z · bob-cli-f5.4] PROPOSED FOLLOW-UP: npm test had 6 failures unrelated to task-link-marks (wikilink rank 13.3ms>12ms budget; freshness reload event empty; gcal create listener 0!==1; keep-inbox timezone 12:30 vs 16:30; note-ready startup storm 1!==2; relationIndex layout-ready timeout). Record if they reproduce on a clean bob-plugins tree.

[2026-11-01T16:22:07Z · bob-cli-f5.4] Landed task link marks 1.81.0. xvfb e2e all passed (LP+Reading six states, ledger skip, managed edges unmarked, cross-note ready→done with one swap, toggle, line-height 24/24, hover, Tasks query rings). Screenshots: /tmp/bob-task-link-marks-e2e-out/e2e-task-link-marks-light.png and e2e-task-link-marks-dark.png. Query rows stamp via Tasks MarkdownRenderer ctx.sourcePath; nested DEPENDS ON/LINKS stay unmarked. Vault copy has toggle-task-link-marks at 1.81.0. npm run validate and docs:check passed. ledger_rows=skip, dim_closed_links=no. Did not close parent bob-cli-f5.

## Dependencies

- **Depends on:** [bob-cli-f5.3](bob-cli-f5.3.md) ✓ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-f5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.4/README.md) | [bob-cli-f5.4](bob-cli-f5.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@32c9e03`](https://github.com/bobs-org/bob-plugins/commit/32c9e03248a03c1570f4dea6a29e7c8f6c15f130) | feat(task-link-marks): land rings in real Obsidian and bump 1.81.0 | [bob-cli-f5.4](bob-cli-f5.4.md) | 2026-11-01 11:23:08 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f5.4][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-f5.4/README.md

<!-- sase:referenced-by:end -->
