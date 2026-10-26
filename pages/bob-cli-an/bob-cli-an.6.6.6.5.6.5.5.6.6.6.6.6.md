# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6 — Backlog batch 13: vault plugin integrity, popout mark gates, CI flakes, and Tasks query cost

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land`
**Created:** 2026-10-26 10:47:09 EDT · **Closed:** 2026-10-26 12:50:29 EDT
**Plan:** [202610/backlog\_batch13\_vault\_integrity\_and\_perf\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch13_vault_integrity_and_perf_1.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch13_vault_integrity_and_perf_1.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch13_vault_integrity_and_perf_1.md

<!-- sase:links:end -->

## Description

Close five existing tasks by preventing host-to-host overwrites of deployed bob-articles files, mirroring the remaining ledger-tools mark gates into Obsidian popouts, diagnosing two CI flakes, and reducing native Tasks query time and memory cost.

## Notes

[2026-10-26T16:50:29Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land] LANDER VERIFICATION (batch 13), 2026-10-26. All 5 phases are closed. I re-read every phase note and checked the source of each epic commit: bob-cli f73f926d (.5) and 6a470ebe (.3), bob-plugins 756a368 (.2), vault 0b682436 (.1, gate), and bob-mac-capture eed300d (verified by .4).

(1) vault-plugin-ignore: athena recheck shows .gitignore:69 ignoring bob-articles, nothing tracked, plugin files present; bob-articles 0.2.1 synced on athena, apollo, and mac. bob-cli-cd closed done.
(2) popout-mark-gates: all four families use applyMarkGateClass + registerMarkGatePopoutSync, with the today off-class passing !enabled, and both-state popout tests. On master 457db03: priority 18/0, task-tag 27/0, freshness 19/0, today 42/0, build:check current. bob-dep-chips has no CSS gate. INTEGRATION: concurrent agent 14l had deployed a pre-rebase 1.74.0 build without these gates at 12:23 and did not redeploy after rebasing onto 756a368. I redeployed with bob plugins sync -p bob-ledger-tools: vault files are byte-identical to 457db03 (7 gate families), 0 drift. Mac also runs 457db03; apollo's checkout is at 24bfdb2 until its next install. bob-cli-cb closed done.
(3) capture-kick-flake: the move_job install-before-remove overlap is real (spool.rs:777). The test now asserts distinct job ids while keeping the real kick, the 20 s clip, and the <10 s guard. bob-cli-5o closed done; the historical panic was never recovered.
(4) refs-refresh-flake: the flake SHA c4dc4b6 (10-09) predates eed300d (10-11), which is an ancestor of master d8a828f. The post-sweep git-date copy is at RefsLibrary.swift:763-778 and the expectation is unchanged. bob-cli-67 closed done.
(5) tasks-query-cost: the Dataview index is skipped for Tasks. Lander live-vault read-only measurement: pre-fix release bob 0.3.1 took 4.3-4.6 s at 1,587 MB max RSS (reproducing 1.58 GB); the master build took 1.0 s at 58 MB with byte-identical output. Phase note #2 was a garbled path, so the full phase evidence is preserved on bob-cli-6k. bob-cli-6k closed done.

DECISIONS honored: deploys only via bob plugins sync; the live-vault repair ran only through a Bryan-approved gate; no version or CHANGELOG edits; just check only, never check-full.

INTEGRATION since 10:47: no concurrent commit touches the epic's files. just check on master 5e8c6ecd did not compile: cc.5's a6d3ecbf test called render_frozen_note with 10 args after c9.5.1's 38a02d7b reduced it to 8. The landing commit fixes that call. Re-run with the fix: lib 3617/3 failed, cli 2227/1 failed, all other binaries green, and every epic regression test passed. The remaining 4 failures are cc.4/cc.5 code, recorded as a DISCOVERED ISSUE on active epic bob-cli-cc.

FOLLOW-UP TRIAGE: .1 note #2 (plugins sync should enforce vault ignore rules) became new task bob-cli-ch (feature, medium). .1 note #6 (ref code catalog/completion/help failures) became a DISCOVERED ISSUE on active epic bob-cli-cc, which caused it; no task. No other PROPOSED FOLLOW-UP notes. Audit discoveries: bob-mac-capture master CI has been red since 14b's 1311536 (6 RefsPanel tests), filed as bob-cli-ci (ci, large); cc.7's failing new Copy test was noted on bob-cli-cc. bob-cli-cg was closed done as resolved by 14l (docs and harness both 116/167 px).

Epic symbols: none. No just symvision recipe. BACKLOG after this audit: 115 unresolved tasks (111 ready, including new bob-cli-ch and bob-cli-ci; 4 snoozed: 3o, 6q, aa, ah). 3o's wake time has passed and its prerequisite is re-verified: Mac hooks log shows 936 reports, all 0 legacy children, the latest at 12:45 today. 3o is actionable.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`993f177`](https://github.com/bobs-org/bob-cli/commit/993f177aa7637ae13d6f5955b5013d797a958729) | fix(highlights-ref): drop stale render\_frozen\_note args from source pointer test | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) | 2026-10-26 12:54:43 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2][1] | parent epic plan and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.2/README.md

<!-- sase:referenced-by:end -->
