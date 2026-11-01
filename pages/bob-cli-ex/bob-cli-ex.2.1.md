# Bead: bob-cli-ex.2.1 — Complete project-note task offers for bob-cli-ex.2

[Bead Pages](../README.md) / [bob-cli-ex.2](bob-cli-ex.2.md) / bob-cli-ex.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ex.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ex.2.md) · **Assignee:** `bob-cli-ex.2.1.land--code`
**Created:** 2026-10-31 13:56:44 EDT · **Closed:** 2026-11-01 09:51:12 EST
**Plan:** [202610/project\_note\_offer\_form.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_offer_form.md)

## Previously Closed

> ↺ Closed 2026-10-31T21:51:05Z · done
>
> (none)
>
> Reopened 2026-11-01T14:04:34Z by `sase bead open`

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/project_note_offer_form.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_offer_form.md

<!-- sase:links:end -->

## Description

Capture @route:id@ creates a project note and offers its eligible tasks through the existing pull-in protocol, with selected tasks identical to authored colon bullets and complete grammar, documentation, and verification coverage.

## Notes

[2026-10-31T21:07:21Z · bob-cli-ex.2.1.land] LAND AUDIT / FOLLOW-UP TRIAGE: Reviewed all notes on bob-cli-ex.2.1.1/.2/.3, approved child/parent plans, and commits 9a30ec4c, e9b9cd1d, e8dd3b65 plus current renderer, planner, parser/rewrite, offer plumbing, acceptance tests, docs and audited glossary strands. initial_marks=none and memory_glossary=yes (only successor-offer/task-successor) honored. Fetched origin/master at e8dd3b65; drift since first child commit consists of 36c48075 (global destination removal), efe2ebe0 (Keep status) and 17702dca (Keep docs). Current parser, rewrite notices, tests and docs preserve route-only @ behavior with item-local seals; Keep changes require no project-offer integration. All child notes reviewed. Only PROPOSED FOLLOW-UP is bob-cli-ex.2.1.3 note #1: trailing #hide interpreted as a type marker. Declined the special-case grammar proposal after sase_new_task searches across bug/all types, last-week sweeps, and active-epic review: documented edge #type syntax deliberately requires escaping literal tags; installed pre-seal bob 0.4.0 reproduces type_marker_not_applicable on old @cash^pkt+ with trailing #hide, while backslash-escaped #hide and mid-text #hide parse without diagnostics. Current type_marker.rs retains that rule from pre-epic 4a95e5b7/d1dd23e2. No new task or corroboration warranted; no causal active epic issue. The installed bob predates sealed offers, so it was not used to verify the current offer implementation. Remaining epic work found by source audit: project_schedule guard is incorrectly conditioned on explicit colon tasks; final offer net pass still trusts stale line numbers for ID-less tasks and does not refresh reported final lines; its Blocked filter only checks prior Ready/Next, leaving prior Pending offers alive when later batch work blocks them. These belong to this epic and will be covered by a single medium repair tale with concrete regression cases and this epic/parent-phase closeout. Both bob-cli-ex.2.1 and bob-cli-ex.2 epic-symbol audits are empty; no symvision recipe currently exists. Epic and parent phase remain open.

