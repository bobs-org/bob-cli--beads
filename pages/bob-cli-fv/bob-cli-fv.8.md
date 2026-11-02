# Bead: bob-cli-fv.8 — Decision record and end-to-end review

[Bead Pages](../README.md) / [bob-cli-fv](README.md) / bob-cli-fv.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5o.linker.w0.md) · **Assignee:** `bob-cli-fv.8` · **Size:** small
**Created:** 2026-11-02 09:28:51 EST · **Closed:** 2026-11-02 16:21:40 EST
**Plan:** [202611/gcal\_description\_bullets.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_description_bullets.md)

## Description

decision-and-review: author the new decision record and the supersession mark, regenerate docs, run the full gates, and do a read-only end-to-end review against the A1–A10 requirements.

## Notes

[2026-11-02T18:22:04Z · bob-cli-fv.8--1] End-to-end review evidence (2026-11-02)

`just check`: exit 0 (fmt, clippy, full workspace test suite). It includes the Gcal fixture-driven fake-gog integration tests. `just docs-check`: exit 0; lint, generated-content drift, strict build, link checks, search smoke, executable tutorial, and docs unit tests passed (447 passed, 1 optional-fonts test skipped).

| Requirement | Test evidence |
| --- | --- |
| A1 Event Tasks only; Maybe→Yes upgrade | `descriptions_become_bullets_in_every_phase`, `context_rows_never_get_bullets`, `upgrade_lands_bullets_above_existing_notes`, `context_rows_still_never_get_description_bullets` |
| A2 directives, boilerplate, separators, blanks, badge duplicates excluded | `description::bullets::bullet_vectors`; `descriptions_become_bullets_in_every_phase`; `teams_only_description_writes_nothing` |
| A3 Google follows untouched bullets; edits/nesting/deletion hands off | `google_description_edit_rewrites_untouched_bullets`, `google_clearing_description_removes_the_block`, `edited_description_is_kept_silently_then_reported_once`, `deleted_description_block_is_never_re_added` |
| A4 flat first-child bullets and list structure | `description::bullets::bullet_vectors`, `descriptions_become_bullets_in_every_phase`, `space_indented_note_gets_space_bullets` |
| A5 imported text stays inert | `description::bullets::hostile_bullets_are_isolated_from_bob_scanners` |
| A6 cap, overflow, oversize fallback | `long_description_caps_at_eight_with_an_overflow_line`, `description::bullets::oversize_input_uses_one_calendar_fallback` |
| A7 pre-feature rows backfill; matching rows are adopted | `pre_feature_row_backfills_on_the_next_sync`, `crash_adoption_matching_bullets_does_not_duplicate` |
| A8 JSON carries count only; journal omits description text | `sync_json_rows_carry_description_lines`, plus privacy assertions in `descriptions_become_bullets_in_every_phase` |
| A9 directive grammar remains unchanged | `descriptions_become_bullets_in_every_phase` verifies `@love #offclock` routes the task and only “And retainers!” becomes prose |
| A10 `gcal.description: off` disables new bullets | `description_off_writes_no_bullets`, `description_off_leaves_existing_bullets_alone` |

Representative rendered daily-note excerpt from the motivating case:

