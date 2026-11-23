# Bead: bob-cli-pj.2.1 — Refresh only reference plans affected by concurrent edits

[Bead Pages](../README.md) / [bob-cli-pj.2](bob-cli-pj.2.md) / bob-cli-pj.2.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-pj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pj.2.md) · **Assignee:** `bob-cli-pj.2.1.land`
**Created:** 2026-11-22 18:51:55 EST · **Closed:** 2026-11-22 21:59:35 EST
**Plan:** [202611/refs\_incremental\_coherence.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/refs_incremental_coherence.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/refs_incremental_coherence.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:f0ee94709e52d2aa9074a8ad | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/refs_incremental_coherence.md

<!-- sase:links:end -->

## Description

Complete bob-cli-pj.2 with dependency-aware PDF replanning at all three stale sites, bounded retries outside writer locks, and preserved fail-closed guards.

## Notes

[2026-11-23T02:08:56Z · bob-cli-pj.2.1.land] LAND FOLLOW-UP TRIAGE: Reviewed every note on phases .1/.2/.3; only PROPOSED FOLLOW-UP is bob-cli-pj.2.1.3 #1. Independent just docs-check on 29d7fec7 reproduced three Mac errors and a plugin advisory (file:explicit:f0ee94709e52d2aa9074a8ad). capture-previews 6082 and keyboard 6036: corroborated bob-cli-jz; protocol 6107: corroborated bob-cli-h9. All three crossed 6000 in Mac d76a4849 (bob-cli-on.15.1.5), so recorded DISCOVERED ISSUE on active bob-cli-on.15.1, which owns repair. plugin-apis 8963/8000: corroborated existing feature bob-cli-ob and recorded requirement-API growth on bob-cli-on.11.1. Declined a new CI bug for it because develop budgets are advisory and headroom remediation is already tracked. No duplicate tasks created. Phase .2 Spotify fake-curl transient failure was reported as passing on isolated rerun, not an outstanding phase failure; no independent recurrence observed here.

[2026-11-23T02:11:20Z · bob-cli-pj.2.1.land] LAND VERIFICATION (incomplete): Read all three phase beads and all notes, both linked plans, commits 063a8768/33f6d08d/29d7fec7, implementation and new tests. Dependency classification, shared 4-refresh/1-rebuild budget, pinned date, global ref/source/config handling, destination precedence, and unlocked planning are present; parent stall_after=two_hours remains unchanged. Code review found remaining epic defects: scan_apply Refresh discards next_change and can return no_work before convergence (sole PDF becomes Failed during refresh then is restored before evidence); refresh pre/post comparison uses old observations/Markdown owners, so newly acquired shared reads can become an empty refresh and accept stale output; complete_comparison_evidence leaks previous owners into stable adopted evidence. New real-reader, mixed preparation/lock-budget, and ownership replacement regressions are required. Phase 3 also retains four dead_code allowances for now test-only legacy validation. No fresh Rust gate result claimed by this lander. These repairs are planned as one medium tale whose last step closes this epic and parent phase bob-cli-pj.2. No epic-symbol entries on either bead; no symvision recipe at baseline. Keep both beads open pending repairs.

[2026-11-23T02:11:25Z · bob-cli-pj.2.1.land] LAND INTEGRATION: Fetched origin/master at 29d7fec7; no additional base-branch commits. Reviewed non-epic commits since epic creation, including the two preceding its first implementation: 8c019eb4 Gmail HTML whitespace, fdd94725 property span operations, 9d0cbfbe requirement docs, 7f104e52 dedicated-link Pomodoro history, 3e480e4a property CLI. No duplicate scan implementation or required consumer migration. Property mutations use the maintenance lock and existing Markdown/root/locator evidence; history-only daily edits appropriately re-finalize without unrelated PDF parsing. Remaining repair tale requires another drift check before close.

[2026-11-23T02:59:35Z · bob-cli-pj.2.1.land] LAND VERIFICATION (complete): All three phases closed (.1 dependency classification, .2 preparation refresh, .3 lock-window refresh). Repairs: lock-window Refresh/Rebuild now converge via settle_prepared_scan consuming every returned change (empty-subset, global, destination) before no-work, preserving shared 4+1 budget, pinned date, hooks once, recovery-before-hooks, error codes, receipt ownership, collision validation, and ref_dir global rule; refresh pre/post now unions live owners/observations into comparison-old (OR flags, AND complete) and stores clean post on convergence vs union on mismatch, dropping obsolete owners; retired PreparedValidation/validate_prepared_scan/scan_change_to_validation/is_destination_asset_stale and dead_code allows, tests assert ScanChange directly. Gates: cargo fmt clean; cargo test --lib highlights_ref::scan_plan 31 passed (28 existing + 3 new live-union/ownership/typed); focused cli interleave 11 passed (lock_failed_recovery, stable_no_work 1 line, global rebuild, dest scan_failed, combined prep+lock 6 lines inputs_changed with maintenance during refresh, plus existing lock_stale/subset/finalization/second_edit/failed_recovery/prep_budget/repeated_churn); sase tool run check succeeded exit 0 in 442501ms run 9d1be27cee08c4bf935c9c3a581e780c (fmt, clippy, full workspace tests); just docs-check fails identically to baseline (capture-previews 6082, keyboard 6036, protocol 6107, plugin-apis 8963) with no new failures, no docs changed. Drift: origin/master moved 2 docs-only commits ef640fde (task-dependencies Mac Pull-In) and bf005290 (task-requirements close behavior), no scan impact, no consumer migration needed. Triage retained from land notes: Mac overages to on.15.1 (DISCOVERED ISSUE), jz/h9 corroborated, plugin-apis to ob/on.11.1, no new tasks. Epic-symbols empty on both beads; no symvision recipe.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pj.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pj.2.1.land.md) | [bob-cli-pj.2.1](bob-cli-pj.2.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`15225a6`](https://github.com/bobs-org/bob-cli/commit/15225a6a7b86e887c7b35a655c719ce197efbc88) | feat(highlights-ref): converge refresh with live dependencies and lock-window settle | [bob-cli-pj.2.1](bob-cli-pj.2.1.md) | 2026-11-22 22:01:49 EST |
| bob-cli--plans | [`bob-cli--plans@b000b3b`](https://github.com/bobs-org/bob-cli--plans/commit/b000b3ba6773cf4ef8ab07ee830be978624ce8b6) | chore(plans): mark refs\_incremental\_coherence done after verified landing | [bob-cli-pj.2.1](bob-cli-pj.2.1.md) | 2026-11-22 22:02:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pj.2.1.1][1] | Need parent epic DECISIONS shown by bead read | 6 |
| read-by | [agent:bob-cli-pj.2.1.2][2] | Need epic decisions governing the preparation refresh phase | 1 |
| read-by | [agent:bob-cli-pj.2.1.3][3] | need epic decisions and status | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pj.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pj.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-pj.2.1.3/README.md

<!-- sase:referenced-by:end -->
