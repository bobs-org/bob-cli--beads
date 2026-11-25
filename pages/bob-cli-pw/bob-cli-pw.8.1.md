# Bead: bob-cli-pw.8.1 — Mac meeting notes filing and Meetings library scope

[Bead Pages](../README.md) / [bob-cli-pw.8](bob-cli-pw.8.md) / bob-cli-pw.8.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pw.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.8.md) · **Assignee:** `bob-cli-pw.8.1.land`
**Created:** 2026-11-24 23:55:02 EST · **Closed:** 2026-11-25 07:27:33 EST
**Plan:** [202611/mac\_meeting\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_meeting_notes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/mac_meeting_notes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_meeting_notes.md

<!-- sase:links:end -->

## Description

Complete bob-cli-pw.8 with guarded clipboard meeting-notes filing from Capture and its agenda, a first-class Meetings kind in Bob Refs, and verified macOS CI.

## Notes

[2026-11-25T09:29:25Z · bob-cli-pw.8.1.land] LANDING AUDIT (2026-11-25): Read all three child beads and every note, the child plan and original Mac phase. Reviewed Mac commits c8692ed3, 7b1fcc05, 1dea9a71, b693bf56, 36b3e4aa, 3b443fe6, 284417d7 and CLI bcf0566b plus current source/fixtures. Existing wire transport pins the event/hash/options, preserves configured status, decodes exit-2 choices, separates filed/queued, and keeps backend ownership; Meetings kind/Command-6 preserves existing scopes. No memory or private-vault work was introduced, honoring no/no memory decisions; first-use scaffolding=rehang and recap_scope=full remain upstream. Independently fetched CI snapshot 3f4fcf361976aac2f1c69c168564bc94f40697b4: its tree exactly matches Mac HEAD 284417d7 (tree 4263a2ce0ef40a450eefa9e67ae2f6b613ee520b). GitHub run 45580348007 reports all required macOS steps success. Prior compile/menu failures are repaired. No unrelated commits landed in bob-cli or Mac between this epic start/first commit and current master; both checkouts equal fetched origin/master. epic-symbols for pw.8.1 and pw.8 returns no entries. Closure is blocked by native integration gaps, detailed in the remaining-work tale: Change meeting never opens the chooser; same-day rows share ForEach path IDs; completed x/DONE agenda rows are incorrectly suppressed; parent/replacement Return and Escape do not follow visible state; native leave/reconfiguration can hide or lose in-flight receipts; entry gating covers only the status menu; refresh callbacks hit agenda twice and omit explicit Refs invalidation; transcript presentation reads shape rather than transcript. Native model/controller/visual acceptance coverage is missing. These are epic work, not external follow-ups.

[2026-11-25T09:29:32Z · bob-cli-pw.8.1.land] FOLLOW-UP TRIAGE COMPLETE: pw.8.1.1 #1 proposes protocol and plugin API budgets; pw.8.1.2 #1 proposes plugin API and navigation budgets; pw.8.1.3 #1 combines protocol, keyboard, plugin API, navigation. Used sase_new_task, all-status searches, last-week task sweep, active-epic scope/history review. Canonical count_words disproves the reported clean-base Mac counts: 7d369ae8 protocol=5997 and keyboard=5978; HEAD 284417d7 protocol=6308 and keyboard=6019. Both regressions are caused by this epic and remain in its repair tale; corroborated existing h9 and jz without outsourcing repair. At plugins c1819664, unchanged plugin-apis=9287/8000 and navigation=6029/6000: corroborated ob (advisory develop-page headroom) and jz (fatal reference-page cap). Declined new duplicate tasks; declined a separate CI failure for plugin-apis because that budget is only a warning. No causally related currently-active epic owns a new plugin-source increment in this report. Earlier Refs assertion is already fixed by Mac 36b3e4aa and the matching-tree green CI, so it is not remaining epic work. No other PROPOSED FOLLOW-UP entries exist.

[2026-11-25T12:27:10Z · bob-cli-pw.8.1.land--3] GREEN macos-ci-check (monitor 91z703): https://github.com/bobs-org/bob-mac-capture/actions/runs/45608004005
Snapshot SHA e7b7bb3cea928247eacb4b11b8167cafef72604a on base 284417d783db8a2c4626045bbc4e17458ee670b8. Required macOS 26 SwiftPM steps passed (lint, build, test, render-fixtures upload, bundle, plist/signature, launch smoke, install/reinstall). Hang-sample upload skipped (no hang).

origin/master drift: bob-mac-capture HEAD 284417d7 equals fetched origin/master; landing overlay remains uncommitted in this checkout. bob-cli workspace HEAD bcf0566b is one commit behind origin/master 5ab392a1 (chore(dev): bob-host-currency bold-drawer probe), unrelated and not pulled.

Visual inspection of render-fixtures artifact MeetingNotesDesignTests PNGs (all 24 present: preview/chooser/parent/replace/filed/queued × 720/480 × aqua/darkAqua). Invented content only (Juniper Systems planning, Orchard design review). Preview shows title, span, destination, status, match evidence, Change meeting, TL;DR, next steps, section/decision counts, transcript omitted, reading-status picker, File/Re-preview/Back. Chooser lists two distinct rows with filter and a check on the selected meeting. Parent lists Team (checked) and Studio. Replace offers Open existing / Review replacement preview (checked) / Keep existing. Filed shows the note path, Open note, Done, and orange source-saved / remote-unavailable. Queued shows vault is busy, scan next-step, and orange re-root skipped. DarkAqua inverts tokens without clipping. 480 keeps actions readable; replace wraps the destination path.

[2026-11-25T12:27:33Z · bob-cli-pw.8.1.land--3] Closed bob-cli-pw.8.1 after original landing audit plus native repair closeout.

Original implementation audit (2026-11-25): children 8.1.1–8.1.3 closed; Mac HEAD 284417d7 plus CLI bcf0566b already had guarded JSON transport (event/hash/options pin, configured status, exit-2 choices, filed vs queued, backend ownership) and Meetings kind/Command-6. No memory edits or first-use vault ops. Prior compile/menu failures repaired. Closure was blocked on native integration gaps recorded in the remaining-work tale.

Repaired native flows in the uncommitted Mac overlay: Change meeting waits for previewReady plus the three-row list then showChooser; chooser ForEach uses distinct row identity and skips tokenless rows (list-same-path.json). Write ownership stays on the session (leave/reconfigure cannot hide an in-flight write). Agenda Notes shows completed x/DONE rows and suppresses cancelled. Parent/replace Return and Escape follow visible state. Capability gating hides Command-M, status-menu File Meeting Notes, and agenda Notes when ref meet is unsupported. Preview presents transcript fields from the report. MeetingNotesDesignTests cover preview/chooser/parent/replace/filed/queued at 720/480 aqua+darkAqua. Item-start double-dot rewrite asserts asks.count >= 1. RefsStores cap tests seed one codec write of 2004 rows then one public append/apply so prune still runs without 2005 fsyncs.

Integration review: Command-M, status menu, and agenda Notes enter one sheet; capture draft and first responder restore; Event Note remains distinct; auto-match and agenda preselection both reach guarded filing; clipboard replacement re-previews; queued receipts never offer Open note.

Tested trees: bob-cli just check; Mac scratch typecheck-tests (BobMacCaptureTests, BobMacCaptureInstallHelperTests, CaptureCoreTests, RefsCoreTests); Athena swift test --filter MeetingNotes and RefsStoresTests (15 passed in 0.171s; cap tests 0.025s/0.032s); protocol.md and keyboard.md canonical count_words 5998/6000.

Green macos-ci-check: https://github.com/bobs-org/bob-mac-capture/actions/runs/45608004005 snapshot SHA e7b7bb3cea928247eacb4b11b8167cafef72604a. Visual inspection of all 24 MeetingNotesDesignTests PNGs recorded on this bead.

docs-check known-unrelated plugin budgets remain at navigation 6029/6000 and plugin-apis 9287/8000 advisory. Follow-up outcomes: h9 (protocol budget, snoozed/+19) and jz (keyboard/nav reference cap, ready/+19) stay the owners for Mac reference overages; ob remains the plugin-apis/nav headroom feature. No new tasks. epic-symbols bob-cli-pw.8.1 listed none. justfile has no symvision recipe.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pw.8.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.8.1.land.md) | [bob-cli-pw.8.1](bob-cli-pw.8.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@3931c30`](https://github.com/bobs-org/bob-mac-capture/commit/3931c308b376904d063208e13f793691396e58cc) | fix(meetings): repair native Meeting Notes landing flows | [bob-cli-pw.8.1](bob-cli-pw.8.1.md) | 2026-11-25 07:30:34 EST |
| bob-cli--plans | [`bob-cli--plans@79c2b32`](https://github.com/bobs-org/bob-cli--plans/commit/79c2b325fda4eeb293391e9aed35ed5910444545) | docs(plan): mark mac\_meeting\_notes epic plan done | [bob-cli-pw.8.1](bob-cli-pw.8.1.md) | 2026-11-25 07:31:58 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pw.8.1.land--3][1] | Need epic note and current status before recording CI evidence and closeout | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pw.8.1.land.md

<!-- sase:referenced-by:end -->
