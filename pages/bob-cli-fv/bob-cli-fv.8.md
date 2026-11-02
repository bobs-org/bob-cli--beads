# Bead: bob-cli-fv.8 — Decision record and end-to-end review

[Bead Pages](../README.md) / [bob-cli-fv](README.md) / bob-cli-fv.8

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5o.linker.w0.md) · **Assignee:** `bob-cli-fv.8` · **Size:** small
**Created:** 2026-11-02 09:28:51 EST
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

## Dependencies

- **Depends on:** [bob-cli-fv.7](bob-cli-fv.7.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-fv.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-fv.8.md) | [bob-cli-fv.8](bob-cli-fv.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8c140e4`](https://github.com/bobs-org/bob-cli/commit/8c140e43d22cf562e063c4a0983cd0c939339c54) | docs(cli): refresh capture and relation contracts | [bob-cli-fv.8](bob-cli-fv.8.md) | 2026-11-02 13:22:59 EST |
