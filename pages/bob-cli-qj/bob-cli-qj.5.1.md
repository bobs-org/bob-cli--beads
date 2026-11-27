# Bead: bob-cli-qj.5.1 — Extract prose sections into prose notes and inline them back

[Bead Pages](../README.md) / [bob-cli-qj.5](bob-cli-qj.5.md) / bob-cli-qj.5.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-qj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.md) · **Assignee:** `bob-cli-qj.5.1.land`
**Created:** 2026-11-27 07:18:27 EST · **Closed:** 2026-11-27 18:27:15 EST
**Plan:** [202611/prose\_section\_extract\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_section_extract_inline.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/prose_section_extract_inline.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 7 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_section_extract_inline.md

<!-- sase:links:end -->

## Description

One Obsidian gesture turns an authored section of an area, project, or prose note into a prose note, and the same gesture folds it back. bob prose extract and bob prose inline own the conversion in Rust: previewed, preimage-guarded, all-or-nothing, link-repairing, crash-recoverable, and lossless on a round trip. Extraction records provenance that the later reversible-projects work can consume.

## Notes

[2026-11-27T13:18:36Z · bob-cli-qp.land] DISCOVERED ISSUE (found by the bob-cli-qp land agent running just check on bob-cli master 85d2fb32): clippy fails the canonical gate with 'error: this let...else may be rewritten with the ? operator' (clippy::question_mark, denied by clippy_gate) at src/native/prose/section_model.rs:922-928 (let Some(rest) = bullet.strip_prefix("- ").or_else(.."* ").or_else(.."+ ") else { return None; };). The file was added by 85d2fb32 (bob-cli-qj.5.1.2), which closed after only cargo test --lib native::prose::section_model::tests. Because the build of bob-obsidian (lib) stops there, just check runs no tests at all on master for every agent. Fix: let rest = bullet.strip_prefix("- ").or_else(...).or_else(...)?; then rerun just check. Log: ~/.cache/sase/tmp/qp-land/just-check.log on apollo.

[2026-11-27T15:57:34Z · bob-cli-r7.2--1] DISCOVERED ISSUE: clippy_gate still red on master at question_mark section_model.rs:924 and items_after_test_module relocate.rs:813 (qj.5.1.2 / qj.5.1.3 leftovers). bob-cli-r7.2 recovery applied the mechanical repairs (let rest = ...?; helpers moved above mod tests) so just check can land unrelated docs-mount work. Please keep those two files in that shape.

[2026-11-27T17:52:53Z · bob-cli-r7.land] DISCOVERED ISSUE (bob-cli-r7.land running just check on bob-cli master 7213dd89, athena): clippy now passes, but cargo test --lib fails 2 of 8270: native::catalog::tests::every_path_resolves_to_a_public_leaf panics at src/native/catalog/tests.rs:63 'excluded path ["prose", "extract"] is not a public leaf' and native::completion::kinds::tests::every_value_arg_has_a_decision panics at src/native/completion/kinds.rs:1352 'value-taking args without a kinds decision: ["prose extract:expect", "prose extract:line"]'. Both come from a558ce11 (bob-cli-qj.5.1.4): it adds a catalog EXCLUDED entry for the .hide(true) extract subcommand and two value args with no kinds decision. Impact: just check is red for every bob-cli agent until fixed. Fix: add kinds decisions for extract --expect/--line, and either un-hide extract or drop/adjust the EXCLUDED entry until it is public (inline will need the same).

[2026-11-27T20:23:35Z · bob-cli-r8.land] DISCOVERED ISSUE: bob-cli-r8.land fresh just check on cbbddc71 (ToolRun 5787740ee74cb5105608f1e11247e2e2) passes fmt then fails clippy at src/native/prose/convert/inline.rs:760 filter_map_bool_then and :1357 useless_format. Both are in eff5d986 from qj.5.1.5 and predate r8 source commit dbdc7d24. Tests were not reached. This corroborates r8.2 note 1, which had identified the same failures; no separate task or edits by this lander.

[2026-11-27T20:45:12Z · bob-cli-qj.5.1.land] LANDING TRIAGE (bob-cli-qj.5.1.land) of every child PROPOSED FOLLOW-UP: (1) glossary:prose-section strand (5.1.1 #2, 5.1.2 #2/#3, 5.1.3 #1, 5.1.4 #1, 5.1.5 #1, 5.1.6 #1, 5.1.7 #1, 5.1.8 #1) -> filed memory task bob-cli-rg (ready, small) for Bryan to approve or cancel; the auto-declined memory_prose_section decision was honored (no epic commit touches sase/memory). (2) just lint red on clean base, 164 errors (5.1.1 #1, 5.1.4 #2) -> declined: just lint and just check share one clippy gate, which passes on 6f12dd0d + this landing; the section_model/relocate leftovers were healed by bob-cli-r7.2 (18785315). (3) clippy 1.95 filter_map_bool_then inline.rs:760 and useless_format :1357 (5.1.6 #3) -> declined as a follow-up: epic-caused, fixed in this landing. (4) install_ui live PTY test test_real_cargo_install_transcript_uses_correct_phases_and_hides_chatter (5.1.6 #2) -> filed flake task bob-cli-rf (ready, small): 5/5 serial passes on an unchanged tree; root cause is an 80 ms fixture window under live.py's 100 ms frame throttle. (5) snooze-add-resnooze-replaces-history mutation vector (5.1.7 #2) -> declined: already tracked as DISCOVERED ISSUE notes #4/#5 on active epic bob-cli-q5 (5.1.7 cited phase bob-cli-r7.3, which only proposed it). Epic notes #1-#3 (clippy question_mark, items_after_test_module, catalog/completion test failures): the first two were fixed by bob-cli-r7.2; the catalog Excluded test passes now that inline unhid extract; the completion kinds gap (extract --expect/--line, inline --expect) and the stale root-help fixtures are fixed in this landing.

[2026-11-27T20:47:13Z · bob-cli-qj.5.1.land] LANDING VERIFICATION (bob-cli-qj.5.1.land): all 8 phases closed; bob-plugins c2f73154/07c4eeb4 on origin/master (commands, Ctrl+Shift+E new_chord, Command Mode rows, marker, tests, docs); vault_rewrite trash/journal/recovery with crash tests; section_model refusals with tests; docs/host probe present; prose_catalog=no and memory_prose_section=no honored; no post-start commit conflicts with or should reuse the epic. Integration fixes made this turn: clippy (inline.rs), completion kinds for extract --expect/--line and inline --expect, root-help fixtures; just check green, docs-gen no diff, docs-check pass. REMAINING EPIC WORK found and handed to a staged tale plan (sase_plan_land_prose_sections_relocation_and_tests.md): relocate.rs canonical_fragment picks the longest fragment (inline writes owner#T#S, so L1 fails for in-note links: [[#Detail]] -> [[#Topic#Detail]]), render_note_path turns vault-rooted path wikilinks into ../ relative links, extract has zero tests, inline lacks has-children/title-dropped/rollback/crash tests, the proptest masks wikilinks, and the cdx relocation matrix is missing. The tale ends with this epic's closeout.

[2026-11-27T23:26:53Z · bob-cli-qj.5.1.land--3] LANDING VERIFICATION (2026-11-27). Prior land note #6 recorded all eight phases closed, plugin integration commits on origin/master, and green just check, docs-gen with no diff, and docs-check. This closeout verifies the remaining extract/inline link-form and shortest-fragment work plus the follow-up repairs: malformed YAML test fixtures, ambiguous duplicate-heading refusal, and byte-identity assertions limited to layout-clean inputs.

Current gates: just check passed (ToolRun csbstnmqnpb4, exit 0): 13,399 Rust tests passed, 0 failed, 5 ignored across all test targets. just docs-gen passed (docs_reference 1/1); inventory reports 12 plugins and 176 registered commands; git diff --exit-code is clean. Plain just docs-check first resolved a stale plugin mount and reported the cabinets URL missing. Re-running the same recipe with BOB_DOCS_BOB_PLUGINS_DIR set to the opened bob-plugins checkout passed every implemented gate: lint, generated drift, strict Zensical, published URLs (266 pages, 1,004 mentions, 65 curated links), offline lychee (0 errors), edit links (256), search smoke (136), tutorial, CLI media, and docs tests (449 passed, 1 skipped because font dependencies are absent). sase bead epic-symbols bob-cli-qj.5.1 returned no --epic-symbol entries. just symvision is unavailable because this checkout has no symvision recipe; just --list confirms that, and the epic symbol whitelist is clean with no entries. Plan 202611/prose_section_extract_inline.md is marked done. Parent phase bob-cli-qj.5 remains closed; parent epic bob-cli-qj remains in progress and was not closed.

## Dependencies

- **Blocks:** [bob-cli-qw](../bob-cli-qw/README.md) ◇ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.1.land.md) | [bob-cli-qj.5.1](bob-cli-qj.5.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@5dc9923`](https://github.com/bobs-org/bob-cli--plans/commit/5dc9923375e145dc05e37e27e08e3abe45ab9b6d) | docs(plan): mark prose section extraction done | [bob-cli-qj.5.1](bob-cli-qj.5.1.md) | 2026-11-27 18:29:19 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.5.1.land][1] | Need the epic scope, children, and linked plan file | 1 |
| read-by | [agent:bob-cli-qj.5.1.land--1][1] | Record current land bead status and plan context before finishing verification | 1 |
| read-by | [agent:bob-cli-qj.5.1.land--2][1] | Verify the prose extraction phase bead and prepare its closure note | 1 |
| read-by | [agent:bob-cli-qj.5.1.land--3][1] | Need assigned epic note and scope for closeout evidence | 3 |
| read-by | [agent:bob-cli-r7.1][2] | check if clean-tree clippy gate failure is already tracked | 1 |
| read-by | [agent:bob-cli-r7.land][3] | Check whether the in-progress prose epic owns the prose extract catalog/completion test failures found while landing bob-cli-r7 | 2 |
| read-by | [agent:bob-cli-r8.land][4] | Verify ownership of landing check failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-r7.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-r7.land/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-r8.land/README.md

<!-- sase:referenced-by:end -->
