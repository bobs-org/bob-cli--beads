# Bead: bob-cli-pl.4.1 — Local Area and Project cards

[Bead Pages](../README.md) / [bob-cli-pl.4](bob-cli-pl.4.md) / bob-cli-pl.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.4--1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.4.md) · **Assignee:** `bob-cli-pl.4.1.land`
**Created:** 2026-11-24 09:51:08 EST · **Closed:** 2026-11-24 15:39:43 EST
**Plan:** [202611/local\_home\_cards.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/local_home_cards.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/local_home_cards.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:450a479cc73a6f86a9c661cc | attached via sase artifact create --bead |
| related | file:explicit:cb88c4643f511cce58e35444 | attached via sase artifact create --bead |
| related | file:explicit:d802ce1e232a7fed3b693268 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/local_home_cards.md

<!-- sase:links:end -->

## Description

Complete bob-cli-pl.4 with locally painted Area and Project title cards, native Properties still visible, unchanged project-task interaction, and verified real-Obsidian behavior.

## Notes

[2026-11-24T19:12:40Z · bob-cli-pl.4.1.land] LAND FOLLOW-UP TRIAGE (all five proposals): pl.4.1.1 #2 docs mount collision corroborated existing bob-cli-it; pl.4.1.3 #3 reports later docs:check green (447 pass, 1 skip), so no remaining epic blocker or new task. pl.4.1.1 #3 protected vault deploy declined as a new task: pl.4.1.2 #2 records landed-commit deployment and pl.4.1.3 #3 records sync 0 copied/0 skipped/34 unchanged, resolving the operational block. pl.4.1.1 #4 event-link-times and frees-marks timing flakes corroborated existing node-specific bob-cli-km and bob-cli-io (phase evidence attributed; no fresh broad-suite reproduction claimed). pl.4.1.3 #2 cache-update failures declined: b4023b85 already adapts freshness and note-ready test listeners to the home-card subscription; both pass now within this lander 82/82 focused suite on 71cf808a. Its alleged clean base 21bbd30c already contained this epic, so it never established independence. pl.4.1.3 #1 Task Card/editor refresh proposal is not established as a distinct independent product defect: alleged clean base b5f2f6c1 is the epic mount commit; the runner uses the still-unfocused shared trust helper from bob-cli-ox, and later commit 71cf808a deletes the Task Card assertion. Recorded diagnostic on ox without claiming confirmed causality; declined a new speculative duplicate. Restore the real Task Card/control checks with verified main-window focus as epic acceptance work, retain results, and triage only a residual independently reproduced defect. No new task beads needed after all-status searches, last-week task sweep, and active-epic scope review.

[2026-11-24T19:15:14Z · bob-cli-pl.4.1.land] LAND AUDIT: Reviewed the epic (no preexisting own notes), all 5/2/3 notes on phases .1/.2/.3, parent phase pl.4, both linked plans, product model/DOM/host/foot/shared-kit code and all four child commits 5717d518/b5f2f6c1/21bbd30c/71cf808a. Decisions honored: local cards, no structure counts, native Properties visible, no memory changes or later editor/report/takeover scope. Intervening bob-plugins b4023b85 retires duplicate project writers and fixes home-event test fan-out; preserve it. Bob-cli drift through 3deee354 adds home settings validation/contract and retired-count deletion plus independent meetings/Gmail work; local chip validity needs parity with that contract. Current 82/82 focused home-card/offline/cache suites pass, but direct probes reproduce: [] offclock_types plus true offclock paints ignored off-clock; mixed invalid clock list silently filters entries; numeric task_type paints #42; mapping task_refresh paints review [object Object]; a two-space nested ^prj supplies terminal lifecycle; negative inbox API answer is overridden by filename fallback. Host type hue calls wrong/nonexistent taskThemeOf rather than api.themes.hueFor. Host lifecycle/source boundary tests and real-app matrix are incomplete; 71cf808a removes Task Card/no-spawn assertions; clock constant is not applied; collapse/drawer/settings/fail-open/denied-context and retained inspected screenshot proof are missing. New medium tale sase_plan_local_home_cards_finish.md covers only those repairs and finishes this landing, including parent phase pl.4. Epic and parent phase remain open. Both epic-symbols scans currently empty; no symvision recipe currently available. All five follow-up proposals are dispositioned in the preceding triage note.

[2026-11-24T20:39:43Z · bob-cli-pl.4.1.land] Landed local Area/Project cards in bob-plugins on 71cf808a plus this tale's uncommitted host/model/e2e repairs. Preserved intervening b4023b85 (retired project count writers + home-card test fan-out). Source/drift: product stays in bob-ledger-tools 249b/249d; no Rust, no memory, no report-backed counts, native Properties remain visible, kit keys stay bare `-` drawer and `+` Property Editor.

Tests: focused home-card model/host/offline e2e 34/34; identity/title/host/foot + freshness + note-ready 131/131 earlier this landing; bob-cli `just check` green; plugin `npm run build` unchanged after last fragment rebuild; `bob plugins sync --repo <bob-plugins> --no-pull` copied bob-ledger-tools main.js (1 copied / 0 skipped / 33 unchanged) without `-F`. Isolated event-link-times and frees-marks 25ms budgets still fail under full `npm test` concurrency and pass isolated; corroborates bob-cli-km/io, assertions left intact.

Real-app: athena xvfb-run `scripts/obsidian-home-cards-e2e.cjs` PASS (75 checks, 28 inspected screenshots). Report file:explicit:cb88c4643f511cce58e35444 ; 28-shot archive file:explicit:d802ce1e232a7fed3b693268. Task Card restored via live `editorCallback` plus isolated stub `~/.config/bob/config.yml`; Escape/q/Ctrl+[ close; WIP fixture unchanged; completion uses complete_plan.md. Collapse reset before inventory; vim stays on for foot `-`.

Follow-ups (lander triage, carried forward):
- pl.4.1.1 #2 docs mount collision: corroborated bob-cli-it; no new task.
- pl.4.1.1 #3 protected deployment: resolved by later syncs including this 1-copy deploy; no task.
- pl.4.1.1 #4 timing flakes: corroborated bob-cli-km and bob-cli-io.
- pl.4.1.3 #2 cache-update failures: resolved by b4023b85; no task.
- pl.4.1.3 #1 Task Card/editor refresh: restored here with verified main-window focus and editorCallback; no residual independent product defect, no new task.

epic-symbols empty. just symvision recipe absent in bob-cli and bob-plugins. plan:202611/local_home_cards.md and plan:202611/local_home_cards_finish.md set status: done.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.4.1.land.md) | [bob-cli-pl.4.1](bob-cli-pl.4.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@45697ae`](https://github.com/bobs-org/bob-plugins/commit/45697ae018dbeb60fd687890faccb781196c3a42) | fix(home-cards): finish local Area and Project card landing | [bob-cli-pl.4.1](bob-cli-pl.4.1.md) | 2026-11-24 15:42:08 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.4.1.2][1] | Need parent epic scope for mount-foot | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pl.4.1.2/README.md

<!-- sase:referenced-by:end -->
