# Bead: bob-cli-c9.3.1.6 — Finish ref create rereads - landing fixes for bob-cli-c9.3.1

[Bead Pages](../README.md) / [bob-cli-c9.3.1](bob-cli-c9.3.1.md) / bob-cli-c9.3.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.land.md) · **Assignee:** `bob-cli-c9.3.1.6.land`
**Created:** 2026-10-25 19:48:33 EDT · **Closed:** 2026-10-25 22:19:18 EDT
**Plan:** [202610/ref\_reread\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_reread_landing_fixes.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/ref_reread_landing_fixes.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_reread_landing_fixes.md

<!-- sase:links:end -->

## Description

Every gap the bob-cli-c9.3.1 land review found is fixed: rereads join only the reference they really repeat, attach and intake keep working on later readings, partial overlaps never reread, every route honours the reread contract, and the docs and tests match the shipped behavior, so the bob-cli-c9.3.1 landing can resume and close.

## Notes

[2026-10-26T01:53:36Z · bob-cli-c9.3.1.6.land] LAND AUDIT at 516d7b98: read the epic, every note on phases .1-.4, the linked landing-fixes plan, and all parent bob-cli-c9.3.1 phase notes plus its previous landing note and plan. Reviewed commits c192014e, e35773e5, d96ed412, 516d7b98 and current intake/doctor, family/birth, create/clip/collection/force/stamp code, docs, and regression tests. Selected decisions are implemented: exact filed URL sets win over larger overlapping collections; full-scan queued-reread collision aborts planning before any move. git fetch origin left origin/master == HEAD; no outside commits landed during this child epic. Parent drift 55334b09 uses the common Markdown render filter, retained by reread routes, with no integration change needed. Remaining epic work found in route_guards: (1) print_reread_narrated_hint returns early when family.newest() has no audio, rather than finding the newest narrated member; the existing test has only v1. (2) newly added exact-output overwrite gates test raw Path::exists, while stamp::resolve_exact_output_path expands tilde and normalizes the path, so a literal ~/existing.pdf can be falsely refused. Plan a small tale with regression tests and same-turn closeout of this epic, then ancestor bob-cli-c9.3.1 and phase bob-cli-c9.3 when readiness checks pass. No source edits or fresh check pass in this audit; sase tool run check reports no configured check tool, so verification must use the documented raw just check fallback. Local target/debug/bob is stale and its exploratory results were discarded. No epic-symbol entries for bob-cli-c9.3.1.6 or bob-cli-c9.3.1; no symvision recipe exists currently.

[2026-10-26T01:53:39Z · bob-cli-c9.3.1.6.land] FOLLOW-UP TRIAGE before remaining-work tale: none of bob-cli-c9.3.1.6.1-.4 has a PROPOSED FOLLOW-UP entry. The sole proposal among parent descendants is bob-cli-c9.3.1.3 note 1 (full-scan raw intake lacks the locked reread occupancy recheck); it was correctly absorbed into this epic and is now addressed by c192014e: plan_xlib_intake invokes the shared whole-bundle check, accumulates conflicts before moves, and the regression asserts both the queued reread and unrelated queued bytes are preserved. No task is warranted for that resolved epic-caused issue. The two current route_guards gaps are also epic work, not task beads. No genuinely distinct unrelated follow-up was identified, and no proposals were declined or left awaiting triage. Preserve the parent landing note deliberate non-goals: ordinary non-versioned full-scan occupancy, ordinary redirect dedupe, index construction, networked URL dry runs, and overwrite-listen legacy attachment remain outside this remainder.

[2026-10-26T02:19:18Z · bob-cli-c9.3.1.6.land--1] Landing complete for bob-cli-c9.3.1.6.

Four-phase/source/decision audit: phases .1-.4 are closed. Decisions remain exact_wins_over_collection=yes and full_scan_collision=abort. Inherited non-goals stand (legacy-only warn+fresh capture, no filed overwrite, no recaptured:, no memory/Cargo.toml/CHANGELOG edits, ordinary full-scan occupancy, ordinary redirect dedupe, per-create index construction, URL dry-run fetching, overwrite-with-listen attach). Land-audit notes #1-#2 already covered c192014e, e35773e5, d96ed412, 516d7b98 plus parent 55334b09 Markdown render filter.

Intervening commits: HEAD and origin/master remain 516d7b98; no commits since that SHA. Uncommitted remainder is this tale's two guards plus tests.

Narrated-member hint: print_reread_narrated_hint now selects the first family member with audio (members are newest-first) instead of returning when family.newest() is silent. route_guards_plain_reread_names_narrated_reading_without_inheriting seeds narrated v1/v2 and silent v3; dry-run and actual capture both hint "v2 is narrated (lib/blogs/existing__v2.mp3)", report existing__v3 → existing__v4, inherit no audio, and leave earlier note/audio bytes unchanged. route_guards_plain_reread_without_audio_has_no_narrated_hint covers the empty-audio path. Shared print_reread_audio_hint still serves create/clip/collection.

Exact-output tilde: overwrite presence now uses stamp::exact_output_exists (resolve_exact_output_path + exists) in force::triage_overwrite_url, collection attach_gate/recapture_gate, and create Markdown/PDF pre-parent probes. Base failures were literal ~/custom.pdf classified as fresh. Tests: route_guards_overwrite_url_exact_output_replaces, route_guards_overwrite_collection_exact_output_replaces, route_guards_overwrite_markdown_exact_output_preparent_probe, route_guards_overwrite_pdf_exact_output_tilde_preparent_probe (existing file under HOME via literal tilde). Already-correct path: highlights_create_overwrite_fresh_url_refuses_before_fetch now also asserts absent ~/absent.pdf still refuses as fresh, fetches/writes nothing. Filed-family overwrite still refuses.

Verification: sase tool run check has no configured named check tool; used plan-approved SASE_TOOL_BYPASS raw just check. Monitor eq3yv7874bfh completed exit 0 (TESTING → TESTED). just --list still has no symvision recipe.

Follow-up dispositions: full-scan occupancy proposal (bob-cli-c9.3.1.3 note 1) absorbed into this epic and fixed by c192014e. No PROPOSED FOLLOW-UP on .6.1-.4. No other proposals, no new unrelated task. No epic-symbol entries for this bead.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.3.1.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.6.land.md) | [bob-cli-c9.3.1.6](bob-cli-c9.3.1.6.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`b48bd93`](https://github.com/bobs-org/bob-cli/commit/b48bd939cb33a5c5a6e9afea690bc4bed06fc3f4) | fix(ref): name newest narrated reading and resolve exact-output overwrite paths | [bob-cli-c9.3.1.6](bob-cli-c9.3.1.6.md) | 2026-10-25 22:22:43 EDT |
| bob-cli--plans | [`bob-cli--plans@3afa34a`](https://github.com/bobs-org/bob-cli--plans/commit/3afa34ac5cfd9e7f1855199c272b51e99e4ddcad) | chore(plans): mark reread landing and create-reread plans done | [bob-cli-c9.3.1.6](bob-cli-c9.3.1.6.md) | 2026-10-25 22:23:40 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.3.1.6.3][1] | Need parent epic scope | 1 |
| read-by | [agent:bob-cli-c9.3.1.6.land--1][2] | Need landing epic status, children, notes, and closeout evidence before closing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.3.1.6.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.3.1.6.land.md

<!-- sase:referenced-by:end -->
