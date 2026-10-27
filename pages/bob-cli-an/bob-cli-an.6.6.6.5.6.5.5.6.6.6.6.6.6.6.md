# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6 — Backlog batch 15: wrong-vault pre-syncs, coordinated PDF moves, plugin deploys that overwrite each other, the last red Mac XCTest, and the docs URL gate

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land`
**Created:** 2026-10-26 15:53:09 EDT · **Closed:** 2026-10-27 03:02:35 EDT
**Plan:** [202610/backlog\_batch15\_vault\_safety\_pdf\_moves\_and\_red\_gates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch15_vault_safety_pdf_moves_and_red_gates.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch15_vault_safety_pdf_moves_and_red_gates.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch15_vault_safety_pdf_moves_and_red_gates.md

<!-- sase:links:end -->

## Description

Close five existing tasks by keeping -b runs from syncing the live vault, coordinating the remaining Highlights PDF writers, guarding plugin deploys against overwriting another agent's uncommitted build, turning bob-mac-capture master CI green, and clearing the docs-check published-URLs gate.

## Notes

[2026-10-27T07:02:23Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land] LANDER VERIFICATION (batch 15), 2026-10-27.

All 5 phases are closed. I re-read every phase note and checked each epic commit's source:
- bob-cli dc040b02 (.1 vault identity guard before locks or pre-sync in rename, migrate-tasks, migrate-zorg, and themes/relations rename).
- Child epic .2.1: f00ae66e, 1e923594, 22882a7d, 0971ad56, 0e6b0400, da3fa751 (coordinated rename/move and id repair, guarded publish for create --force and the public writers, acceptance kit). bob-mac-capture 9db33a6 (rename hint removed).
- bob-cli 115a3610 and bob-plugins 0b02193 (.3 deploy stamps and refusal; DECISION deploy_guard=refuse honored in evaluate_guard).
- bob-mac-capture f2513d2 (.4 queued-Return expectation corrected; fixture and production unchanged).
- bob-cli b65bff1b and bob-plugins 1621bd6 (.5 docs links).

EPIC-CAUSED DEFECTS FIXED IN THE LANDING:
1. f00ae66e's macOS-only file_coordination/macos_tests.rs never compiled. bob-cli macOS CI therefore failed 'Lint macOS-only targets' on every commit from f00ae66e to da3fa751, and the move tests never ran. 0a5f0793 fixes it: PathBuf import, &mut presenter, typed Err. I reproduced and verified it with an aarch64-apple-darwin clippy gate on athena. CI 40462474420 is green on ubuntu and macOS, and all nine macos_tests ran natively, including the NSDocument presenter move, rollback, and hold fixtures.
2. Phase .3's .bob-deploy.json deployed_at wrote Bob's day-zone clock with a Z suffix (02:42Z at 06:42 UTC). 2f004d77 records real UTC, keeps BOB_NOW as a day-zone test pin, and adds a regression test. just check passed (6171), and CI 40463816281 is green on ubuntu and macOS.

INTEGRATION: commits since the epic started that are not part of it:
- bob-cli 96793fda, 82716a64, 42abfa70 (bob-cli-ct link catalog).
- bob-mac-capture 6c3b1d4, 2764ec5 (ct.4/.5) and 906a7df (agent 14k.w0, no bead).
None pre-syncs a -b vault or writes Highlights PDFs outside the guarded or coordinated paths: ct.3 recatalog reads PDFs and commits code.json locally with no sync. Phase .2.1 started after ct.3 and built on it. I noted on bob-cli-ch that .3's stamp-ignore check is reusable there. 906a7df broke the bob-mac-capture master Build (filed as bob-cli-cz, below), which leaves 9db33a6 not yet CI-verified. I did not patch it: bob-mac-capture AGENTS.md forbids landing uncompiled Swift, and the Mac is offline (ssh timed out).

ACCEPTANCE:
- bob-plugins master 0b02193 has a current build:check. I re-synced it with the stamp-aware workspace bob (--repo linked checkout, --no-pull): 0 copied, 22 unchanged.
- Stamps were written, then re-stamped with the fixed UTC binary (--force, 0 copies): clean 0b02193, 2026-10-27T06:55:06Z.
- bob plugins list reports 8 synced, 0 drift. Every stamp is git-ignored and the vault tree is clean.
- just docs-check (BOB_DOCS_BOB_PLUGINS_DIR set to bob-plugins master) passed every gate, including published URLs (173 pages).

TARGET TASKS closed done with evidence: bob-cli-cj, bob-cli-az, bob-cli-cu, bob-cli-cr (CI 40396107283 on f2513d2 ran both queued-Return tests green), bob-cli-cs.

FOLLOW-UP TRIAGE:
- .2 note #2 (annotated-overwrite archive move issues no didMoveToURL): not caused by the epic (the archive transaction predates it) and could not be verified natively. Filed as bob-cli-d0 (bug, large).
- .3 PROPOSED FOLLOW-UP (docs published-URL gate on run-bob-from-obsidian.md:111): declined as a duplicate of bob-cli-cs, which .5 fixed. The gate passes.
- .1, .4, .5, and .2.1.* recorded no proposals.
- Lander discoveries:
  - bob-cli-cz (ci, small): bob-mac-capture Build broken since 906a7df.
  - bob-cli-d1 (memory, small): decisions:open-pdf-writes-are-coordinated omits the batch-15 move, stamp, and create --force scope. No phase filed it, though the plan asked.

LIMITATIONS: real-Highlights acceptance for rename and stamp is unrun (Mac offline). highlights.coordinate_pdf_writes stays off until it passes (bob-cli-ay).

Epic symbols: none. No just symvision recipe.

[2026-10-27T07:02:35Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land] Verified all 5 phases (and child epic .2.1) against source and commits; deploy_guard=refuse honored. Fixed two epic-caused defects in the landing: bob-cli 0a5f0793 (macOS-only move-coordination tests never compiled, so macOS CI lint was red from f00ae66e to da3fa751; now green, and all nine NSDocument/move tests ran natively in CI 40462474420) and 2f004d77 (deploy stamp deployed_at was local time labelled Z; now UTC, with a regression test; CI 40463816281 green). Integration: ct.1-3 and bob-mac-capture ct.4/5 need no changes. 906a7df broke the bob-mac-capture Build, filed as bob-cli-cz; it is not patched because the Mac is offline and Swift must be compiled. Plugins re-synced from master 0b02193 with stamp-aware bob: 8 synced, 0 drift, clean UTC stamps. just check 6171 passed; docs-check passed all gates. Targets cj, az, cu, cr, cs closed done. Follow-ups: filed d0 (archive move presenter, from .2 #2), cz, and d1 (decision record scope); declined the .3 docs-URL proposal as a duplicate of cs (fixed). No epic symbols. Details in the preceding note.

[2026-10-27T07:07:28Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land] CONTINUATION: I authored the successor batch-16 epic plan. The scratch file is sase_plan_backlog_batch16_mac_build_orphan_refs_archive_moves_plugin_guards.md, the expected archive is plan:202610/backlog_batch16_mac_build_orphan_refs_archive_moves_plugin_guards.md, and its parent_bead is this epic. It validated with --explain and then plain, with 0 warnings, and I submit it through sase plan propose right after this note. Ownership transfers to the batch-16 lander on approval.

It assigns five existing beads:
- cz: bob-mac-capture master build broken by 906a7df (small).
- cy: bob ref create leaves a saved source without its source_markdown pointer (large).
- d0: annotated-overwrite archive move under an open PDF (large).
- ch: plugin folder ignore check (medium; decision plugin_ignore, default warn).
- a6: Obsidian startup smoke check (large; decision startup_smoke, default implement).

Landing commits: bob-cli 0a5f0793 and 2f004d77, plans fb1d78a (batch-15 status done); no bob-plugins or bob-mac-capture changes. A fresh no-limit enumeration after closing finds 122 unresolved tasks: 117 ready and 5 snoozed (6q, aa, ah, cp, cq; no tag contains 0f76d558 yet).

Deferred:
- 8r and 9x remain separate large launches.
- cv, 5m, and 5n are sase-repo fixes.
- 8q and b9 stay with 3j, which has had no open phases and no running lander since 2026-10-02 and needs 'sase bead work bob-cli-3j'.
- 58 waits for 87.
- b4 and ax wait for Bryan.
- d1 and the other memory tasks need Bryan's authorization.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0a5f079`](https://github.com/bobs-org/bob-cli/commit/0a5f079320a2add11749b24e54895b70dce34ed1) | test(file-coordination): fix macOS-only move-coordination test build | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) | 2026-10-27 02:40:09 EDT |
| bob-cli | [`2f004d7`](https://github.com/bobs-org/bob-cli/commit/2f004d7722bde0dd8ae7ba13a16581defcc21bcd) | fix(plugins): record deploy stamp time in real UTC | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) | 2026-10-27 02:53:40 EDT |
| bob-cli--plans | [`bob-cli--plans@fb1d78a`](https://github.com/bobs-org/bob-cli--plans/commit/fb1d78ab5af96c3c72e5dea1c3937a74cf459f45) | chore(plans): mark backlog batch 15 done | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) | 2026-10-27 03:02:47 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land][1] | Need the parent epic's landing notes and how the prior lander handed off | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land][2] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
