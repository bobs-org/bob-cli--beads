# Bead: bob-cli-hg.6.1 — Complete Gmail save and offline list

[Bead Pages](../README.md) / [bob-cli-hg.6](bob-cli-hg.6.md) / bob-cli-hg.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.md) · **Assignee:** `bob-cli-hg.6.1.land`
**Created:** 2026-11-05 23:47:35 EST · **Closed:** 2026-11-06 06:58:56 EST
**Plan:** [202611/gmail\_save\_list.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_save_list.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_save_list.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:18705a7c72a5c9d067cf6be1 | attached via sase artifact create --bead |
| related | file:explicit:e7aea0b4b642b917e1e2d9f7 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_save_list.md

<!-- sase:links:end -->

## Description

Finish bob-cli-hg.6 with confirmed thread saving, inert local images, append-only refresh, exact-path vault commits, and offline saved-mail listing.

## Notes

[2026-11-06T10:23:23Z · bob-cli-hg.6.1.land] FOLLOW-UP TRIAGE (all seven PROPOSED FOLLOW-UP entries across four phases): .1 #1, .2 #1, .3 #1, and .4 #2 overlap on clipboard registrations; corroborated bob-cli-hp with proposing IDs. .2 #3, .3 #1, and .4 #1 share the README contract-table digest defect; corroborated bob-cli-hs, no new duplicate. .1 #1 and .2 #2 catalog 73-vs-72 are repaired in b70a8fbf/fcc4efa5; added resolution evidence to bob-cli-de and decline a new task/stale +1. .1 #1 successor verdict assertions are repaired by intervening 5c119a06; decline a new task. Root-help portions of .1 #1, .2 #2, .3 #1, .4 #2 are caused by outer hg.4 and already noted on hg; appended causal evidence there and include snapshot refresh in the remaining repair tale. Searches covered CI task statuses, the last-week CI task sweep, and all 17 in-progress epic descriptions; no distinct new follow-up remains. These outcomes must be repeated in the eventual close note. Remaining save transaction/preview defects found by this lander are epic work, not follow-up tasks.

[2026-11-06T10:25:02Z · bob-cli-hg.6.1.land] LAND AUDIT: Reviewed all four child scopes and all eleven child notes (seven PROPOSED FOLLOW-UP entries and four closure notes), approved child and outer plan contracts/DECISIONS, commits cdc40030/c0d877be/b70a8fbf/fcc4efa5 and current source. Full-body and subject_who defaults are honored and no forbidden memory edits occurred. Reviewed intervening 6af313b4/248a2bfa/5c119a06: merge and successor changes do not alter the staged writer/lock/commit APIs; fetch confirmed origin/master=fcc4efa5. Remaining epic work independently reproduced using current bob with only temporary synthetic vaults/fake gog: failed image-save commit then retry persists an embed and image but no attachment origin, and its Gmail save event incorrectly records created=false/added=0; headers save followed by full without rerender returns unchanged yet writes an unreferenced image; changing configured account only to uppercase refuses the same saved identity; human -d -R emits only a status line labelled structural preview, with no actual diff. The validated medium tale sase_plan_gmail_save_closeout.md plans those repairs plus missing orchestration/race acceptance, root-help integration, and both epic and hg.6 parent-phase closeout in its own coding turn. Epic and parent remain open. epic-symbols for hg.6.1 and hg.6 are empty; justfile has no symvision recipe. just check run dffe775a90af653215b67f14325a396b finished exit 101: fmt/lint passed, lib 5371 passed/2 clipboard failures/2 ignored, CLI 3262 passed/1 stale root-help failure, gmail_shell 24/24 and all other binaries passed. Catalog protocol and every capture successor-verdict test pass, confirming those declined proposals are fixed. just docs-check completed with only known bob-cli-hs digest failure, 446 passed/1 skipped. No check-full was run. Portable synthetic reproducer is attached as file:explicit:e7aea0b4b642b917e1e2d9f7.

[2026-11-06T11:58:56Z · bob-cli-hg.6.1.land--1] Gmail save/list closeout — 2026-11-06

Implementation completed the approved save transaction repair: imports and origins now follow the final merged note; failed-commit retries retain accurate creation/addition facts and emit exact-once journal/origin events; image collisions choose safe deterministic paths; account identity comparisons tolerate case-only changes while preserving the original path and metadata; and human/JSON dry-runs include a redacted structural preview. Added synthetic orchestration regressions for image retry, append-only merge, rerender, collisions, account case, and body-free preview. Refreshed the two root-help snapshots and documented preview/recovery behavior. The four original child phases are closed.

Reviewed commits: cdc40030, c0d877be, b70a8fbf, fcc4efa5, plus intervening 6af313b4, 248a2bfa, and 5c119a06. The latter capture merge and successor-verdict work was checked for impact on the staged Gmail writer/lock/commit APIs.

Preserved decisions: full bodies remain the default; Gmail links use the subject-and-who label; this save/list work makes no SASE memory edits or new decision/glossary records. Gmail remains read-only, network work stays outside the vault lock, and all new coverage uses synthetic mail and isolated temporary vaults.

Verification: Gmail shell suite 30/30 passed; `just docs-gen` passed and root-help snapshots match. `just check` exited 101 with 5,371 library tests passed, 2 ignored, and only these two unchanged clean-base failures: `native::catalog::tests::public_leaves_are_entries_or_excluded` (clipboard appears in both lists) and `native::completion::kinds::tests::every_table_entry_matches_the_tree` (duplicate `clipboard:count`). All other targets passed. `just docs-check` exited 1 with 446 passed, 1 skipped, and only the known unchanged `test_readme_table_matches_original_contract_index_snapshot` digest mismatch tracked by bob-cli-hs; lint, generated drift, strict site build, URLs, links, search, tutorial, and media checks passed. `sase bead epic-symbols` is empty for both bob-cli-hg.6.1 and bob-cli-hg.6. `just symvision` is unavailable because no recipe exists.

Disposition of all seven original child proposals:
1. bob-cli-hg.6.1.1 note #1: clipboard catalog/completion failures are corroborated under bob-cli-hp; no duplicate filed. Its catalog 73-vs-72 and capture successor-verdict failures are repaired by b70a8fbf/fcc4efa5 and 5c119a06 respectively; no stale +1 task. Its root-help drift belongs to outer hg.4 and the snapshots are refreshed here.
2. bob-cli-hg.6.1.2 note #1: same clipboard failures, corroborated under bob-cli-hp; no duplicate.
3. bob-cli-hg.6.1.2 note #2: catalog 73-vs-72 is repaired and recorded under bob-cli-de; root-help drift is included in this repair; no duplicate.
4. bob-cli-hg.6.1.2 note #3: README contract-table digest mismatch is corroborated under bob-cli-hs; no duplicate.
5. bob-cli-hg.6.1.3 note #1: clipboard failures belong to bob-cli-hp, README digest to bob-cli-hs, and root-help drift to outer hg.4 (refreshed here); no duplicate.
6. bob-cli-hg.6.1.4 note #1: README contract-table digest mismatch is corroborated under bob-cli-hs; no duplicate.
7. bob-cli-hg.6.1.4 note #2: clipboard failures belong to bob-cli-hp and root-help drift to outer hg.4 (refreshed here); no duplicate.

The linked Gmail save/list plan is marked status: done. Parent bob-cli-hg.6 has one child epic, this completed bob-cli-hg.6.1; all listed dependencies are closed and its complete save/list scope is met. Outer epic bob-cli-hg remains open for its waiting land agent.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.1.land.md) | [bob-cli-hg.6.1](bob-cli-hg.6.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7825a98`](https://github.com/bobs-org/bob-cli/commit/7825a98f0eebbec5c05932aabe267773fe7915cd) | fix(gmail): close transactional save gaps | [bob-cli-hg.6.1](bob-cli-hg.6.1.md) | 2026-11-06 07:02:37 EST |
| bob-cli--plans | [`bob-cli--plans@e619854`](https://github.com/bobs-org/bob-cli--plans/commit/e6198541744c8f65619f32d9232fd8a5f70f2244) | docs(gmail): mark save list plan done | [bob-cli-hg.6.1](bob-cli-hg.6.1.md) | 2026-11-06 07:03:24 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-hg.6.1.3][1] | Need the epic decisions governing the save transaction phase | 1 |
| read-by | [agent:bob-cli-hg.6.1.land--1][2] | Inspect the approved Gmail epic closeout scope, child beads, and recorded decisions | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.6.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.6.1.land.md

<!-- sase:referenced-by:end -->
