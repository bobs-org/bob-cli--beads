# Bead: bob-cli-jf.1.1 — Restore bob-mac-capture master and clean polluted checkouts

[Bead Pages](../README.md) / [bob-cli-jf.1](bob-cli-jf.1.md) / bob-cli-jf.1.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-jf](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-jf.md) · **Assignee:** `bob-cli-jf.1.1` · **Size:** medium
**Created:** 2026-11-10 06:47:59 EST
**Plan:** [202611/bob\_mac\_capture\_history\_restore.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_mac_capture_history_restore.md)

## Description

restore: rebuild master as 29147289 plus every genuine Mac commit now on top of 9a0bb25c, then publish it per restore_method (rewrite gate with cross-machine checkout cleanup, or a fast-forward revert commit), verify docs-check and the exact-SHA macOS CI run, and record the old-to-new SHA mapping.

## Notes

[2026-11-10T12:06:14Z · bob-cli-jf.1.1] RESTORE GATE PREPARED: No prior phase work had landed. Live master 5e29dd26 includes three genuine Mac commits (b20ceca5, 3fb3a2be, 5e29dd26); replay onto 29147289 passes author/date and tree fidelity checks on all 52 changed paths. Local bare-mirror and cp -a checkout rehearsals passed with the exact bundled shell command: clean and harmless-dirty branches moved, dirty/untracked bytes and stash retained, conflicting edits and unique local commits preserved/reported, enclosing-host fake checkout skipped, polluted CI branch deleted while clean CI branch retained. Merge and concurrent-master lease refusal checks passed; already-restored master refuses rerun. Read-only surveys reached athena/apollo/mac: 3/1/1 polluted checkouts respectively, all working trees clean. The approved plan explicitly requires a human gate before force-pushing; preparing that gate now. No shared-history push or live checkout cleanup has run. Gate continuation owns remote/checkout verification, docs-check, exact-SHA macOS CI via monitor, real SHA mapping notes, epic-symbol check, and closing only this phase. Scratch source/evidence: /tmp/bob-cli-jf-restore-prep; scripts and rehearsal results are embedded in the durable gate bundle. This is the planned approval handoff, not unfinished coding scope requiring a child epic.

[2026-11-10T12:16:36Z · bob-cli-jf.1.1--1] HISTORY RESTORED by approved gate custom-79d25c9d-301c-4338-adf4-7fd429460d10 on 2026-11-10. Old master 2c406dd500915f4d8bee43cbae8f5bdbd985df1b -> restored master af604c6d9e05ec6440bfce5fa15ced97e388035c, based on unchanged GOOD 29147289ca584953ce7f8cfd29b5ed60a5380f76. Complete genuine Mac commit mapping:
- b20ceca5526c6f379f8d2983e70115f150a9ae48 -> 6dddea35b47bfc64c1295d547a3966c9e7a516e7 (feat(capture): present notebook capture targets and previews)
- 3fb3a2bea591fd9756722cf8b313d0394ffdf746 -> a36f3e8163357828e09b132a5fc2c9fdf77c2c05 (fix(capture): name nested notebook parent and restore Mac tests)
- 5e29dd26b1adb908cb402df83153b1c73c25164d -> 37933a1425f4fc8f2dcb1cb261dca065e9d7b7fd (fix(capture): show set Record Card values and conceal the route @)
- 2c406dd500915f4d8bee43cbae8f5bdbd985df1b -> af604c6d9e05ec6440bfce5fa15ced97e388035c (test(capture): fix notebook picker assertions and dotted type-through harness)
BAD 9a0bb25c4b55b547a6d92c35c93017471e74feff and the accidental bob-cli history are removed, not replayed. Gate verified fidelity on all 53 touched paths; scratch recovery backup remains /tmp/bob-mac-restore-0ig_wzuq. Deleted polluted remote branch refs/heads/ci/precommit/4f12681e038ad03a8ecb1de466d2a1ae (af75f0912ead90bad77bd8a6c0886409b2b00bd1). Live master verified equal to restored SHA; fetched every advertised head/tag and no remote ref contains BAD (4 heads, 0 tags). SHA searches found citations on bob-cli-jf, bob-cli-jf.1.1, and bob-cli-j8.8, so this full mapping is recorded on each. Exact-SHA CI run 42813392077 remains pending; this note does not claim CI is green. Run: https://github.com/bobs-org/bob-mac-capture/actions/runs/42813392077

[2026-11-10T12:17:13Z · bob-cli-jf.1.1--1] POST-GATE CHECKOUT VERIFICATION 2026-11-10: Reused the rehearsed cleanup script in read-only survey mode and independently checked HEAD, all local refs, and every stash entry. Athena: 12 real Mac checkouts; Apollo: 6; Mac: 1. All 19 checkouts have zero refs/HEAD/stashes containing BAD. The five originally polluted branches now point to af604c6d9e05ec6440bfce5fa15ced97e388035c (athena linked workspaces 10/12/13, apollo linked workspace 11, Mac primary). Two unrelated dirty checkouts remain intact (athena workspace 15 and apollo workspace 32); no unique-work rebase or further reset was needed. Mac was reachable and clean on final resurvey. Linux docs caches were removed by the approved gate; Apollo has since recreated a cache with no BAD refs; Athena and Mac caches are absent. Full read-only JSON evidence is in /tmp/bob-cli-jf-restore-verify/{athena,apollo,mac}.json. No unresolved cleanup issue. All four advertised remote heads were fetched and audited, no tags advertised, no ref contains BAD, master exactly equals restored tip. epic-symbols reports no entries. No tracked source changes were made by this continuation; bob-cli clean base HEAD is 4219d70a75d81299cb9321bf194508abcbb96367. Remaining verification: just docs-check on that clean base plus exact-SHA macOS CI run 42813392077 (currently running), to be handed to a SASE monitor; only after results are assessed should this phase close.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-jf.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-jf.1.1.md) | [bob-cli-jf.1.1](bob-cli-jf.1.1.md) | 0 |
