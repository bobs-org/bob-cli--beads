# Bead: bob-cli-ey.7 — Finish capture drawers (bob-cli-ey landing repairs)

[Bead Pages](../README.md) / [bob-cli-ey](README.md) / bob-cli-ey.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.land.md) · **Assignee:** `bob-cli-ey.7.land`
**Created:** 2026-11-01 03:50:52 EST · **Closed:** 2026-11-01 09:20:05 EST
**Plan:** [202611/finish\_capture\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_capture_drawers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/finish_capture_drawers.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_capture_drawers.md

<!-- sase:links:end -->

## Description

The drawer contract from the parent epic is fully shipped. `Text @foo+bar#requirements #fix` files the note and retypes `^bar` in one transaction. Drawer creation writes clean Markdown. bob reports the drawer object, the drawer span fields, refusal codes, the near-catalog warning, and the full drawer menu. Bob Mac Capture's fixtures are generated from that real bob, and macOS CI fails only bob-cli-f3's seven baseline tests.

## Notes

[2026-11-01T13:18:20Z · bob-cli-ey.7.land] LAND FOLLOW-UP TRIAGE: bob-cli-ey.7.2 note #1 proposes skipping drawer cache writes when no note changed. Declined as written: load_drawer_catalog persists last_scan_unix in the same JSON cache; after TTL expiry, omitting that write leaves every later process outside the 60-second TTL and forces repeated vault enumeration/aggregation. recent_count also ages with time even without note changes. The measured warm menu delta (+6 ms) meets the approved <=~20 ms target. A redesigned cache layout would be optional optimization, not unfinished drawer functionality; no task bead warranted for the proposed change. No other PROPOSED FOLLOW-UP entries occur in the four repair phases.

[2026-11-01T13:27:22Z · bob-cli-ey.7.land] LAND FOLLOW-UP TRIAGE (additional readiness findings): global sase plan links validate reports 58 unrelated historical errors, none naming this epic or its parent/descendant plans. Through sase_new_task: corroborated existing canceled stale-triage task bob-cli-y with a fresh post-close reproduction of its 57 prompt-in-plans-store errors (original proposer bob-cli-t.4.4); no duplicate created. The distinct 202610/bob_cli_7b_mac_compile.md PLAN-versus-PROMPT link-kind error was filed as small bug bob-cli-f4 and marked ready, proposed by this lander. Task/last-week sweeps across types and all 12 active epic scopes found no causal owner or duplicate for f4; bob-cli-1v and bob-cli-dg were reviewed and declined as duplicates because they cover wrong commit trailers and missing sidecars, respectively. Epic-linked plans resolve correctly; cli_directives_split and mac_directives are done. Keep these historical provenance issues out of drawer implementation.

[2026-11-01T13:28:53Z · bob-cli-ey.7.land] LAND AUDIT: Read this epic and all four phase scopes/notes, normative repair and parent plans, parent decisions, and all parent descendant notes. Reviewed actual bob-cli commits f2b599c4/c7afa6d0 and current planner/parser/resolver/menu/tests, Mac b48d1b4/361e929 and real fixture generators/Swift decoding/preview, and plugin bff0345. Fresh scratch smokes at bob-cli 9625c9ac pass normal drawer/plain-child retyping, new-drawer exact bytes, JSON drawer object, named refusal codes and near-catalog warning, task/recent/new menus, D8 relocation with lane unchanged, refusal/later-item vault rollback, percent-n/listen/history/template directives, and bare-hash/percent unselected menus. Three epic-caused gaps remain: (1) valid ID-less --task-ref plus note #fix, with or without --drawer, exits 1 requiring a block ID (plan.rs sub_bullet_retype unwrap); (2) note @foo+bar # and note @foo+bar#requirements # report subject=new while typed #fix reports existing (incomplete mode drops task_types.rs sub_bullet_existing); (3) #req near REQUIREMENTS tells the user to quote REQUIREMENTS to create REQUIREMENTS, whereas parent section 3.2 requires the requested REQ override. The writer also lacks the approved focused exact-byte and transactional regression coverage. A medium tale will repair only these remaining paths and finish this epic and parent bob-cli-ey in the same implementation turn. Do not close yet. Mac CI 41308048455 snapshot d85e98c1 is tree-identical to landed 361e929 (git diff empty); build/lint passed and failure logs confirm exactly bob-cli-f3 seven baseline methods, no epic regressions. Mac retirement grep and bash syntax checks pass. Plugin promotion/reversal node suites: 68 passed. Integration: fetched bob-cli origin/master=9625c9ac; later non-epic 9625c9ac and plugin ba0a6ee affect Keep indicator docs/icons only; no required capture integration. Mac has no non-epic post-start drift. No release-version or changelog edits; both Rust wire-break commits use ! and BREAKING CHANGE. epic-symbols for ey.7 is empty and just symvision is absent. Follow-up dispositions are in preceding triage notes; no epic defects deferred to task beads.

[2026-11-01T13:31:27Z · bob-cli-ey.7.land] BASELINE VERIFICATION: sase tool run check (ToolRun 675c171311cf44f7ce050d9fe2403261, argv just check) succeeded with exit 0 in 628898 ms on bob-cli 9625c9ac. No product source edits during the run. Never ran just check-full. Existing tests are green despite the three independently reproduced acceptance gaps in the preceding land audit. The medium repair tale must add their regressions, rerun just check after fixes, and finish both normal closeouts.

[2026-11-01T14:20:05Z · bob-cli-ey.7.land--1] Retype closeout repairs landed and verified. (1) ID-less --task-ref retype: plan.rs sub_bullet_retype now resolves Ref without block ID via new task_theme apply_type_marker_to_existing_line (line-index edit, no minted ID/link/lane change); stale/ambiguous refs preserved; child insert uses recomputed ref; D8 relocation kept for existing IDs; full batch stays atomic with dry-run writing nothing. (2) Bare-marker existing context: task_types build_inner derives sub_bullet_existing from SubBulletRoute+SubBulletBlockId spans in Incomplete mode so 'note @foo+bar #' and 'note @foo+bar#requirements #' report existing like their typed forms; new @route^id stays new; inherited/current type consistent; empty query keeps initial_selection none. (3) Near-duplicate override: resolve_drawer_for_write suggestion stays near.slug but quoted creation now uses requested selector intended title with writer casing/key rules, so #req refuse teaches write #"REQ" to create REQ; task-drawer and ^prj H2 scope wording kept; completion menu inherits via same resolver. (4) Acceptance pinning: new tests/cli/capture/retype_closeout.rs (641 lines, table-driven) plus touched complete_drawers/prj_drawers/drawers unit tests cover ID-less plain/drawer refs, existing-ID refs, inherited clearing, stale/ambiguous, later-item rollback, new-drawer+type, tab/space/CRLF/EOF/managed-log bytes, closed/unconfigured/strict-cap/later-failure snapshot, JSON drawer object/spans/refusal codes. Verification: sase tool run check ToolRun 7432c6e6cf416c9d2f669749877f67a6 exit 0. No Cargo.toml/CHANGELOG edits; grammar 3 schema 1 unchanged; no new wire breaks (prior feat! + BREAKING CHANGE footers stand); no docs/help changes so no docs-gen needed. Integration: origin/master drift since 9625c9ac is only 81b3b5a4 Keep footer docs (no capture integration); no Mac/plugin source changes this turn; Mac CI 41308048455 evidence stands. Follow-ups per epic notes: 7.2 cache-write proposal declined (loses persisted TTL rescan, warm +6ms meets target, no bead); historical plan-link errors triaged via sase_new_task: 57 legacy corroborated on bob-cli-y, distinct bob_cli_7b provenance error filed as bob-cli-f4 ready, bob-cli-1v/dg declined as non-duplicates; no epic-linked plan errors. epic-symbols empty for ey.7.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.7.land.md) | [bob-cli-ey.7](bob-cli-ey.7.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`12078cc`](https://github.com/bobs-org/bob-cli/commit/12078cc59ffdf66155dc3a519f711fb99b4be20f) | fix(capture): retype ID-less picker refs, bare-marker existing subject, near-duplicate override | [bob-cli-ey.7](bob-cli-ey.7.md) | 2026-11-01 09:21:54 EST |
| bob-cli--plans | [`bob-cli--plans@1c71fab`](https://github.com/bobs-org/bob-cli--plans/commit/1c71fabf2418250b3bfa9fcbc0b2de7bd10f9fce) | docs(plans): mark finish\_capture\_drawers and capture\_drawers\_and\_directives done | [bob-cli-ey.7](bob-cli-ey.7.md) | 2026-11-01 09:22:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ey.7.1][1] | Need epic DECISIONS and plan pointer | 2 |
| read-by | [agent:bob-cli-ey.7.2][2] | Need epic decisions and notes | 2 |
| read-by | [agent:bob-cli-ey.7.3--2][3] | Need epic DECISIONS before closing mac-ci-regressions phase | 1 |
| read-by | [agent:bob-cli-ey.7.4--c][4] | Confirm inherited epic decisions before closing phase bob-cli-ey.7.4 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.7.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ey.7.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.7.3.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.7.4.md

<!-- sase:referenced-by:end -->
