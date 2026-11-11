# Bead: bob-cli-ji.8 — Finish private event notes — correctness fixes and the missing extras

[Bead Pages](../README.md) / [bob-cli-ji](README.md) / bob-cli-ji.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ji.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.land.md) · **Assignee:** `bob-cli-ji.8.land`
**Created:** 2026-11-10 22:31:45 EST · **Closed:** 2026-11-11 02:45:41 EST
**Plan:** [202611/finish\_private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_private_gcal_event_notes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/finish_private_gcal_event_notes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_private_gcal_event_notes.md

<!-- sase:links:end -->

## Description

Close the gaps the bob-cli-ji land audit found in `bob gcal note`: previews that show a stale note, options that are silently swallowed as note text, orphan clear commands that fail, an account-blind note fold, held rows reported as updates, and an incomplete extras phase (`-e`, `-A`, the doctor `notes` check, and the fragile-description hint). Every fix ships with tests, and the JSON stays compatible with Bob Mac Capture.

## Notes

[2026-11-11T06:34:24Z · bob-cli-ji.8.land] FOLLOW-UP TRIAGE: Read every note on ji.8.1-.4. ji.8.2 #1 (cross-host same-second gcal.note ties): declined as a defect/new task; parent approved Shared design explicitly requires deterministic (ts, host, path, line) order like load_series_roots, and journal::load_notes implements it. A monotonic/distributed ordering redesign is outside accepted scope and has no demonstrated requirement. ji.8.3 #1 and ji.8.4 #1 (Mac fixtures): one duplicate proposal, retained as this epic integration work, not deferred to a task. On linked Mac e638795 exactly 15 of 18 JSON copies differ: applied, both_scopes, cleared, google_reasons, inherited_reasons, invalid, preview, preview_match, saved, saved_elsewhere, saved_sync_failed, series_scope, show, show_preview_match, unchanged. ambiguous, list_all, waiting_states are already equal; phase notes overstate the changed set. ji.8.3 #2 (docs budgets): corroborated existing bob-cli-jz and bob-cli-h9 with current canonical counts 6036/6088/6060/6149 at Mac e638795; plugin overage remains covered by jz, not independently recounted. Same-type searches, recent-task sweeps, broader search, and all 12 active epics inspected; no distinct unrelated new task warranted.

[2026-11-11T06:35:03Z · bob-cli-ji.8.land] LAND AUDIT at ba7a1c90: Read all four child scopes/notes, both linked plans, accepted private-note decision, all four phase commits (54e650d1, 9660397d, b706f559, ba7a1c90), changed engine/select/write/extras code and test coverage. Account-aware fold, pre-note exact clone, held rows, provenance pruning, alias stripping, read modes, write spans/suggestions, adoption/fragile rules are present. DECISIONS remain auto_sync=yes and Google read-only; no memory changes. Fetched origin/master equals HEAD; no non-epic commits since first ji.8 commit and no PR base divergence. Epic symbols empty; no symvision recipe. Remaining source-confirmed work: (1) rewrite_note_tail does not recognize an explicit -- after implicit TEXT; compiled unmodified functions in a small rustc probe: [-i,e1,@family,--,-d] becomes [-i,e1,-d,--,@family,--], violating literal-tail contract. (2) -e -d passes initial checks, empty editor sets prepared.clear=true, write_one clear path unconditionally appends/syncs; direct -c -d is correctly rejected. (3) current_scope_text prompts for a recurring scope but does not retain it in prepared args; write_one prompts again or auto-selects a different clear scope, and empty recurring edits without an existing note error before the unchanged branch. (4) doctor notes accumulates per-issue fixes then discards all but first; unresolved series fix prints -e -s series -i <master> although only clear handles a bare master. (5) clear_by_key also handles live bare masters but skips writer-host immediate sync and claims the event is gone, leaving existing occurrence rows stale. (6) 15 Mac JSON copies need refresh, as triaged. These stay epic work in a medium tale which owns this closeout and re-audits parent bob-cli-ji. No full cargo check was run in this audit; no current checkout binary exists, and installed bob is older. Only the exact-source argv probe was executed; editor/doctor/series issues are established by control-flow review and require regression tests.

[2026-11-11T07:45:41Z · bob-cli-ji.8.land--2] TALE LANDING VERIFIED (plan 202611/finish_gcal_note_landing.md): (1) rewrite_note_tail honors first explicit -- after implicit TEXT: one clap separator, rest verbatim; pre-pass vectors + fake-gog CLI regression assert saved/preview text and mutation count. (2) Edit/adopt resolves scope once through seed/validate/preview/save/clear; empty -e -d previews without mutating (unchanged for both-empty, event note preserved for series-empty); -A existing-note guard under resolved scope; fake-editor regressions with BOB_GCAL_ASSUME_TTY, no live vault/Google. (3) doctor notes keeps one remedy per issue kind (newline-separated) and prints runnable occurrence-edit or series-key clear for unresolved series routes; run actual printed command in tests; 25-lookup cap and outage-vs-notfound preserved. (4) Bare-master -c -s series reuses normal clear path via occurrence so rendered days sync immediately (live-aware by-key fallback); true missing-master clears remain by key; live-master test asserts row reverts to Google values with hand-edit preservation and no future notes; off-writer/sync-failure honest status. (5) docs/gcal-notes.md documents cleared status. (6) Mac fixtures: 37b0e68 refreshes 15 JSON copies; all 18 agree (diff clean except README). CHILD NOTES/DECISIONS: ji.8.1-.4 closed; follow-up triage stands (timestamp-tie declined, fixture proposal retained here, jz/h9 docs budgets corroborated); auto_sync=yes and Google read-only honored; no memory/Cargo/version/CHANGELOG changes; no epic-symbols. DRIFT: bob-cli 05ec8253==origin/master (one commit since ba7a1c90 audit base, no non-epic commits); Mac 37b0e68==origin/master (one commit since e638795). TESTS: just check exit 0 (3m39s); prepass 11 pass; gcal_note_cli 39 pass (7 new); gcal_auth 62 pass (1 new); gcal_notes 21 pass; lint pass; fmt clean; docs-check only 5 known jz/h9 word-budget failures; Mac portable-check 2468 pass 0 fail; macOS CI run 42977953644 GcalNote suites 69 pass, macos-ci-check snapshot run 42979134697 red only on 3 pre-existing CaptureAliasTipPanelTests timeouts (same as e638795 run 42950195338), tracked in bob-cli-jx with +1 this turn, no new task.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.8.land.md) | [bob-cli-ji.8](bob-cli-ji.8.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`05ec825`](https://github.com/bobs-org/bob-cli/commit/05ec8253f144ed6e5947f659a17eb50dea45d251) | fix(gcal): finish private note landing boundary cases | [bob-cli-ji.8](bob-cli-ji.8.md) | 2026-11-11 02:12:55 EST |
| bob-mac-capture | [`bob-mac-capture@37b0e68`](https://github.com/bobs-org/bob-mac-capture/commit/37b0e68a1dcfc24e6b7dca75a3074daf13f887b0) | test(gcal-note): refresh contract fixtures from bob-cli | [bob-cli-ji.8](bob-cli-ji.8.md) | 2026-11-11 02:13:41 EST |
| bob-cli--plans | [`bob-cli--plans@469f92b`](https://github.com/bobs-org/bob-cli--plans/commit/469f92b162c691f521e78289e735c043cfeaef02) | docs(plans): mark private event note plans done after ji.8 landing | [bob-cli-ji.8](bob-cli-ji.8.md) | 2026-11-11 02:48:00 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.8.1][1] | Need epic DECISIONS that this phase must honor | 1 |
| read-by | [agent:bob-cli-ji.8.2][2] | Need epic scope, DECISIONS, and design | 1 |
| read-by | [agent:bob-cli-ji.8.4][3] | Need parent epic DECISIONS and phase split | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.4/README.md

<!-- sase:referenced-by:end -->
