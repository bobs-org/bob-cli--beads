# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6 — Backlog batch 16: the broken Mac build, orphaned reference sources, archive moves under open PDFs, unignored plugin folders, and a plugin startup smoke check

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land`
**Created:** 2026-10-27 03:08:26 EDT · **Closed:** 2026-10-27 06:20:17 EDT
**Plan:** [202610/backlog\_batch16\_mac\_build\_orphan\_refs\_archive\_moves\_plugin\_guards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch16_mac_build_orphan_refs_archive_moves_plugin_guards.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch16_mac_build_orphan_refs_archive_moves_plugin_guards.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch16_mac_build_orphan_refs_archive_moves_plugin_guards.md

<!-- sase:links:end -->

## Description

Close five existing tasks by repairing the bob-mac-capture master build, stopping bob ref create from leaving saved sources without a pointer, verifying and coordinating the annotated-overwrite archive move, warning when a deployed plugin folder is not git-ignored, and giving plugin rollouts a real Obsidian startup check.

## Notes

[2026-10-27T10:20:14Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land] LANDER VERIFICATION (batch 16), 2026-10-27.

All 5 phases are closed. I re-read every phase note and checked the source of each epic commit:
- .1 mac-build-repair: bob-mac-capture d055e4f + d433166, merged as 0e7eba4 (PR #8). Master CI 40469875355 passed lint, Build, Test, Bundle, plist/signature, launch smoke, and install/reinstall. It ran batch 15's 9db33a6 RefsPanelModelTests.testRetryableCoordinationRenameErrorsRetainDraftAndDoNotAnnounceSuccess green.
- .2 ref-pointer-orphans: bob-cli 017b6927. Both sync executors carry the planned source_markdown, and create intake verifies the store and the persisted pointer. Doctor names the repair. A gate repaired the live orphan.
- .3 archive-move-presenter: bob-cli e557b021. Archive and reverse moves run in bounded ForMerging|ForMoving scopes with notifications.
- .4 plugin-ignore-guard: bob-cli 49f6131d and bob-plugins 3886e69. plugin_ignore=warn is honored: warnings only, and nothing edits .gitignore or untracks files.
- .5 plugin-startup-smoke: bob-plugins 88f0cdd and bob-cli 29d6105b. startup_smoke=implement is honored.

EPIC-CAUSED DEFECT FIXED IN THE LANDING: e557b021's native test archive_move_presenter_rollback_inside_move_restores_live_save_target failed deterministically on macOS CI (29d6105b run 40470693115, 017b6927 run 40479500571), so bob-cli master macOS was red. With the Mac offline, I ran diagnostics on a scratch ci/b16-presenter-diag branch (run 40481907132, branch deleted). NSDocument applies move notifications and re-reads about 0.5-0.6 s after the request ends. A move round trip leaves the URL and text unchanged, so the test edited before that re-read, and the re-read discarded the edit. The coordinated rollback itself is correct once the presenter settles. c2b69089 adds wait_for_reloaded_document. It passed the aarch64-apple-darwin clippy gate, scratch macOS CI (13 coordination tests x3, run 40484462394), and just check (6183 passed). Master CI 40485333363 on c2b69089 is green on ubuntu, macOS (both steps), lint, and package.

INTEGRATION: no non-epic commits landed in bob-cli (after 2f004d77), bob-plugins (after 0b02193), or bob-mac-capture (after 9db33a6) while the epic ran, so nothing needed rewiring.

ACCEPTANCE:
- bob-plugins master 88f0cdd: build:check is current, and I re-synced it with the stamp-aware workspace bob (--repo linked checkout, --no-pull). The dry run and the real sync both reported 0 copied, 22 unchanged, and no vault_ignore findings. bob plugins list reports 8 synced, 0 drift, and the vault tree is clean.
- Rollout gate 'xvfb-run -a npm run smoke:obsidian -- --deployed-vault /home/bryan/bob' passed: layout-ready 520 ms, heap peak 58 MiB, relation ready with 0 non-Markdown keys and reads, 4/4 editors, 0 exceptions/rejections/crashes.
- macOS CI checked on every landed SHA in both repositories (above).

TARGET TASKS closed done with evidence: bob-cli-cz, bob-cli-cy, bob-cli-d0, bob-cli-ch, bob-cli-a6.

FOLLOW-UP TRIAGE:
- No phase recorded a PROPOSED FOLLOW-UP.
- Lander discoveries:
  - The NSDocument post-move re-read window is acceptance evidence for the existing Mac run, so I routed it as a note on bob-cli-ay instead of filing a task.
  - The decision-record scope gap for the archive move went to bob-cli-d1 as a note, as the plan directed.
  - 017b6927 lacks a SASE_BEAD trailer: cosmetic, declined.
  - The tracked-folder warning wording (advice to remove from the index plus the never-untrack caution) is consistent with plugin_ignore=warn: declined.
- No new tasks filed.

LIMITATIONS: the real-Highlights guided acceptance for the archive move is unrun (Mac offline; ssh timed out). highlights.coordinate_pdf_writes stays shipped off until bob-cli-ay's acceptance passes.

Epic symbols: none. No just symvision recipe.

[2026-10-27T10:20:17Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land] Verified all 5 phases against source and commits; plugin_ignore=warn and startup_smoke=implement honored. Fixed one epic-caused defect in the landing: e557b021's native rollback presenter test was red on macOS CI for 29d6105b and 017b6927, because it edited before NSDocument's post-move re-read. c2b69089 waits for the re-read, and master CI 40485333363 is green on ubuntu and macOS. bob-mac-capture master 0e7eba4 CI 40469875355 is green through install. Integration: no non-epic commits landed in bob-cli, bob-plugins, or bob-mac-capture during the epic. Plugins re-synced from master 88f0cdd with the stamp-aware bob: 8 synced, 0 drift, no vault-ignore findings. The packaged Obsidian smoke gate passed against the deployment. just check passed with 6183 tests. Targets cz, cy, d0, ch, and a6 closed done. Follow-ups: no phase proposals; evidence routed to bob-cli-ay and bob-cli-d1; no new tasks. No epic symbols. Details in the preceding note.

[2026-10-27T10:22:50Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land] CONTINUATION: I authored the successor batch-17 epic plan. The scratch file is sase_plan_backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md, the expected archive is plan:202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md, and its parent_bead is this epic. It validated with --explain (10 decision-length errors fixed) and then plain, with 0 warnings. I submit it through sase plan propose right after this note; ownership transfers to the batch-17 lander on approval. It assigns five existing beads, all ready and unassigned:
- by: precommit macOS CI gate (large; decision macos_gate, default scratch_ci).
- co: attach-source ambiguous and title-mismatch skips (medium; attach_disambiguation, default verify; writes only via a Bryan gate).
- cm: research-hook hash-suffixed duplicate references (large; hook_dedupe, default implement).
- b1: per-PDF dirty ref-scan refusal (large; dirty_pdf, default hold).
- 8k: bob-mac-capture .swift-format (small).
Landing commits: bob-cli c2b69089 and plans dc50837 (batch-16 status done); no bob-plugins or bob-mac-capture changes. A fresh no-limit enumeration after closing finds 117 unresolved tasks: 112 ready and 5 snoozed (6q, aa, ah, cp, cq; no tag contains 0f76d558 yet). Deferred: 8r and 9x stay separate large launches; cv, 5m, and 5n are sase-repo fixes; 8q and b9 stay with 3j, whose lander has not run since 2026-10-02 ('sase bead work bob-cli-3j'); 58 waits for 87's land; b4 and ax wait for Bryan; ay, cx, and 30 need Bryan's Mac session; d1, 1x, and the other memory tasks need Bryan's authorization.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c2b6908`](https://github.com/bobs-org/bob-cli/commit/c2b6908913d8350cbefa9115da676499259e9f50) | test(file-coordination): wait for the presenter re-read after a rollback move | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.md) | 2026-10-27 06:01:59 EDT |
| bob-cli--plans | [`bob-cli--plans@dc50837`](https://github.com/bobs-org/bob-cli--plans/commit/dc50837833ac56c887b230bf50d199e94638aecb) | chore(plans): mark backlog batch 16 done | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.md) | 2026-10-27 06:20:34 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land][1] | Need the parent link and batch-16 landing pattern | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land][2] | Need the epic scope, children, and linked plan file | 1 |
| read-by | [agent:bob-cli-d2.land--1][3] | Final acceptance re-read after recording verification artifacts and blockers | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d2.land.md

<!-- sase:referenced-by:end -->
