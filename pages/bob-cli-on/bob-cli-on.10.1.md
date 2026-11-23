# Bead: bob-cli-on.10.1 — Obsidian requirement guards, toggle, drop, and typing assist

[Bead Pages](../README.md) / [bob-cli-on.10](bob-cli-on.10.md) / bob-cli-on.10.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-on.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.md) · **Assignee:** `bob-cli-on.10.1.land`
**Created:** 2026-11-21 14:10:17 EST · **Closed:** 2026-11-21 23:04:03 EST
**Plan:** [202611/obsidian\_req\_gestures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_gestures.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/obsidian_req_gestures.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_req_gestures.md

<!-- sase:links:end -->

## Description

Complete bob-cli-on.10 (the obsidian-gestures phase of plan:202611/task_requirements.md). The cycler, nav, and Block ID Prompt recognize requirement lines through byte-identical JS twins that pass bob-cli's RQ/RL/RW vectors. Every task gesture refuses or redirects on a req line with the contract copy. Ctrl+] toggles note and req with zone placement and the first-req scoop, Alt+[ drops with a reason and Alt+] restores, Ctrl+Shift+P opens the owner's Task Card, the offer-close scope note never counts reqs, and typing `- [` then space expands to `- [ ] ` with overtype absorption, atomic Backspace, Vim insert support, and a clean Undo. Each write is one undo step.

## Notes

[2026-11-22T02:11:52Z · bob-cli-oj.land] FROM bob-cli-oj.land (deploy coordination): the vault's task-status-cycler is still stuck behind a clean stamp from 726f9a5, bob-cli-oj.1's lost local commit, so 'bob plugins sync -p task-status-cycler' refuses without -F (bug bob-cli-or). The deployed 1.52.0 bytes equal landed ancestor 6e0d764, so forcing drops nothing unlanded. bob-cli-oj.land staged a Bryan-approval gate that rechecks the stamp and those bytes, then force-deploys origin/master task-status-cycler from a temporary detached worktree. If the gate already ran, sync normally after fetching and merging origin/master; if your lander already resolved the stamp, the gate reports 'skipped' and does nothing.

[2026-11-22T03:39:08Z · bob-cli-on.10.1.land] LANDING TRIAGE of every child PROPOSED FOLLOW-UP (bob-cli-on.10.1 land agent): (1) ^prj NOTES filing (.1 #1) — not caused by this epic (bob-cli-on.3 task_block_layout); already DISCOVERED ISSUE #2 on active epic bob-cli-on, corroborated there with the twin/RW-writer details. (2) bob plugins sync clean-stamp refusal (.1 #2, .2 #1, .3 #3) — duplicate of bob-cli-or, +1 recorded; all three plugins now dry-run 'up to date'. (3) offer-close project scope counts top-level #ref rows (.2 #2) — new bug bob-cli-p8 (small), related to bob-cli-on.11. (4) bob-cli docs contract-registry tests 54 vs 55 (.3 #1, .5 #1) — caused by bob-cli-on.1 (a0961435), already DISCOVERED ISSUE #1 on bob-cli-on; re-reproduced 3/8 failing on e5ee4a8d and corroborated there. (5) perf-budget flakes (.1 #3, .3 #2, .4 #2) — duplicates, +1 on bob-cli-io (frees-marks) and bob-cli-m1 (dependency stage). (6) published-URLs feed.rs:70 docs/1.0.md (.4 #1, .6 #1) — caused by active epic bob-cli-os (0c60af45, bob-cli-os.7), already a DISCOVERED ISSUE there; corroboration note added. (7) real-Obsidian e2e launch env / DBUS stall (.4 #3) — same remediation as bob-cli-np (runner launch environment), +1 with the DBUS evidence and helper pointer. (8) bob-ledger-tools adopting the full RQ twin (.6 #2) — new feature bob-cli-p9 (medium). No proposal declined.

[2026-11-22T04:04:03Z · bob-cli-on.10.1.land] Verified the six phase commits: bob-plugins f292fff, e5cb895, 28d76fd, d3b80d7, d2877fe, and 7b96dce; bob-cli e5ee4a8d. Their land verification covered RQ/RL/RW vectors 144/144 and twin copies 7/7, cycler guards/drop/toggle/typing, nav guards 19/19, Block ID Prompt guard 4/4, SV verdicts 14/14 including SV25, and the e2e self-test. Fixtures remain byte-identical and the docs §5 gesture table landed.

This integration closed the two remaining gaps. The transcluded tree close now applies bob-cli finish_close_node's whole-token #task guard to each node's own write while continuing through that node's children; the new regression cases cover skipped plain roots, a closing #task child, and a #task root retaining completion-field behavior. The insert twin now returns added as the count of newly owned reqs at every depth, matching bob-cli 536455ac; tests cover nested additions (3), insertion beside two existing reqs (1), and loose notes excluded from the count. All targeted guard/vector/copy suites passed (165/165). npm run build, docs:gen, build:check, and docs inventory check passed.

npm test completed with 8569/8575 unit tests passing and 13/13 perf tests passing; its two failures were load-sensitive budgets in test-ledger-tools-frees-marks and test-ledger-tools-event-link-times. Both scripts passed alone on rerun; test-navigation-dependencies-stage-performance also passed alone. docs:check passed lint, generated drift, and strict Zensical build; it failed only the known published URL from bob-cli src/native/highlights_ref/podcast/feed.rs:70 (docs/1.0.md points to missing /1.0). The contract-registry suite passed in this run.

Deployed and dry-run verified task-status-cycler 1.57.0 and bob-navigation-hotkeys 2.104.0; both dry-runs report up to date. No -F was used. Follow-up triage was already recorded on this epic: bob-cli-p8 and bob-cli-p9, +1 on bob-cli-or, bob-cli-io, bob-cli-m1, and bob-cli-np, with notes on bob-cli-on and bob-cli-os. Both epic-symbols commands list nothing. `just symvision` could not run because this checkout has no such recipe.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-on.10.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-on.10.1.land.md) | [bob-cli-on.10.1](bob-cli-on.10.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@1d397b7`](https://github.com/bobs-org/bob-cli--plans/commit/1d397b783ee7e5eff90d3fc711bc5ad83054adac) | docs(plans): mark req gestures plan done | [bob-cli-on.10.1](bob-cli-on.10.1.md) | 2026-11-21 23:06:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-on.10.1.1][1] | Need epic decisions and notes | 1 |
| read-by | [agent:bob-cli-on.10.1.2][2] | Need the epic decisions | 1 |
| read-by | [agent:bob-cli-on.10.1.4][3] | Epic context and decisions | 1 |
| read-by | [agent:bob-cli-on.10.1.5][4] | Need parent epic DECISIONS before implementing nav guards | 1 |
| read-by | [agent:bob-cli-on.10.1.6][5] | need epic plan and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.4/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.5/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-on.10.1.6/README.md

<!-- sase:referenced-by:end -->
