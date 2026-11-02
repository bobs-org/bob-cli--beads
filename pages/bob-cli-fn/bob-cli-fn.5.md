# Bead: bob-cli-fn.5 — Finish capture lists — section names with spaces, header completion, and undoable ID splices

[Bead Pages](../README.md) / [bob-cli-fn](README.md) / bob-cli-fn.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-fn.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fn.land.md) · **Assignee:** `bob-cli-fn.5.land`
**Created:** 2026-11-02 07:14:36 EST · **Closed:** 2026-11-02 11:16:33 EST
**Plan:** [202611/capture\_list\_section\_names.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_list_section_names.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/capture_list_section_names.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_list_section_names.md

<!-- sase:links:end -->

## Description

A list header can name any section, including one whose title has spaces (`@sase#future-work` or `@sase#"Future Work"` both reach `## Future Work`). Picking a section from the menu always inserts a selector that reaches that section. Route and section completion work on a list header even after bullets are typed below it. Accepting a block ID in Bob Mac Capture is one native Undo step. With this done, bob-cli-fn can land.

## Notes

[2026-11-02T15:28:28Z · bob-cli-fn.5.land] LAND AUDIT / FOLLOW-UP TRIAGE: Read fn.5 and both children with every note, parent fn decisions/landing notes, approved plan, bob-cli b483c93b and Mac f4ed5bb source/tests. Neither fn.5.1 nor fn.5.2 has a PROPOSED FOLLOW-UP entry. fn.5.1 #1 is implemented for ordinary spaced selectors/header completion/incomplete literals/off-clock equivalence; #2 stale keep_moving golden is fixed. fn.5.2 #1/#2 test harness fixes are in f4ed5bb; #3/#4 report all seven new Undo tests passing on CI 41466582525, with 21 existing failures owned by f3/fu (both beads read); no new independent defect or new task proposal. Remaining epic defect: section_selector_replacement checks raw spelling safety only on title, not slug. Heading including literal quotes, e.g. ## "Future Work", yields slug "future-work"; resolver-only check succeeds but parse_route_token decodes it as exact future-work, so completion cannot reach the selected heading. Curly opening quotes have the same problem. Exact fallback is also not checked against heading identity, so duplicate titles can produce a candidate for a heading the selector cannot reach. These violate phase-1 round-trip scope and stay epic work, to be repaired by one tale, not a task bead. Preserve all inherited DECISIONS and ID calibration. No proposals declined beyond the parent fn notes #2/#3/#8 already-recorded triage. epic-symbols fn.5 is currently clean; no symvision recipe.

[2026-11-02T15:29:25Z · bob-cli-fn.5.land] INTEGRATION AUDIT: Both origin/master refs fetched; local bob-cli a7931a64 and Mac f4ed5bb match their bases. Reviewed creation-window drift and post-b483c93b commits: ace86f8e/cb729a76/98bfec6a relation-successor work uses shared per-item capture planning and corrects project offer identity/order; fa1118c1 changes only gcal link sorting; a67cc79a start selection/warnings flows through the shared staged batch planner (lists inherit it); 0dfaeaa3 shared text escaping and 1562baab cancel-log indentation do not introduce alternate section routing or duplicate the feature; blocked-marks docs have no capture behavior overlap. Mac 6c7cf30 agenda icons and 1b61ac7 mid-meeting warning coexist with f4ed5bb (no shared edited splice/section path). No integration code change identified beyond completing the selector round-trip guarantee. CI 41466582525 metadata independently confirms Build/Lint success and Test failure at f6cab4f270a19e186bea9450b8e48c5eda2287ab; bundle/install gates skipped. No fresh just check claimed; remaining-work coder must run it, never check-full.

[2026-11-02T15:32:35Z · bob-cli-fn.5.land] CI EVIDENCE VERIFIED: Read full CI log for Mac run 41466582525. CaptureListPanelTests has 26 passing test cases and zero failures, including all seven native Undo cases, both partial-quote accepts, header-with-bullets accept, and calm section need. The 21 failing test case names match f3/fu exactly (11 clip, one line-case, three model, one pull-in, three separator, two task-type). Build and Lint passed; Bundle/Launch/Install skipped because Test is red. No new CI task or duplicate proposal. Remaining-work tale is limited to Rust selector lex/resolve consistency and concrete fn.5 plus fn parent closeout.

[2026-11-02T16:16:33Z · bob-cli-fn.5.land] Selector round-trip repair landed in uncommitted bob-cli working tree on HEAD 35c0a39a (host commits after this turn). `section_selector_replacement` now requires `unquoted_selector_spelling` on the hyphen slug as well as the raw title, and the quoted `"Title"` fallback is returned only when `resolved_bullet_heading_line(..., exact=true)` hits that heading's `line_index`. Unreachable headings (duplicate titles, case variants, H1 shadowed by a non-H1) are omitted via `Option` + `filter_map`. Preference order stays raw title, hyphen slug, escaped quoted literal. Grammar revision stays 6; no Swift, suggester, Cargo version, CHANGELOG, or memory edits.

Verification: pre-fix `section_completion_omits_selectors_that_cannot_round_trip` failed on quote-leading `## "Future Work"` (emitted slug `"future-work"`). After the helper change, unit `section_completion*` 9/9, `shell_completion_preserves_quoted_section_replacement`, CLI table `capture_complete_replacements_round_trip_to_the_picked_heading` (list apply+capture plus ordinary capture for quote-leading-spaced and slug-collision), and `quoted_section_replacement_is_a_raw_protocol_value` pass. Existing `capture_complete_then_list_lands_under_future_work` and `capture_off_clock_list_matches_equivalent_batch` still pass. `just check` exit 0 (fmt+clippy+workspace tests). `just docs-check` 447 passed, 1 skipped fonts. Never ran `just check-full`.

Mac: no Swift this turn. Retained independently verified CI run 41466582525 at f6cab4f270a19e186bea9450b8e48c5eda2287ab: Build/Lint pass, 26 CaptureListPanelTests pass including all seven native Undo cases; 21 failures remain exactly bob-cli-f3 / bob-cli-fu. Mac checkout still f4ed5bb.

Drift since fn.5 audit SHA a7931a64 is one commit, 35c0a39a feat(gcal): parse calendar descriptions into structured lines — gcal-only, no section-routing overlap.

Follow-up outcomes: neither fn.5.1 nor fn.5.2 has a PROPOSED FOLLOW-UP. fn.5.1 notes cover slug matching, header completion, incomplete literals, off-clock equivalence, and the stale keep_moving golden. fn.5.2 notes cover window-hosted undo tests and CI 41466582525. Parent fn notes #2/#3/#8 already record the older proposals (BufferPart as_str, docs-check/fo, routing-counter flake, declined decisions-record, declined plugin hold example, Jaccard gate met, bare-@ refusal, Mac Capture lists link, native undo remaining then done in fn.5.2). No new task. `sase bead epic-symbols bob-cli-fn.5` is clean. `just --list` has no `symvision` recipe.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-fn.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-fn.5.land.md) | [bob-cli-fn.5](bob-cli-fn.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`05b7fb1`](https://github.com/bobs-org/bob-cli/commit/05b7fb1b1842c46641aaa6aabea8f29a5b9f2c84) | fix(capture): round-trip section completion replacements to the picked heading | [bob-cli-fn.5](bob-cli-fn.5.md) | 2026-11-02 11:19:20 EST |
