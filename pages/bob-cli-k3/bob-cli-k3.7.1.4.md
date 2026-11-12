# Bead: bob-cli-k3.7.1.4 — Album breadcrumb and read-only schema header

[Bead Pages](../README.md) / [bob-cli-k3.7.1](bob-cli-k3.7.1.md) / bob-cli-k3.7.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-k3.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.7.md) · **Assignee:** `bob-cli-k3.7.1.4` · **Size:** medium
**Created:** 2026-11-11 23:10:17 EST · **Closed:** 2026-11-12 09:44:57 EST
**Plan:** [202611/album\_plugin\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_plugin_ui.md)

## Description

album-header: implement path-resolved breadcrumb, copy-capture affordance, report-driven schema card, album-only record-property hiding, Reading/Live Preview lifecycle, and header tests.

## Notes

[2026-11-12T11:57:46Z · research.4b.linker.w0] COORDINATION: user-endorsed research research:202611/album_record_schema_ux/album_record_schema_ux.md recommends the read-only schema card be COLLAPSED BY DEFAULT (one summary line under the header that expands into a chip view) instead of an always-open schema table. A follow-up epic plan ('Album record schema: render in the header, edit through bob') has been proposed to reshape this header and add an editable Schema Card backed by a new bob albums update writer. If your header has not painted yet, preferring the collapsed summary saves that epic a reshape; either way keep every fixture in your phase spec (Properties isolation, unrelated record key, type change, empty schema, ordered choices, unload) - the follow-up epic builds on them unchanged. Do not expand your scope: the always-open table is the only part the research drops.

[2026-11-12T14:38:37Z · bob-cli-k3.7.1.4--2] PROPOSED FOLLOW-UP: Fix the three clean-base bob-plugins npm test failures. Full suite on clean master failed 3 of 6,255: two existing 200-link / 50-target Live Preview timing budgets (keep-moving-marks surface: 717.2 ms vs 25 ms; off-clock link chips: 90.1 ms vs 25 ms) and task-tag session toggle/onload wiring (expected one call, got two). The same failures reproduce without the album-header changes; the performance suite passes.

[2026-11-12T14:40:31Z · bob-cli-k3.7.1.4--2] PROPOSED FOLLOW-UP: Repair the clean-base docs:check strict-site failure. Running BOB_CLI_DIR=... npm run docs:check with the album changes stashed reproduced the same pre-existing broken link at develop/plugins/validation.md:55 to bob-vim-yank-flash.md#verification; lint and generated-drift checks pass. This link is outside the album-header changes.

[2026-11-12T14:44:57Z · bob-cli-k3.7.1.4--2] Implemented and deployed the album breadcrumb/schema header. npm run build completed; all 8 focused album-header tests pass. Full npm test had 3 failures on the clean base (two existing 200-link Live Preview timing thresholds and task-tag session toggle/onload assertion), recorded as PROPOSED FOLLOW-UP. docs:check failed on both changed and clean trees at the existing develop/plugins/validation.md:55 link to bob-vim-yank-flash.md#verification; recorded as PROPOSED FOLLOW-UP. After syncing the landed upstream build without -F, bob plugins sync deployed bob-ledger-tools from this checkout; vault main.js and styles.css compare byte-for-byte, and bob plugins list reports synced/enabled. epic-symbols is empty.

## Dependencies

- **Depends on:** [bob-cli-k3.7.1.3](bob-cli-k3.7.1.3.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-k3.7.1.5](bob-cli-k3.7.1.5.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.7.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.7.1.4.md) | [bob-cli-k3.7.1.4](bob-cli-k3.7.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c2f6834`](https://github.com/bobs-org/bob-plugins/commit/c2f683490cdbcb5e1eabaa596cb164847f46d9ba) | feat(album-header): add breadcrumb and schema header | [bob-cli-k3.7.1.4](bob-cli-k3.7.1.4.md) | 2026-11-12 09:46:11 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.4b.cld][1] | Check progress of the in-flight album header phase that hides the record row, to sequence recommendations | 1 |
| read-by | [agent:research.4b.grk][2] | Need the schema header phase that currently treats record as read-only | 1 |
| read-by | [agent:research.4b.mus][3] | research record frontmatter Obsidian rendering | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.cld/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.grk/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.mus/README.md

<!-- sase:referenced-by:end -->
