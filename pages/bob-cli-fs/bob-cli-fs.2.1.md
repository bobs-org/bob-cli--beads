# Bead: bob-cli-fs.2.1 — Rust relation-successor policy and planner for bob-cli-fs.2

[Bead Pages](../README.md) / [bob-cli-fs.2](bob-cli-fs.2.md) / bob-cli-fs.2.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-fs.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.2.md) · **Assignee:** `bob-cli-fs.2.1.land`
**Created:** 2026-11-02 06:30:50 EST
**Plan:** [202611/relation\_successor\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/relation_successor_core.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/relation_successor_core.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:02f513efcf6d714094b172c0 | attached via sase artifact create --bead |
| related | file:explicit:ed01e90996e17bd9acfc75b6 | attached via sase artifact create --bead |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/relation_successor_core.md

<!-- sase:links:end -->

## Description

Complete the Rust policy, shared copy, pure relation-successor engine, and successor-planner integration for bob-cli-fs.2 while preserving capture output until its later wiring phase.

## Notes

[2026-11-02T14:05:01Z · bob-cli-fs.2.1.land] FOLLOW-UP TRIAGE before repair tale: reviewed every note on phases .1/.2/.3 and used sase_new_task (all-status semantic search, last-week task sweep, active-epic review). .1 #1 SU-P22 and .1 #2 SA23 are one shared-fixture parity issue caused by this epic, not separate tasks. Cycler copy is now byte-identical (SHA256 08ffccedd68489dbfc06c73faf7a1be65df7b49cb48fdee1804f98d748c11cc0); navigation copy still differs in exactly those two vectors. Its relationCopyTruncate also returns 49 code points and splits an emoji. Repair and focused parity/Unicode tests belong to the landing tale; recorded on outer bob-cli-fs. .3 #1 human_pick_suffix_and_not_pulled_in is declined as already resolved: b483c93b updates the stale ^write-changelog expectation, and cargo test --test cli capture::keep_moving::human_pick_suffix_and_not_pulled_in -- --exact passes on cb729a76 (1/1). No genuinely distinct external follow-up remains and no new task was created. Copy this triage disposition into the eventual close note.

[2026-11-02T14:09:11Z · bob-cli-fs.2.1.land] LAND AUDIT at cb729a76 (fresh origin/master matches): reviewed epic/three closed phases/all notes, approved core and parent plans, DECISIONS, c3a2e62a/ace86f8e/cb729a76 source changes, and intervening 311b1514/b483c93b/fa1118c1 (also nearby 16f3a28f/a8f61375). Capture stays relation: None; no core memory/version/changelog edits. Four temporary Rust probes fail: classifier same-note ordering uses IDs (a-second before z-first), planner numbers Ready before Next across notes, a genuinely Blocked recovered dependent loses relation metadata, and an id-less duplicate-text offer changes the wrong task. Probe source file:explicit:02f513efcf6d714094b172c0 and result file:explicit:ed01e90996e17bd9acfc75b6; tracked source restored byte-for-byte. Additional concrete source gaps: explicit RelationEvent.slot is never read; integrated resolver ignores the full NoteIndex and cannot safely represent resolved unavailable targets; raw dependency counts/effective recovery and display-vs-placement dedup need correction; integration coverage skips fixture expectations and capture compatibility merely repeats one identical planner invocation. No epic-symbol entries for this epic or parent phase; no symvision recipe. These are residual epic work, not task follow-ups. Authored medium tale sase_plan_relation_successor_core_closeout.md with regression-backed repairs, navigation fixture integration, just check/docs-check, and same-turn epic plus bob-cli-fs.2 phase closeout. Epic remains open pending that work.

[2026-11-02T14:17:07Z · bob-cli-fs.8.1.land] DISCOVERED ISSUE corroboration from bob-cli-fs.8.1 landing, proposed by bob-cli-fs.8.1.4 note #3: bob-plugins 2ead3a8 still has navigation relation_successor vectors SHA256 22ad9ac75a0daa4bb13711b60cd1dbd7547aa9e47ab80cf09ffd4c924143fd4f versus canonical/cycler 08ffccedd68489dbfc06c73faf7a1be65df7b49cb48fdee1804f98d748c11cc0. This matches your notes #1/#2 and existing repair tale ownership for SA23/SU-P22 plus Unicode truncation. No duplicate task and no competing navigation edits from this landing.

[2026-11-02T14:26:07Z · bob-cli-fs.2.1.land] Closeout partial implementation: 4 land-audit probes now permanent and passing (classifier_orders_same_lane_by_source_line, planner_numbers_next_before_ready_across_notes, recovered_blocked_direct_dependent_keeps_relation_reason, missing_id_selects_the_exact_source_row). Classifier now orders rows by source line and groups by target path+line; planner OfferOrderKey is now (group, target-order|anchor, lane, path, line) with relation group_order so Next precedes Ready and placement never orders relation groups; identity uses line-based keys (no text resolve, no bare-path collision) and recovered ? offers as Ready; integrate uses full NoteIndex for known paths. Plugin parity: nav vectors copied byte-identical (08ffcced...), 206b truncate fixed to 48-scalar Array.from (matches Rust/cycler, astral-safe), nav/cycler vector+presentation suites pass (22+69), build and build:check pass. Deploy refused safely: bob plugins sync would overwrite uncommitted builds from bob-cli_10 (block-id-prompt) and bob-cli_16 (nav-hotkeys); did not force with -F. Residual per plan still open: explicit RelationEvent.slot production read with line-coordinate validation/fallback, effective-state projection for raw depends_on/project hide-tag (beyond recovered ?), relation-winner placement rebuild + fold recompute + keep-moving fold filtering, full SA14/SA15/SA18/SA20/SA21 coverage without skip-counting, run_planner keep-moving/bob_dir typed-routing proof, and real temp-vault capture compat across 3 configs. Beads left open; just check/docs-check not yet run to green.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fs.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.2.1.land.md) | [bob-cli-fs.2.1](bob-cli-fs.2.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`98bfec6`](https://github.com/bobs-org/bob-cli/commit/98bfec6aca2a877b9bceccb2ce5c9dbd6aa39267) | feat(task-relations): repair relation-successor ordering, identity, and recovery regressions | [bob-cli-fs.2.1](bob-cli-fs.2.1.md) | 2026-11-02 09:28:30 EST |
| bob-plugins | [`bob-plugins@e9f2fb7`](https://github.com/bobs-org/bob-plugins/commit/e9f2fb71019fbaa4a78579339c0c4b995f681218) | fix(nav): sync relation-successor vectors and 48-scalar truncation parity | [bob-cli-fs.2.1](bob-cli-fs.2.1.md) | 2026-11-02 09:28:56 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fs.2.1.1][1] | Need the governing decisions for this phase | 1 |
| read-by | [agent:bob-cli-fs.2.1.2][2] | Need epic DECISIONS that bind the classifier phase | 3 |
| read-by | [agent:bob-cli-fs.2.1.3][3] | Need child epic scope, plan file, and DECISIONS | 1 |
| read-by | [agent:bob-cli-fs.8.1.land][4] | Confirm follow-up dispositions still hold before closing fs.8.1 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fs.2.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fs.8.1.land.md

<!-- sase:referenced-by:end -->