[2026-10-31T21:51:05Z · bob-cli-ex.2.1.land] Landing repairs complete. Reviewed child commits 9a30ec4c (offer engine), e9b9cd1d (colon seal + protocol), e8dd3b65 (contracts + acceptance incl byte-equal Offer vs authored colon). Repaired: (1) future-project guard Offer branch in project_note.rs so s:3 Offer with only ordinary/caret-ID bullets reports link_guard project_schedule, zero offers/picks, no daily write, day-absent ok; Create unchanged; unused named-destination refusal preserved. (2) Identity reconciliation in task_complete.rs: ID-less project offers resolve by cleaned description (both sides) + frozen duplicate ordinal from offer key, not stale line; net pass refreshes final line/status after relevant mutations; later-Blocked exclusion now covers Pending '/' (Ready/Next/Pending all drop, s:0 '?' preserved byte-equal). Focused regressions in project_note_offer.rs: future-without-colon guard, line-shift stale-line, typed with fields, duplicate ordinals, selected preview/submit + partial unselected-no-ID, Pending-blocked Ready/Next/Pending. Tests: 19/19 offer pass; lib 4236 pass; full cli 2590 pass; clippy gate pass; fmt clean. Canonical sase tool run check 5dae6d51 failed once on 2 flakes (articles adopt_note_completion, complete_themes shell) that pass in isolation and in the full cli re-run; no product regression. Post-start integration: origin/master identical at e8dd3b65; non-epic 36c48075 (remove @route+id), efe2ebe0 (Keep status), 17702dca (Keep guide) preserve route-only @ + item-local seals; Keep needs no integration. Decisions honored: initial_marks none, memory_glossary yes (only successor-offer/task-successor, already complete), offers unselected, picks via colon writer no freshness, ^prj/placeholder never offered, Create unchanged, no memory edits/options, no version/CHANGELOG. Declined bob-cli-ex.2.1.3 note 1 trailing-#hide exception: documented #type grammar requires escaping literal tags; pre-seal bob reproduces refusal; \#hide and mid-text #hide pass; no duplicate/causal task; no new bead.

[2026-11-01T13:55:17Z · bob-cli-ex.2.1.land] CLOSED-BEAD LAUNCH: agent bob-cli-ex.2.1.land launched against this closed bead; status left closed.
Launch submitted 2026-11-01T13:51:57.651477Z; run 20261101085200.
Prior close: 2026-10-31T21:51:05Z · done.

