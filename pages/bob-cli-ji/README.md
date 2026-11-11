# Bead: bob-cli-ji — Private event notes for Google Calendar events

[Bead Pages](../README.md) / bob-cli-ji

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.3z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.3z.linker.w0.md) · **Assignee:** `bob-cli-ji.land`
**Created:** 2026-11-10 05:59:46 EST · **Closed:** 2026-11-11 02:46:36 EST
**Plan:** [202611/private\_gcal\_event\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/private_gcal_event_notes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/private_gcal_event_notes.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-k0][2] | Epic that accepted the single badges-hash cost for private event notes |
| related | [bead:bob-cli-k1][3] | Epic that shipped event and series note scopes |
| related | [bead:bob-cli-k2][4] | Epic that added gcal.row note provenance the tooltip would read |

_Plus 8 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/private_gcal_event_notes.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-k0/README.md
[3]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-k1/README.md
[4]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-k2/README.md

<!-- sase:links:end -->

## Description

Bryan can give any Google Calendar event (including events other people own and invitations he has not answered yet) Bob-only metadata at RSVP time: `@route`, `#off`/`#on`, `-30 reason`, `+15 reason`, and prose. He can write it from the CLI, over SSH, or from Bob Mac Capture. The metadata lands on the event's Event Task exactly as if those lines were in the Google description, and it beats that description field by field. Bob never writes to Google: it validates notes at write time, previews them faithfully, and never drops one silently.

## Notes

[2026-11-10T20:12:49Z · bob-cli-js.land] DISCOVERED ISSUE: just check / just lint fails at cargo clippy on master 947f24ff with 4 deny-level lints, all in this epic's gcal code: clippy::len_zero at src/native/gcal/note/write.rs:177 (note.errors.len() > 0) and clippy::collapsible_if at src/native/gcal/note/write.rs:1181 and :1421 (both from cf7c0605, bob-cli-ji.4), plus clippy::collapsible_if at src/native/gcal/doctor.rs:357 (c8934b93, bob-cli-ji.5). Because clippy fails at the lib level, cargo test never runs under just check. First proposed by bob-cli-js.3 note #2 (PROPOSED FOLLOW-UP); reproduced by the bob-cli-js land agent with just check on 2026-11-10 (exit 101, 'could not compile bob-obsidian (lib) due to 4 previous errors'). Fix: replace the length check with !note.errors.is_empty() and collapse the three nested ifs (let-chains), then rerun just check.

[2026-11-11T00:14:11Z · bob-cli-jt.land] DISCOVERED ISSUE: Landing bob-cli-jt, triaging jt.1 notes #3 and #4. Two stale test expectations are causally owned by this epic: a2809a1d (ji.2) added gcal-note in src/native/catalog/table.rs, but tests/cli/catalog.rs:42 still expects 88; current land check 31d25bfee9dd8db6b2887c2a6f3d7f41 on 4c1f7dde reproduces protocol_1_parses_with_schema_version_one failure (catalog is 89). Existing task bob-cli-de also tracks this recurring assertion drift. c8934b93 (ji.5) added the doctor notes check, but tests/gcal_auth.rs::doctor_json_healthy_setup exact ID list at line 1094 still omits notes; jt.1 reproduced that on clean base. Update the catalog contract assertion and doctor healthy expectation without removing the new product behavior. The four gcal deny-level clippy findings from jt.1 note #2 are already fixed in 4c1f7dde; this landing check passed clippy. Evidence file:explicit:5d919abc2555b8f911456244

[2026-11-11T00:17:45Z · bob-cli-jt.land] Runtime confirmation of the jt lander DISCOVERED ISSUE: just check 31d25bfee9dd8db6b2887c2a6f3d7f41 completed on 4c1f7dde, exit 101, with exactly the catalog 89-vs-88 and doctor_json_healthy_setup notes-ID expectation failures described above. All other test targets and Clippy passed. Completed evidence: file:explicit:a7ca20870803705cc70efee4.

