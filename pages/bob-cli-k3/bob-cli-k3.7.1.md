# Bead: bob-cli-k3.7.1 — Obsidian album cards, live chips, headers, and navigation

[Bead Pages](../README.md) / [bob-cli-k3.7](bob-cli-k3.7.md) / bob-cli-k3.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-k3.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.7.md) · **Assignee:** `bob-cli-k3.7.1.land`
**Created:** 2026-11-11 23:10:17 EST · **Closed:** 2026-11-12 11:18:02 EST
**Plan:** [202611/album\_plugin\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_plugin_ui.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/album_plugin_ui.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 8 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_plugin_ui.md

<!-- sase:links:end -->

## Description

Complete bob-cli-k3.7 with report-driven album and record cards, album headers, correct parent and task-home pickers, and a tested, documented plugin deployment.

## Notes

[2026-11-12T15:38:30Z · bob-cli-k3.7.1.land] LAND TRIAGE of PROPOSED FOLLOW-UPs (k3.7.1.1-.5): (1) task-tag-marks.cjs 'session toggle and onload wiring' 2!==1 (.2#4, .3#2, .4#2, .5#1): not caused by this epic. Bisected to bank commit 4e4a580 (bob-cli-kd.6.1.4; kd is closed); a stack probe shows refreshBankMarks dispatching from a synchronous apiBankSubscribe during onload. Filed new task bob-cli-kw (ci, small). (2) The 200-link Live Preview timing budgets (.2#1, .4#2) are load flakes; the files pass in isolation on 3dc30c7. Corroborated the existing trackers with +1 on bob-cli-ki (keep-moving surface) and bob-cli-ju (off-clock link chips). (3) The strict docs-check link develop/plugins/validation.md:55 -> ../bob-vim-yank-flash.md#verification (.1#1/#4, .2#2/#5, .3#1, .4#3, .5#2) still reproduces on bob-cli 94897d50 + bob-plugins 3dc30c7, and is now the only strict warning (the two bob-cli anchors were repaired by 9662ce54). It is already tracked by bob-cli-kk, linked to active epic bob-cli-kb, and k3.7.1.1 already corroborated it, so no new task was filed. Declined: (4) note-ready startup-storm 3!==2 (.1#2, .2#1) no longer reproduces; test-ledger-tools-note-ready.cjs passes on 3dc30c7. (5) The npm test open-handle hang (.2#4, .3#2) no longer reproduces: dashboard-parity, date-marks, and day-strip-hosts each exit in 0-3 s on 3dc30c7.

[2026-11-12T15:38:45Z · bob-cli-k3.7.1.land] LAND VERIFY/INTEGRATE (so far): all five phase commits are on bob-plugins master (9c79123 album-data, bd6fc41 owner-cards, ed5e648 records-cards, c2f6834 album-header, 2d10fca album-navigation), and the plan APIs, constants, and wiring are present (apiAlbum*, 3 s sync debounce, fold-after-12, visited/watched_on chips, 'Name @stem/' copy, scoped record-property hide, lifecycle setup/teardown). The 129 focused album/navigation tests pass, and the real-bob fixture test passes against bob-cli master 94897d50. Post-start drift: bob-cli 1174a17b (bob-cli-kr.1) adds album list JSON fields (dated_notes, legacy, schema_fingerprint, per-field suggest/line/filled/default/min/max, choice count). They are additive, the plugin decoder still accepts them, and consuming them is bob-cli-kr.3's scope. de5c0e56 (the kr.2 update writer) is unrelated to the UI. Bank and mail plugin commits do not conflict. Deployment: phase 5 left the vault drifted, so I ran a normal bob plugins sync from 3dc30c7 without -F. It now shows 10 synced, 0 drift. epic-symbols are empty for k3.7.1 and k3.7. REMAINING: the plan's land-agent acceptance proof (album CDP e2e plus offline npm-test wrapper, real-Obsidian screenshot checks, and full gates) was never built. It is planned as a tale.

[2026-11-12T16:18:02Z · bob-cli-k3.7.1.land] Phases verified, drift integrated, follow-ups triaged (bob-cli-kw new; +1 bob-cli-ki, bob-cli-ju; bob-cli-kk existing). Album e2e: offline self-test passes; real-Obsidian CDP walkthrough PASS 35/35 (Reading+Live, light+dark, 375px). Artifacts: report file:explicit:9ae486976c079f219df059bc, shots file:explicit:6230ce612ee64dca3dd635e6 file:explicit:6d8b063162070659a9595460 file:explicit:87c126a8a0998ec9a8e7798 file:explicit:f9dffba616cbfcd014d78646 file:explicit:447ce6ff62f89f134cf87d73. Gates: build ok, validate 11/11, docs:check only known pre-existing validation.md:55 warning (clean-base identical), npm test only known clean-base failures, just check green on retry. Deployment: bob plugins sync 11 synced 0 drift.

## Dependencies

- **Blocks:** [bob-cli-kr.3](../bob-cli-kr/bob-cli-kr.3.md) ✓ · ⧖ 2026-11-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.7.1.land.md) | [bob-cli-k3.7.1](bob-cli-k3.7.1.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8cef0d5`](https://github.com/bobs-org/bob-cli/commit/8cef0d56c8c987de0d0acbc31d260b72c6c37953) | docs(records): link albums section to Obsidian Album cards page | [bob-cli-k3.7.1](bob-cli-k3.7.1.md) | 2026-11-12 11:22:46 EST |
| bob-plugins | [`bob-plugins@1b8982c`](https://github.com/bobs-org/bob-plugins/commit/1b8982cf4283d1a20615e3b1f8977cebe2627444) | feat(ledger-tools): add album UI acceptance e2e and verification docs | [bob-cli-k3.7.1](bob-cli-k3.7.1.md) | 2026-11-12 11:24:01 EST |
| bob-cli--plans | [`bob-cli--plans@48505cc`](https://github.com/bobs-org/bob-cli--plans/commit/48505cc0413332a3cba361aab1ac5ba3f1b53aa8) | docs(plans): mark album plugin UI epic and acceptance plans done | [bob-cli-k3.7.1](bob-cli-k3.7.1.md) | 2026-11-12 11:24:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k3.7.1.3][1] | Need parent epic DECISIONS that this phase must honor | 3 |
| read-by | [agent:bob-cli-k3.7.1.5][2] | Need parent epic scope and decisions | 1 |
| read-by | [agent:bob-cli-kr.3--1][3] | Need resolution after wait | 1 |
| read-by | [agent:dl--1][4] | Check whether this active plugin deployment epic owns the vault ignore recurrence | 1 |
| read-by | [agent:research.4b.cld][5] | Check child epic for plugin album header and schema card status | 1 |
| read-by | [agent:research.4b.gem][6] | Check child tasks under phase 7 | 1 |
| read-by | [agent:research.4b.grk][7] | Need child epic details for Obsidian album cards and schema rendering | 1 |
| read-by | [agent:research.4b.mus][8] | research record frontmatter Obsidian rendering | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.7.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.7.1.5/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kr.3.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.dl.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.cld/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.gem/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.grk/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.mus/README.md

<!-- sase:referenced-by:end -->