[2026-11-01T14:04:43Z · bob-cli-ex.2.1.land] RELAUNCH AUDIT / FOLLOW-UP TRIAGE: Reviewed every note on phases bob-cli-ex.2.1.1/.2/.3, the child and parent plans, commits 9a30ec4c/e9b9cd1d/e8dd3b65/42dd92bc and current renderer/planner/offer plumbing/grammar/rewrite/output/tests/docs. The prior fixes landed, including post-close parent repair 86a63e84 preserving unpicked duplicate offers. Integration audit through HEAD=origin/master=81b3b5a4: directive migrations, drawer writes/retyping/menu and JSON renames preserve routed project seals and shared colon placement; Keep changes require no integration. Decisions remain initial_marks=none and memory_glossary=yes for only successor-offer/task-successor; no new memory work or version/CHANGELOG edits. Sole PROPOSED FOLLOW-UP is bob-cli-ex.2.1.3 note 1 (trailing #hide). Re-triaged via sase_new_task: bug/all-type searches and last-week sweeps found no duplicate; bob-cli-bu is an unrelated relation glossary task; 12 active epic scopes including ey/ey.7 do not own this long-standing behavior. Declined the exception again: current built bob returns type_marker_not_applicable for trailing #hide, while escaped or mid-text #hide parses and captures correctly; docs teach that distinction. No task or corroboration needed. NEW REMAINING EPIC WORK: current public capture --dry-run --no-clip -f json with Finish it @:goog-exit@ returns exit 0, kind=task, and an inbox task containing the unfinished marker, violating the approved route-required execution contract. Named @:goog-exit@#admin does the same, and capture-parse reports mode=incomplete instead of pomodoro_project_note. Caret @^goog-exit@ correctly refuses execution. Root cause: is_pomodoro_marker_candidate excludes an empty route, so terminal dispatch falls through to prose; grammar.rs explicitly locks in that incorrect behavior. Named offer editor branches omit the route-less mode override present in the unnamed branch. Reopened for a small repair tale with exact public refusal/rollback and editor regressions and concrete same-turn closeout. Both child and parent-phase epic-symbol audits empty; just symvision is absent. Linked child plan currently says done and will be reopened to in_progress for the repair. Baseline just check ToolRun d6f4f2dfc0694788f1f60175641541e2 is still running; no source edits made.

[2026-11-01T14:09:21Z · bob-cli-ex.2.1.land] BASELINE / REPAIR HANDOFF: just check passed (sase ToolRun d6f4f2dfc0694788f1f60175641541e2, exit 0, 637522 ms; 4265 lib and 2612 CLI tests plus other test binaries). No source edits or check-full run. Green existing coverage does not discharge the reproduced route-less contract failure: a real scratch-vault capture of Finish packet @:pkt@ with child Draft memo writes the marker and child into mac_inbox.md. Additional editor matrix: @:pkt@#admin and @:pkt@#"Lit Name" lose pomodoro_project_note despite needs=route; @cash:@ and @cash:pkt@# also report incomplete rather than the approved Offer mode. The validated medium tale sase_plan_project_offer_routeless_closeout.md covers only sealed-offer execution refusal, consistent incomplete Offer modes/needs/spans, focused public atomicity tests, and same-turn child/parent-phase closeout. The child plan status was changed from done to in_progress in the opened plans sidecar. Parent bob-cli-ex.2 is confirmed an open phase under bob-cli-ex; coder must close ex.2.1 then ex.2 normally, leaving containing epic ex to its land agent. Historical #hide proposal remains declined as documented in the preceding triage note.

[2026-11-01T14:51:12Z · bob-cli-ex.2.1.land] CLOSEOUT after relaunch audit repair (verified against the working tree; host finalization commits it). Re-read bob-cli-ex.2.1.1/.2/.3 notes: original offer acceptance (engine, colon seal + public protocol, contracts/acceptance incl. byte-equal Offer vs authored colon bullets) remains satisfied. REPAIRED the two reproduced remaining contracts: (1) Execution: route-less sealed colon project markers (@:pkt@, @:pkt@#admin, @:pkt@#"Lit Name", @:@; leading or trailing, with authored children, multibyte body text) now refuse with the Pomodoro route error before any write, via new tokens.rs::route_less_sealed_project_note_error called from BOTH parse_terminal_route_token and validate_special_terminal_markers_line next to retired_route_less_project_note_error; scoped to a seal inside the block part, so unsealed @: / @:id, mid-prose tokens, forced-route semantics and retired @:id+ teaching are unchanged. Isolated-vault CLI regressions (tests/cli/capture/project_note_offer.rs) prove dry-run, real submit, -p all and JSON refusals change no file, a mixed draft with a valid earlier item (plain and offer) is atomic, and routed offers / literal forms still work. Old grammar.rs assertion that route-less offers become literal task text replaced. (2) Editor: editor_classify.rs::classify_pomodoro_offer_token now keeps pomodoro_project_note on every recognized sealed Offer (missing route, missing ID, unfinished name or unterminated quoted name) while retaining the precise route/pomodoro_id/pomodoro_name needs; @r:@#name no longer misplaces the seal span (byte-correct, non-overlapping, offer modifier on marker/route/ID/placeholders, none on the name). Caret Create behavior untouched. Added editor mode/span unit tests and capture-parse CLI tests incl. non-ASCII prefixes; updated two editor_modes assertions that encoded the old Incomplete mode. Docs: docs/capture.md paragraph + capture-parse help sentence, reference regenerated with just docs-gen (only capture-pars

… and 1285 more characters

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ex.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ex.2.1.land.md) | [bob-cli-ex.2.1](bob-cli-ex.2.1.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`42dd92b`](https://github.com/bobs-org/bob-cli/commit/42dd92bc66193dfc3ad16fc6ff0b9813d51c92c9) | fix(capture): finish project-offer landing repairs for bob-cli-ex.2.1 | [bob-cli-ex.2.1](bob-cli-ex.2.1.md) | 2026-10-31 17:52:51 EDT |
| bob-cli--plans | [`bob-cli--plans@4d46180`](https://github.com/bobs-org/bob-cli--plans/commit/4d461800f67260ed99d9ebd1510197189ed1875f) | docs(plans): mark project\_note\_offer\_form done for bob-cli-ex.2.1 landing | [bob-cli-ex.2.1](bob-cli-ex.2.1.md) | 2026-10-31 17:53:33 EDT |
| bob-cli | [`f411232`](https://github.com/bobs-org/bob-cli/commit/f41123201f285887d63e1ed50802c7bd118e38d0) | fix(capture): refuse route-less sealed offers and keep offer mode while incomplete | [bob-cli-ex.2.1](bob-cli-ex.2.1.md) | 2026-11-01 09:53:08 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ex.2.1.1][1] | Need parent epic DECISIONS and phase list | 1 |
| read-by | [agent:bob-cli-ex.2.1.3][2] | Need parent epic decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.2.1.3/README.md

<!-- sase:referenced-by:end -->