[2026-11-11T03:27:47Z · bob-cli-ji.land] FOLLOW-UP TRIAGE (bob-cli-ji land agent): (1) docs-check word-budget overages (ji.1 #1, ji.2 #1, ji.3 #1, ji.4 #1, ji.5 #1, ji.6 #7): not caused by this epic; json-outputs.md is back under budget since 891fa3e4, and the mounted Mac pages are already tracked by bob-cli-jz (which cites ji.2 #1) and bob-cli-h9, so no new bead. (2) ji.6 #1 glossary term Private Event Note: declined. The reviewer chose memory_glossary=no, and decisions:private-event-notes-beat-google-per-field already carries the 'private event note' aliases, so a glossary strand would duplicate it. (3) ji.6 #2 badge-hash split -> new feature bob-cli-k0. (4) ji.6 #3 Google Keep phone path: declined. The plan made it conditional on phone RSVPs turning out to be common, there is no such evidence yet, and the guide documents the gcal.colors stopgap. (5) ji.6 #4 this-and-following scope -> new feature bob-cli-k1. (6) ji.6 #5 Ledger Tools pill tooltip -> new feature bob-cli-k2. (7) ji.6 #6 RSVP from Bob: declined as a task. It would reverse the accepted decision bob-gcal-is-read-only-and-proposes-once, so it needs Bryan's own decision rather than a discovered-work bead; the reopen condition is already recorded in decisions:private-event-notes-beat-google-per-field. The bob-cli-ji.7.1 follow-ups were already triaged by its land agent (bob-cli-jx, jy, jz, h9, jc). Epic notes #1-#3 (clippy, catalog 89, doctor notes ID) were fixed by 4c1f7dde/85e618d8; just check on 85e618d8 passed: 10457 tests, 0 failed.

[2026-11-11T03:30:30Z · bob-cli-ji.land] LAND AUDIT (bob-cli-ji land agent): The epic is not complete. Verified OK: all phases closed; DECISIONS honored (auto_sync=yes writer-host sync; cmd_e Mac chord via bob-cli-ji.7.1; memory_record decision strand plus superseded-in-part marks; no glossary strand). Engine/hardening tests are present, and just check on 85e618d8 passed. Integration: the 15 non-epic commits since 4219d70a (capture/notebooks/stats/periods/freshness) neither conflict with nor duplicate this feature; 891fa3e4 only moved note.rs prepass tests. Remaining epic work found by reading the source: (a) lookup_exact clones google_event after apply_notes, so -i/URL previews and -c show the stale note, and cleared.json locks this in; (b) the argv pre-pass swallows options after the first directive (a trailing -d saves instead of previewing); (c) printed orphan clear commands fail; any gog error becomes a not_found orphan; past-hiding runs before the gone/cancelled check for series; (d) load_notes folds without the account, so a foreign note hides this account's; (e) held rows are reported as updated and a duplicate gcal.row is appended every run; (f) the extras phase (c8934b93) shipped no tests: -e lacks the TTY check, vi fallback, git scissors, Edit-again loop, and empty-clears; -A drops bare buffers and lacks the existing-note refusal; the doctor notes check lacks cancelled/declined/series orphans, the 25-lookup cap, malformed records, and per-issue fixes; the fragile hint ignores the task/guests/no-note conditions and lacks fragile_directives JSON; (g) write contract: suggestions are always empty, clock_off/clock_on spans where the Mac expects clock, no invalid spans, one plan warning missing, rail labelled with the colour name. Planned as child epic 'Finish private event notes' (engine -> select -> write -> extras).

[2026-11-11T06:38:14Z · bob-cli-ji.8.land] CHILD LANDING CHECKPOINT: bob-cli-ji.8 remains open. Its four phases are closed and the planned core fixes are present, but the ji.8 lander found explicit -- mishandling after implicit TEXT (executed exact-source probe), editor dry-run and scope-control defects, incomplete doctor remedies, and missing immediate sync when clearing a live series by master ID. Fifteen Mac JSON fixture copies also remain stale from this child. A validated medium tale will finish these and owns ji.8 closeout, then a fresh review of this parent and all descendants; do not mark either plan done yet. ji.8 follow-up proposals are fully triaged on that bead, with existing docs-budget tasks jz/h9 corroborated and timestamp ordering retained as explicitly designed.

[2026-11-11T07:46:36Z · bob-cli-ji.8.land--2] PARENT CLOSEOUT VERIFIED after ji.8 landing: all 7 phases closed (ji.1 engine, ji.2 command/select, ji.3 provenance, ji.4 write, ji.5 editor/adopt/doctor/hint, ji.6 decision/guide, ji.7 Mac Event note mode) plus child epic ji.8 closed with its 4 phases (engine/select/write/extras). Notes #1-#3 fixed by 4c1f7dde/85e618d8 (clippy, catalog 89, doctor notes ID; just check passed 10457 tests); #4 follow-up triage stands (docs budgets jz/h9, glossary declined per memory_glossary=no, k0/k1/k2 split out, RSVP declined per read-only decision); #5 audit gaps closed by ji.8 tale 05ec8253; #6 checkpoint superseded by this close. Linked plan plan:202611/private_gcal_event_notes.md re-read; child plan finish_private_gcal_event_notes.md set done. Drift: bob-cli 05ec8253==origin/master (single tale commit since ba7a1c90, no non-epic commits, tree clean); Mac 37b0e68==origin/master (fixture refresh only, 18/18 agree, tree clean). Decisions: auto_sync=yes (live-master clears sync immediately), mac_chord=cmd_e, memory_record=yes (authorized records only), memory_glossary=no (no strand) all honored; Google read-only preserved. Validation: epic-symbols empty for ji and ji.8; sase plan links validate shows only 58 legacy unrelated errors (prompt-in-plans-store + one PLAN link, none on these plans). Tests: just check exit 0; Mac portable 2468 pass 0 fail; macOS GcalNote suites 69 pass; 3 tip-panel timeouts pre-existing tracked in jx (+1 this turn).

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ji.1](bob-cli-ji.1.md) | Note store and per-field layering engine | ✓ closed | medium | 2026-11-10 | 1 | 1 |
| [bob-cli-ji.2](bob-cli-ji.2.md) | bob gcal note command, event selection and read-only modes | ✓ closed | medium | 2026-11-10 | 1 | 1 |
| [bob-cli-ji.3](bob-cli-ji.3.md) | Note provenance in gcal.row and fail-safe reads | ✓ closed | small | 2026-11-10 | 1 | 1 |
| [bob-cli-ji.4](bob-cli-ji.4.md) | Writing, previewing, and applying notes | ✓ closed | medium | 2026-11-10 | 1 | 1 |
| [bob-cli-ji.5](bob-cli-ji.5.md) | Editor, adopt, doctor check, and fragile-description hint | ✓ closed | small | 2026-11-10 | 1 | 1 |
| [bob-cli-ji.6](bob-cli-ji.6.md) | Decision record, glossary term, and guide | ✓ closed | small | 2026-11-10 | 1 | 1 |
| [bob-cli-ji.7](bob-cli-ji.7.md) | Bob Mac Capture Event note mode | ✓ closed | large | 2026-11-10 | 1 | 0 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ji: Private event notes for Google Calendar events [closed]"]
    n1["bob-cli-ji.1: Note store and per-field layering engine [closed]"]
    n2["bob-cli-ji.2: bob gcal note command, event selection and read-only modes [closed]"]
    n3["bob-cli-ji.3: Note provenance in gcal.row and fail-safe reads [closed]"]
    n4["bob-cli-ji.4: Writing, previewing, and applying notes [closed]"]
    n5["bob-cli-ji.5: Editor, adopt, doctor check, and fragile-description hint [closed]"]
    n6["bob-cli-ji.6: Decision record, glossary term, and guide [closed]"]
    n7["bob-cli-ji.7: Bob Mac Capture Event note mode [closed]"]
    n8["bob-cli-ji.7.1: Complete Bob Mac Capture Event note mode [closed]"]
    n9["bob-cli-ji.7.1.1: Complete event-note fixtures and the Swift process contract [closed]"]
    n10["bob-cli-ji.7.1.2: Event-note session, request ordering, and mutation undo [closed]"]
    n11["bob-cli-ji.7.1.3: Shared hatched meeting and buffer rail [closed]"]
    n12["bob-cli-ji.7.1.4: Mode entry points, capture preservation, and event picker [closed]"]
    n13["bob-cli-ji.7.1.5: Highlighted editor, live preview, and save controls [closed]"]
    n14["bob-cli-ji.7.1.6: Document the shipped mode and assemble completion evidence [closed]"]
    n15["bob-cli-ji.8: Finish private event notes — correctness fixes and the missing extras [closed]"]
    n16["bob-cli-ji.8.1: Account-aware note fold, honest held rows, and accurate note provenance [closed]"]
    n17["bob-cli-ji.8.2: Exact selection, argv pre-pass, orphans, and list/show fixes [closed]"]
    n18["bob-cli-ji.8.3: Write contract, validation warnings, human output, and missing tests [closed]"]
    n19["bob-cli-ji.8.4: Finish -e, -A, the doctor notes check, and the fragile-description hint [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n0 --> n7
    n7 --> n8
    n8 --> n9
    n8 --> n10
    n8 --> n11
    n8 --> n12
    n8 --> n13
    n8 --> n14
    n0 --> n15
    n15 --> n16
    n15 --> n17
    n15 --> n18
    n15 --> n19
    n1 -.-> n2
    n1 -.-> n3
    n2 -.-> n4
    n3 -.-> n6
    n4 -.-> n5
    n4 -.-> n6
    n4 -.-> n7
    n6 -.-> n7
    n9 -.-> n10
    n9 -.-> n11
    n10 -.-> n12
    n11 -.-> n13
    n12 -.-> n13
    n13 -.-> n14
    n16 -.-> n17
    n17 -.-> n18
    n18 -.-> n19
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ji.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.1/README.md) | [bob-cli-ji.1](bob-cli-ji.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.2/README.md) | [bob-cli-ji.2](bob-cli-ji.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.3/README.md) | [bob-cli-ji.3](bob-cli-ji.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.4/README.md) | [bob-cli-ji.4](bob-cli-ji.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.5/README.md) | [bob-cli-ji.5](bob-cli-ji.5.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.6/README.md) | [bob-cli-ji.6](bob-cli-ji.6.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.md) | [bob-cli-ji.7](bob-cli-ji.7.md) | 0 |
| [bbugyi200.apollo.bob-cli-ji.7.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.7.1.1/README.md) | [bob-cli-ji.7.1.1](bob-cli-ji.7.1.1.md) | 2 |
| [bbugyi200.apollo.bob-cli-ji.7.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.2.md) | [bob-cli-ji.7.1.2](bob-cli-ji.7.1.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.7.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.3.md) | [bob-cli-ji.7.1.3](bob-cli-ji.7.1.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.7.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.4.md) | [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) | 3 |
| [bbugyi200.apollo.bob-cli-ji.7.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.5.md) | [bob-cli-ji.7.1.5](bob-cli-ji.7.1.5.md) | 2 |
| [bbugyi200.apollo.bob-cli-ji.7.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.7.1.6/README.md) | [bob-cli-ji.7.1.6](bob-cli-ji.7.1.6.md) | 2 |
| [bbugyi200.apollo.bob-cli-ji.7.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.land.md) | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 6 |
| [bbugyi200.apollo.bob-cli-ji.8.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.1/README.md) | [bob-cli-ji.8.1](bob-cli-ji.8.1.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.8.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.2/README.md) | [bob-cli-ji.8.2](bob-cli-ji.8.2.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.3/README.md) | [bob-cli-ji.8.3](bob-cli-ji.8.3.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.4/README.md) | [bob-cli-ji.8.4](bob-cli-ji.8.4.md) | 1 |
| [bbugyi200.apollo.bob-cli-ji.8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.8.land.md) | [bob-cli-ji.8](bob-cli-ji.8.md) | 3 |
| [bbugyi200.apollo.bob-cli-ji.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.land.md) | [bob-cli-ji](README.md) | 0 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`4219d70`](https://github.com/bobs-org/bob-cli/commit/4219d70a75d81299cb9321bf194508abcbb96367) | feat(gcal): layer private event notes over Google descriptions | [bob-cli-ji.1](bob-cli-ji.1.md) | 2026-11-10 06:48:22 EST |
| bob-cli | [`7ff24c8`](https://github.com/bobs-org/bob-cli/commit/7ff24c8241b1fefbed57906f5486367e3f86e14d) | feat(gcal): record note provenance in gcal.row and fail-safe reads | [bob-cli-ji.3](bob-cli-ji.3.md) | 2026-11-10 07:15:55 EST |
| bob-cli | [`a2809a1`](https://github.com/bobs-org/bob-cli/commit/a2809a1dc48db0d2ac384f44d3e5fce7c8635715) | feat(gcal): add bob gcal note selection and read-only modes | [bob-cli-ji.2](bob-cli-ji.2.md) | 2026-11-10 08:11:11 EST |
| bob-cli | [`cf7c060`](https://github.com/bobs-org/bob-cli/commit/cf7c06052b26b64d5fb68e10a4b65b5f759fac10) | feat(gcal): add private event note writes and preview | [bob-cli-ji.4](bob-cli-ji.4.md) | 2026-11-10 09:56:07 EST |
| bob-cli | [`8f2b492`](https://github.com/bobs-org/bob-cli/commit/8f2b492552dc4c325322af1fc8cc8b25987028e5) | feat(gcal): record private event notes decision and guide | [bob-cli-ji.6](bob-cli-ji.6.md) | 2026-11-10 10:14:40 EST |
| bob-cli | [`c8934b9`](https://github.com/bobs-org/bob-cli/commit/c8934b93af196e36b08a480aac36df5b336dcda6) | feat(gcal): edit and adopt private event notes | [bob-cli-ji.5](bob-cli-ji.5.md) | 2026-11-10 10:24:00 EST |
| bob-cli | [`8e2b93c`](https://github.com/bobs-org/bob-cli/commit/8e2b93c7d0ed6bee06cb5b19b5ce95bc8f09115e) | feat(gcal): expose effective buffer reasons in note JSON | [bob-cli-ji.7.1.1](bob-cli-ji.7.1.1.md) | 2026-11-10 11:21:54 EST |
| bob-mac-capture | [`bob-mac-capture@8273c8f`](https://github.com/bobs-org/bob-mac-capture/commit/8273c8fe459b844bf2df58d30ed8d47794801e7a) | feat(capture): add gcal note process contract | [bob-cli-ji.7.1.1](bob-cli-ji.7.1.1.md) | 2026-11-10 11:22:27 EST |
| bob-mac-capture | [`bob-mac-capture@7cb516f`](https://github.com/bobs-org/bob-mac-capture/commit/7cb516fbab387fc79f014bc2750b2e83b92ac5dd) | feat(capture): add shared hatched meeting and buffer rail | [bob-cli-ji.7.1.3](bob-cli-ji.7.1.3.md) | 2026-11-10 11:33:26 EST |
| bob-mac-capture | [`bob-mac-capture@809b66a`](https://github.com/bobs-org/bob-mac-capture/commit/809b66abeaee819e72e1d89e78c2136dc7999db3) | feat(capture): add GcalNoteSession lifecycle | [bob-cli-ji.7.1.2](bob-cli-ji.7.1.2.md) | 2026-11-10 11:50:34 EST |
| bob-mac-capture | [`bob-mac-capture@cdd7384`](https://github.com/bobs-org/bob-mac-capture/commit/cdd73844aec701344b2fa8d1be97eb49d30d5ed0) | feat(capture): add Event Note picker overlay in capture panel | [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) | 2026-11-10 13:54:12 EST |
| bob-mac-capture | [`bob-mac-capture@f32a575`](https://github.com/bobs-org/bob-mac-capture/commit/f32a575071d016a8aa4c7e35dceae157d4cb58ba) | fix(capture): import CaptureCore testably in Event Note picker tests | [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) | 2026-11-10 14:10:47 EST |
| bob-mac-capture | [`bob-mac-capture@90b6f9e`](https://github.com/bobs-org/bob-mac-capture/commit/90b6f9e3cd96b3513687e35e85167a75f69578a8) | fix(capture): expect Command-E to open Event Note in the line-motion test | [bob-cli-ji.7.1.4](bob-cli-ji.7.1.4.md) | 2026-11-10 14:40:18 EST |
| bob-mac-capture | [`bob-mac-capture@5bf8907`](https://github.com/bobs-org/bob-mac-capture/commit/5bf8907e6071f4f364a86b90f28a25cd8957ed09) | feat(capture): add Event Note editor, highlights, and save controls | [bob-cli-ji.7.1.5](bob-cli-ji.7.1.5.md) | 2026-11-10 16:01:17 EST |
| bob-mac-capture | [`bob-mac-capture@62a7b70`](https://github.com/bobs-org/bob-mac-capture/commit/62a7b70fb8d217e6afcdeb7cff0062019ac65524) | fix(capture): publish Event Note preview and show updates atomically | [bob-cli-ji.7.1.5](bob-cli-ji.7.1.5.md) | 2026-11-10 16:35:31 EST |
| bob-cli | [`23e7f90`](https://github.com/bobs-org/bob-cli/commit/23e7f90df5be9b52b5600c82a6b9104c6324d924) | docs(gcal): mark Mac event-note mode shipped and point at Mac guide | [bob-cli-ji.7.1.6](bob-cli-ji.7.1.6.md) | 2026-11-10 17:10:50 EST |
| bob-mac-capture | [`bob-mac-capture@1498f34`](https://github.com/bobs-org/bob-mac-capture/commit/1498f348f9095daacfe02a8fda9f07e8012030ef) | docs(capture): add event-notes page and nav entry with key/protocol/agenda links | [bob-cli-ji.7.1.6](bob-cli-ji.7.1.6.md) | 2026-11-10 17:11:22 EST |
| bob-cli | [`4c1f7dd`](https://github.com/bobs-org/bob-cli/commit/4c1f7dde9f6e8515f069ccfd3e58c30047d76a0e) | fix(gcal): clean event note lint and add preview fixtures | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 18:28:36 EST |
| bob-mac-capture | [`bob-mac-capture@f1e5c99`](https://github.com/bobs-org/bob-mac-capture/commit/f1e5c99c05539d54e71789f8afba95837b8fccc2) | feat(capture): complete event note editing and preview | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 18:29:07 EST |
| bob-cli | [`85e618d`](https://github.com/bobs-org/bob-cli/commit/85e618d889ab2172c29ab5b25cae66d209968936) | test(cli): align catalog and gcal doctor expectations | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 20:14:17 EST |
| bob-mac-capture | [`bob-mac-capture@15e34ba`](https://github.com/bobs-org/bob-mac-capture/commit/15e34bafc9638dc63117ab527719dd327c57085a) | test(capture): check event note footer accessibility bounds | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 20:14:46 EST |
| bob-mac-capture | [`bob-mac-capture@e638795`](https://github.com/bobs-org/bob-mac-capture/commit/e63879582888becb02c51430c012f0c4b6b26592) | test(gcal-note): verify compact editor footer layout | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 22:03:42 EST |
| bob-cli--plans | [`bob-cli--plans@b03a50d`](https://github.com/bobs-org/bob-cli--plans/commit/b03a50db376878c4df63ec373f72d8624a2f4654) | docs(gcal-note): mark Mac event note plan done | [bob-cli-ji.7.1](bob-cli-ji.7.1.md) | 2026-11-10 22:04:14 EST |
| bob-cli | [`54e650d`](https://github.com/bobs-org/bob-cli/commit/54e650d17699f9ff2362a40f20ae8e80e8b59585) | fix(gcal): fold private notes per account and report held rows honestly | [bob-cli-ji.8.1](bob-cli-ji.8.1.md) | 2026-11-10 23:04:40 EST |
| bob-cli | [`9660397`](https://github.com/bobs-org/bob-cli/commit/9660397de55695647da3a01c2f595e1560651058) | fix(gcal-notes): nine select fixes for note previews, options, clear, list/show | [bob-cli-ji.8.2](bob-cli-ji.8.2.md) | 2026-11-11 00:05:16 EST |
| bob-cli | [`b706f55`](https://github.com/bobs-org/bob-cli/commit/b706f5592a5475a66e61f6b99cbbf5daef1a6f5c) | fix(gcal): complete private event note write contract | [bob-cli-ji.8.3](bob-cli-ji.8.3.md) | 2026-11-11 00:40:52 EST |
| bob-cli | [`ba7a1c9`](https://github.com/bobs-org/bob-cli/commit/ba7a1c9092a368dded96c3ec95dee72c0261f7b0) | feat(gcal): finish private event note extras | [bob-cli-ji.8.4](bob-cli-ji.8.4.md) | 2026-11-11 01:25:11 EST |
| bob-cli | [`05ec825`](https://github.com/bobs-org/bob-cli/commit/05ec8253f144ed6e5947f659a17eb50dea45d251) | fix(gcal): finish private note landing boundary cases | [bob-cli-ji.8](bob-cli-ji.8.md) | 2026-11-11 02:12:55 EST |
| bob-mac-capture | [`bob-mac-capture@37b0e68`](https://github.com/bobs-org/bob-mac-capture/commit/37b0e68a1dcfc24e6b7dca75a3074daf13f887b0) | test(gcal-note): refresh contract fixtures from bob-cli | [bob-cli-ji.8](bob-cli-ji.8.md) | 2026-11-11 02:13:41 EST |
| bob-cli--plans | [`bob-cli--plans@469f92b`](https://github.com/bobs-org/bob-cli--plans/commit/469f92b162c691f521e78289e735c043cfeaef02) | docs(plans): mark private event note plans done after ji.8 landing | [bob-cli-ji.8](bob-cli-ji.8.md) | 2026-11-11 02:48:00 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ji.7.1.land--8][1] | Confirm the parent epic remains open after phase closeout | 1 |
| read-by | [agent:bob-cli-ji.8.1][2] | Need parent legend/epic DECISIONS that phases must honor | 1 |
| read-by | [agent:research.40.cdx][3] | Inspect the epic context for an independent private event metadata guide | 1 |
| read-by | [agent:research.40.cld][4] | Context for writing a user guide on adding metadata to private event tasks | 1 |
| read-by | [agent:research.40.final][5] | Ground consolidated private-event-notes guide in the epic's current status and guide requirements | 1 |
| read-by | [agent:research.40.gem][6] | Understand requirements and context for adding metadata to private event tasks | 1 |
| read-by | [agent:research.40.grk][7] | Need full epic bead context including notes and follow-ups for the user-guide research | 1 |
| read-by | [agent:research.40.mus][8] | research guide on adding metadata to private event tasks | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ji.7.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ji.8.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.cdx/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.cld/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.final/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.gem/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.grk/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.40.mus/README.md

<!-- sase:referenced-by:end -->
