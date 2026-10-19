# Bead: bob-cli-9y.2 — Clean up duplicates and stale ideas in place

[Bead Pages](../README.md) / [bob-cli-9y](README.md) / bob-cli-9y.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.124](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.124.md) · **Assignee:** `bob-cli-9y.2` · **Size:** medium
**Created:** 2026-10-19 16:26:36 EDT · **Closed:** 2026-10-19 16:43:22 EDT
**Plan:** [202610/sase\_hub\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/sase_hub_split.md)

## Description

hub-cleanup: in the live vault, cancel merged and duplicate tasks while carrying their details to survivors. Delete stale Future Work bullets, record contradiction and check notes, then reconcile and sync.

## Notes

[2026-10-19T20:43:22Z · bob-cli-9y.2] Hub-cleanup landed in the live vault (athena commits 12e138fc, ce0b201c, adb3fc01). `bob task reconcile` regrouped sase.md (14 cancels moved into Done & Canceled; 23 done/canceled total) and sase_pre_blog.md (1 cancel). `bob vault-sync` is clean (HEAD=origin/master adb3fc01, no conflicts). No --epic-symbol leftovers.

Cancels (snapshot line → live title):
- Exact dup: sase_pre_blog second “Remove `branch_or_workspace_name` dependency!” (first kept)
- [1] L282 Always [[sase#^grill]] epics! → [[sase#^grill]]
- [2] L745 “sase” rename idea: “bai”; L1027 Sase rename idea: “sal” → [[sase#^rename-candidates]] (L126 survivor)
- [5] L664 Sase needs a way to shut down all agents… → [[sase#^restart-survival]] (earlier L1001)
- [7] L1278 Explore tmux instead of headless CLI agents? → [[sase#^tmux-mayor]] (L199)
- [8] L1275 hermes chat --oneshot → [[sase_pre_blog#^hermes-llm]]
- [10] L825 cpu=<N>.<duration> %wait kwarg → [[sase#^wait-for-load]]
- [11] L1035 xprompt freshness labels → [[sase#^freshness-notifications]] (L740)
- [13] L554 %name directive → [[sase#^better-name-ow]] (earlier L806)
- Cross-note: L1105 /sase_stitch how_to_git_commit.md → [[sase_memory#^commit-to-stitch]]
- Cross-note: L879 beads specify xprompt → [[sase_better_tasks#^task-type-prompts]]
- Cross-note: L123 require artifact-create reason → [[sase_art_links#^artifact-create]]
- L1096 open linked repo as external (superseded: sase repo open redirects)
- L1270 plans lost on memory confirmation (own sub-bullet: wasn’t a big deal)

FW/Req deletions (snapshot): L1357 dup materialize-replay; L1418 sawi; L1391 PIW copilot; L1372 hidden-agents; L1385 black wrapping; L1409 %hide; L1425 ,X relaunch; L1338 /sase_run + children; L1333 dyn-agent-fams; L1335 apollo remote; L1340 launch-hitl; L1341 install codex; L1343 sidecar sdd/; L1347 single SASE.md; L1348 pylimit; L1352 audio-artifacts; L1365 pyvision.md; L1390 research _cld/_cdx; Req L1430 Antigravity; L1360 sdd/decisions; L1363 sdd/tales; Req L1431 ChangeSpec analogy; Req L1432 sdd/events ^8ff48a.

Kept: L1359 ChangeSpec→PARENT keymap; L833 lumberjack/chop; L1134 Remove ALL “SDD”; L80 Files→Attachments; [9] L57+L121; [14] L46+L353+L355 (CHECK only); [6] Codex/Claude reminders.

Notes added:
- DECIDE on L918 (hidden vs %hide; ship one) and L756 (skill bundles vs sase skills read vs “do memory webs even need to exist?”)
- CHECK on L295 + sase_art_links research-lead (artifact-read derived links); L353 plan attribution 0; L355 TUI uses sase stats 0f2052be6a; L472 related [[sase_post_blog#^auto-wait-for-vars]]; L1039 ,X last-launched shipped, remainder is any selected agent; L1148 tui_perf.md still a child of tui.md; L1208 tailnet.md covers Mac SSH; FW L1349 plans sidecar / related L1152; FW L1373 not adopted (commit obligation); FW L1374 generated macro skills
- Split malformed FW L1342 into “Implement PR comment reading!” and “Create /sase_comments and add mentors…” [created::2026-06-08]

Deleted-anchor inbound leftovers (historical, left in place): done/sase_done.md → ^dyn-agent-fams (acceptable); 2026/20260614.md → ^audio-artifacts; 2026/20260531.md → ^8ff48a.

## Dependencies

- **Blocks:** [bob-cli-9y.3](bob-cli-9y.3.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9y.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9y.2/README.md) | [bob-cli-9y.2](bob-cli-9y.2.md) | 0 |