\```markdown
- [*] #task **0800-0815** Swings! [📅](…) #offclock [root:: love] ^swings
  - And retainers!
\```

Memory reconciliation blocker: the approved plan decisions say `decision_record = no` (do not create `decisions:gcal-description-bullets-follow-google-until-edited`) and `supersede_propose_once = yes` (mark the existing strand partly superseded by that new record). The new target does not exist and is explicitly declined, so there is no valid `superseded_by` target or back-link to write. I made no memory edits and left the phase open rather than inventing the target. The existing docs are generated-current per `just docs-check`.

[2026-11-02T21:11:40Z · bob-cli-fv.8] Decision reconciliation: applied supersede_propose_once=yes by appending the description-bullet exception to the authorized existing record only. Its superseded-in-part status and existing root successor remain valid. Since decision_record=no explicitly declines the proposed new strand, no replacement strand or dangling superseded_by target was added; the new exception cites the approved plan, docs/gcal.md, and lifecycle tests directly. The accepted original body and root supersession remain unchanged. This resolves the earlier note without reopening a declined decision.

[2026-11-02T21:11:44Z · bob-cli-fv.8] PROPOSED FOLLOW-UP: Fix two unresolved links in the capture-sigils decision — sase memory init --no-commit succeeds but warns that [[task-drawer]] and [[task-type]] in decisions/capture-sigils-say-where-what-how.md should be qualified as glossary:task-drawer and glossary:task-type. That note is unchanged by this phase and outside its memory authorization.

[2026-11-02T21:14:38Z · bob-cli-fv.8] Offline end-to-end review completed against the landed implementation.

An isolated scratch vault with a realistic daily note was driven through BOB_GCAL_GOG using seven synthetic events: the motivating Swings event, HTML agenda, Teams with and without a video badge, long agenda, hostile Markdown, and managed-log impersonation. No real calendar or vault was read or changed.

Verified exact rendered bullet bytes against the committed retainer/HTML/hostile/managed-log vectors; directive routing and buffer fields; Teams exclusion when the badge exists and one retained join link when it does not; the 8-line cap including its overflow; dry-run immutability; description counts with no prose in JSON or journal; byte-identical rerun; a Google description update; local edit handoff; and a once-only conflict notice after Google changes again. The A1–A10 traceability table in note #1 remains applicable; A2 also includes description::tests::keep_bullet_labels_by_vendor and the scratch no-badge case. The approved boilerplate-filter step 4 requires this join-link exception; docs/gcal.md is clarified to match.

Full initial rendered note for visual review (tabs preserved, all data synthetic):

\```markdown
\# Friday 2026-10-30

\## Notes

- A quiet morning
\## Events

*↻ synced 07:00 · [you@example.com](https://calendar.google.com/calendar/r/day/2026/10/30?authuser=you%40example.com)*
- [*] #task **0800-0815** Swings! [📅](https://calendar.google.com/event?eid=swings) #offclock [root:: love] [type:: MEET] ^swings
	- And retainers!
- [*] #task **1400-1500** Onsite interview [📅](https://calendar.google.com/event?eid=onsite-interview) [buffer:: -15m] [root:: job] [type:: MEET] ^onsite-interview
	- **Agenda:**
		- Intros
		- System design – [prep doc](https://docs.google.com/document/d/1AbC/edit)
	- Bring laptop & ID
- [*] #task **1500-1530** Teams join only [📅](https://calendar.google.com/event?eid=teams-join-only) [root:: meet] ^teams-join-only
	- [Join Teams meeting](https://teams.microsoft.com/l/meetup-join/example)
- [*] #task **1530-1600** Teams invite [📅](https://calendar.google.com/event?eid=teams-invite) [📹](https://teams.microsoft.com/l/meetup-join/example) [root:: meet] ^teams-invite
- [*] #task **1600-1630** Long agenda [📅](https://calendar.google.com/event?eid=long-agenda) [root:: meet] ^long-agenda
	- Agenda item 1
	- Agenda item 2
	- Agenda item 3
	- Agenda item 4
	- Agenda item 5
	- Agenda item 6
	- Agenda item 7
	- *…5 more lines in [Google Calendar](https://calendar.google.com/event?eid=long-agenda)*
- [*] #task **1700-1730** Hostile input [📅](https://calendar.google.com/event?eid=hostile-input) [root:: meet] ^hostile-input
	- Run \`$= dv.el("b", 1)\` now
	- RSVP \#task by Friday
	- See \[\[Secret Note]]
	- **TBD**
	- Bring &#127813; salad
	- Room\:\: 4B
	- click
	- Use \<% tp.date.now() %> here
- [*] #task **1730-1800** Log guard [📅](https://calendar.google.com/event?eid=log-guard) [root:: meet] ^log-guard
	- *Work log*

\## Pomodoros
- [ ] () — MEET
	- [[#^swings]]
	- [[#^onsite-interview]]
	- [[#^teams-join-only]]
	- [[#^teams-invite]]
	- [[#^long-agenda]]
	- [[#^hostile-input]]
	- [[#^log-guard]]
\```

[2026-11-02T21:16:32Z · bob-cli-fv.8] Publication verification: sase memory init --no-commit completed; just docs-gen regenerated only docs/develop/decisions.md. Final just docs-check exited 0 after the conferencing docs clarification: lint, generated drift, strict build, links, search, tutorial, media determinism, and documentation tests passed (447 passed, 1 optional-fonts skip). The authorized memory is readable with the new exception and the original root backlink intact. Full Rust gate is running as ToolRun 3d6bd1ab8d21425dc65b413467589044.

[2026-11-02T21:21:40Z · bob-cli-fv.8] Completed the authorized partial supersession in the existing Gcal policy record without creating the declined replacement strand; republished memory and regenerated docs. Clarified the conferencing join-link exception and inert task-link wording. Recorded a seven-event offline end-to-end review with the full rendered synthetic daily note and confirmed the existing A1–A10 traceability table. Verified just check passed (ToolRun 3d6bd1ab8d21425dc65b413467589044, exit 0), final just docs-check passed (447 tests, one optional-fonts skip), and git diff --check passed. sase bead epic-symbols reported no entries. Unrelated unresolved memory links are recorded as PROPOSED FOLLOW-UP. Closed only this phase.

## Dependencies

- **Depends on:** [bob-cli-fv.7](bob-cli-fv.7.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fv.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-fv.8/README.md) | [bob-cli-fv.8](bob-cli-fv.8.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8c140e4`](https://github.com/bobs-org/bob-cli/commit/8c140e43d22cf562e063c4a0983cd0c939339c54) | docs(cli): refresh capture and relation contracts | [bob-cli-fv.8](bob-cli-fv.8.md) | 2026-11-02 13:22:59 EST |
| bob-cli | [`30d3120`](https://github.com/bobs-org/bob-cli/commit/30d312095ab2a009e635d2b51fb1697d49885970) | docs(gcal): record description ownership and join-link exception | [bob-cli-fv.8](bob-cli-fv.8.md) | 2026-11-02 16:22:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-fv.8][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-fv.8--1][1] | Need the phase scope, design file, decisions, and prior notes before completing the assigned phase | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fv.8.md

<!-- sase:referenced-by:end -->
