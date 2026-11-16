# Bead: bob-cli-mc.2 — In-place tab-jump executor

[Bead Pages](../README.md) / [bob-cli-mc](README.md) / bob-cli-mc.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.4y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.4y.linker.w0.md) · **Assignee:** `bob-cli-mc.2` · **Size:** medium
**Created:** 2026-11-16 11:01:02 EST · **Closed:** 2026-11-16 11:59:59 EST
**Plan:** [202611/obsidian\_ctrl\_w\_numbered\_tab\_jump.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_numbered_tab_jump.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:b79ef7c12eaaec467009169b | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

actions: execute focus-tab plans losslessly (load if deferred, session check, setActiveLeaf, invariants, restore), fold the selectedTab fix through the move executor, and prove it on real Obsidian with a new e2e tabs group.

## Notes

[2026-11-16T16:57:54Z · bob-cli-mc.2] TAB JUMP E2E: athena xvfb-run /snap/bin/obsidian --only tabs 15/15 PASS (pass=true, skipped=0). Report file:explicit:b79ef7c12eaaec467009169b sourceSha 2e15ec3 plugin 2.83.2 appVersion None. Vectors: across-selected 3 → [ WP-A  WP-B' ] | [ WP-C*  WP-D ]; across-unselected 4 → [ WP-A  WP-B' ] | [ WP-C  WP-D* ]; same-split 1 → [ WP-A*  WP-B ] | [ WP-C' ]; pinned-are-tabs 1 → [ WP-A!*  WP-B ] | [ WP-C' ]; already-here 2 → [ WP-A  WP-B* ] | [ WP-C' ]; no-such-tab 7 → [ WP-A  WP-B* ] | [ WP-C' ]. Source split kept WP-B (currentTab 1) after jump to D. Undo round-trip PASS. Scroll: unselected long note 2929→2929, ephemeralPreserved=true, lostDomScroll=false — no getEphemeralState restore. Clip: tab 9 focused with fullyVisible=false (header left 664 / right 704 vs parent 344–624 width 280); guarded tabHeaderEl.scrollIntoView({block:nearest,inline:nearest}) is in the executor as the plan requires. PDF tiny.pdf viewType=pdf hasEditor=false. Stacked via setStacked [ WP-A*  WP-B  WP-C ]. Deferred reload focused WP-D.md markdown with editor. bob plugins sync copied bob-navigation-hotkeys/main.js +182/-6. 🔒 report.json

[2026-11-16T16:58:20Z · bob-cli-mc.2] PROPOSED FOLLOW-UP: thirteen-clip still fullyVisible=false after the plan's guarded tabHeaderEl.scrollIntoView({block:nearest,inline:nearest}) — header left 664 vs parent 344–624 under an artificial 280px clip that may not use a native overflow scroller. Finish/visual can try inner-container scrollLeft if a native overflow strip still clips the destination numeral.

[2026-11-16T16:59:59Z · bob-cli-mc.2] Verified: focus-tab executor mixin (loadIfDeferred, armed.isCurrent, setActiveLeaf {focus:true}, invariants, restore+Notice, serialized queue, guarded scrollIntoView); selectedTab rollback via windowPrefixSelectedLeaf; 17 tab-actions + 21 prefix-actions unit tests pass including failed-join currentTab reselect; athena xvfb /snap/bin/obsidian tabs group 15/15 PASS (file:explicit:b79ef7c12eaaec467009169b); scroll 2929 preserved so no ephemeral restore; clip fullyVisible=false so scrollIntoView is in the executor; dormant until prefix; no version bump; bob plugins sync copied main.js.

## Attachments

- 🔒 report.json · application/json · 6.25098 KiB (private attachment)

## Dependencies

- **Depends on:** [bob-cli-mc.1](bob-cli-mc.1.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mc.4](bob-cli-mc.4.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mc.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mc.2/README.md) | [bob-cli-mc.2](bob-cli-mc.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b61b55c`](https://github.com/bobs-org/bob-plugins/commit/b61b55cc6b7e7fd321398b5f5a4930278183fa85) | feat(navigation): add in-place tab-jump executor | [bob-cli-mc.2](bob-cli-mc.2.md) | 2026-11-16 12:02:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mc.2][1] | Need full notes, decisions, design, and remaining work | 7 |
| read-by | [agent:bob-cli-mc.3][2] | Need actions phase status to avoid conflicts | 1 |
| read-by | [agent:bob-cli-mc.4][3] | Need GO LIVE e2e run pattern from closed actions phase | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mc.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mc.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mc.4/README.md

<!-- sase:referenced-by:end -->
