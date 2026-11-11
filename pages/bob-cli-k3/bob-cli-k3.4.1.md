# Bead: bob-cli-k3.4.1 — Album schemas for records, capture, and completion

[Bead Pages](../README.md) / [bob-cli-k3.4](bob-cli-k3.4.md) / bob-cli-k3.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-k3.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.4.md) · **Assignee:** `bob-cli-k3.4.1.land`
**Created:** 2026-11-11 09:19:33 EST · **Closed:** 2026-11-11 13:33:32 EST
**Plan:** [202611/album\_record\_consumers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_record_consumers.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/album_record_consumers.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_record_consumers.md

<!-- sase:links:end -->

## Description

Complete bob-cli-k3.4 so every record consumer uses its effective vault's album schemas, records carry album identity, and albums refuse tasks.

## Notes

[2026-11-11T16:57:13Z · bob-cli-k3.4.1.land] LANDING AUDIT / FOLLOW-UP TRIAGE: Read bob-cli-k3.4.1 and all four children, including every note (one, two, one, and one notes respectively). No child contains a PROPOSED FOLLOW-UP entry; no proposals were declined or filed and no independent out-of-scope issue was discovered. All remaining defects below were introduced in this epic and remain epic work, not new task beads. Reviewed commits f7332f58, 8edd5a5f, c36e6e75, 3d1c0763 and actual registry/context/render/records-check/CLI/capture/parse/targets/completion/task-home implementations. The four phase reports describe real landed code, but the epic is not ready to close. Final parent DECISIONS were read: no new memory edits, no declined albums decision, and outer ledger/glossary work remains assigned to its phases.

DISCOVERED ISSUE: capture_record.rs keeps an independent legacy config map; registry Unclaimed/DiscoveryIncomplete/read-error results can fall through resolve_record_route to configured_dir and route_kind_for to config. A restaurant album at eat.md suppresses config restaurant dir old_eat, yet the old route can be resurrected; parse planning skips the same Unclaimed outcome. Valid.warnings is discarded, dropping records_config_deprecated. Completion route_diagnostic_result searches the entire draft, so another item's broken album can block a healthy named-field picker or intercept notebook completion. records check skips whole album trees despite immediate-only membership; partial discovery errors are hidden in JSON and do not affect status. Bare-album parse rewrites are offered even when the owner cannot resolve. These are source-inspection findings for regression tests and repair, not claims of fresh runtime reproduction.

INTEGRATION: reviewed post-start non-epic commits 7eb82440 and 921e51d9 (SVG), f9d998c1 (staged notebook sections), and db91ab20 (keep-moving docs). Fetched master and fast-forwarded to db91ab20. SVG/keep-moving need no album adaptation; the remaining completion repair must preserve staged notebook menus through the shared dispatcher. docs/records.md still explicitly says capture/records read config until k3.4; the five landing docs and integrated acceptance remain unfinished. No fresh just check was run during this planning audit; child .2 reports ToolRun 075822f0ee1567d32188ce6125793f24 passed. Both epic-symbols bob-cli-k3.4.1 and bob-cli-k3.4 report no entries; no symvision recipe currently exists. The research ref named in the original child plan returned missing; both approved plans were audited successfully.

NEXT: validated medium tale sase_plan_album_consumer_landing_repairs.md covers only these repairs, docs, isolated walkthrough, just check/docs gates, then normal closure of bob-cli-k3.4.1, marking plan:202611/album_record_consumers.md done, and normal closure of parent phase bob-cli-k3.4. It leaves bob-cli-k3 open and does not depend on the final code's future SHA/push/CI.

[2026-11-11T17:21:55Z · bob-cli-k7.land] DISCOVERED ISSUE: (found by the bob-cli-k7 land agent) just check fails on bob-cli master db91ab20 at -p bob-obsidian --lib: native::capture_link_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates (src/native/capture_link_tasks.rs:883) gets 2 warnings, expected 1. Deterministic in 3 isolated reruns (cargo test -p bob-obsidian --lib native::capture_link_tasks::tests::warns_for_unreadable). Warnings: ["locked.md: failed to read file: Permission denied (os error 13)", ".: locked.md: failed to read file: Permission denied (os error 13)"]. Cause: 3d1c0763 (bob-cli-k3.4.1.4) makes capture_targets::scan_capture_targets extend report.issues with the album registry's DiscoveryHealth::Partial errors, so discover_at reports the unreadable note once from the registry scan (vault root '.') and again from its own per-target read. Fix either dedupe the warning or update the test's contract. All other 6479 lib tests pass.

[2026-11-11T18:33:32Z · bob-cli-k3.4.1.land] Landing repairs complete on base db91ab20 plus this turn's uncommitted repairs (host commits after turn). AUDIT: re-read epic plus all four children (k3.4.1.1/1.2/1.3/1.4 all CLOSED done) and every note (1,2,1,1 plus k7.land note 2 below); no child holds a PROPOSED FOLLOW-UP entry. Prior commits f7332f58/8edd5a5f/c36e6e75/3d1c0763 retained. REPAIRS: (1) resolved routing authoritative - new PerRouteDecision::DiscoveryIncomplete, record_policy_for_draft keeps incomplete/read-error as explicit diagnostics (deterministic bad-byte fixtures), route_kind_for and resolve_record_intents no longer fall back for explicit outcomes, records_config_deprecated warnings carried from resolved kinds through policy into capture parse diagnostics, capture execution warnings, capture-targets rows, and records CLI (human+JSON stderr, payloads unchanged); expand_capture now builds policy from the effective -b vault (fixes -E masking against the wrong vault, found via record_field_template regression). (2) completion route errors scoped to the cursor item (album_schema_invalid/records_config_invalid/discovery-incomplete overlap the cursor item only; healthy items and notebook completion no longer intercepted). (3) collect_orphan_records scans album descendants excluding only immediate members (nested stray reports record_outside_album; symlinks/exclusions kept); report_discovery_errors emits for JSON and never blocks healthy single-album commands while full-inventory list/check fail on Partial with partial results retained; list emits config-deprecation warnings; bare-album refusal omits the rewrite and reports unresolvable owner. TRIAGE: k7.land note 2 (warns_for_unreadable 2-vs-1 warnings, caused by this epic's 3d1c0763 double-reporting unreadable files via scan issues plus registry Partial errors) FIXED here by deduping registry errors against scan issues in append_record_targets plus a guard in discover_at; no new task beads (epic-caused defects fixed, no independent out-of-scope defect found). INTEGRATION: reviewed origin/master 07f1c744 (bank), 0f37849b (grammar-26 section bullets, additive section_action hunks in record.rs/capture_parse.rs disjoint from these edits), ba700bcb, 0b4483be - nothing reverted; host merge may touch the same two files in disjoint regions. ACCEPTANCE: new regression tests (suppressed legacy route valid+broken x folder present/absent, bad-byte DiscoveryIncomplete, healthy album amid unrelated bad file, mixed-draft cursor scoping both orders, nested-orphan membership, owner-unresolved no-rewrite); just check FULLY GREEN (lib 6486 pass 0 fail, cli 3546 pass 0 fail, all suites); just docs-gen clean; docs-check passes for all 5 touched pages while 5 untouched pages (mac-capture x4, plugins hotkeys) remain over word budget - pre-existing, unrelated to this epic. Walkthrough (2 albums eat/podcasts + unclaimed config movie): new by noun and stem with source album identity and canonical parent/type storage, config kind warns records_config_deprecated on stderr with clean JSON, staged multi-item parse, dry-run byte-equal to write with zero dry-run writes, -b wins over conflicting BOB_DIR, broken-podcast isolation with healthy eat listed, bare-album refusal with owner rewrite and writeless failures, identical identity across records/parse/targets, record-only writes with owner notes byte-unchanged.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.4.1.land.md) | [bob-cli-k3.4.1](bob-cli-k3.4.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6e42159`](https://github.com/bobs-org/bob-cli/commit/6e4215971c02e0f88e12616fee37159fe455f0e1) | feat(capture)!: finish the album consumer landing repairs | [bob-cli-k3.4.1](bob-cli-k3.4.1.md) | 2026-11-11 13:36:26 EST |
| bob-cli--plans | [`bob-cli--plans@2814cf2`](https://github.com/bobs-org/bob-cli--plans/commit/2814cf2080d90274459893f3498694682be87ea1) | docs(plans): mark album\_record\_consumers done after consumer landing | [bob-cli-k3.4.1](bob-cli-k3.4.1.md) | 2026-11-11 13:37:21 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k3.4.1.1][1] | Need parent epic decisions and current phase plan context | 1 |
| read-by | [agent:bob-cli-k3.4.1.3][2] | Need child epic phase statuses | 1 |
| read-by | [agent:bob-cli-k7.land][3] | Need the epic scope to attach a causally related discovered CI failure | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.4.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k3.4.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-k7.land/README.md

<!-- sase:referenced-by:end -->
