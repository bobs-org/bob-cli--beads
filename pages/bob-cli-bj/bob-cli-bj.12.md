# Bead: bob-cli-bj.12 — Relation label vocabulary landing repairs — green Mac build and tests, bounded catalog cache

[Bead Pages](../README.md) / [bob-cli-bj](README.md) / bob-cli-bj.12

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-bj.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bj.land.md) · **Assignee:** `bob-cli-bj.12.land`
**Created:** 2026-10-24 20:05:46 EDT · **Closed:** 2026-10-24 20:55:13 EDT
**Plan:** [202610/relation\_label\_vocabulary\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary_landing_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/relation_label_vocabulary_landing_repairs.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/relation_label_vocabulary_landing_repairs.md

<!-- sase:links:end -->

## Description

Finish the remaining work that epic bob-cli-bj caused. The bob-mac-capture app target builds again. Every relation-card XCTest compiles and passes on macOS CI. The relation-label catalog cache stops growing by one file per vault.

## Notes

[2026-10-25T00:42:10Z · bob-cli-bj.12.land] LAND AUDIT: Read the repair plan, every child scope and note (bj.12.1-.3; no PROPOSED FOLLOW-UP entries), parent plan and all bj.1-.11 notes. Inspected bob-cli d8a8f1f8 cache source/tests and Mac a2e230e + 569cb36 diffs. CI https://github.com/bobs-org/bob-mac-capture/actions/runs/40146325983 on 569cb364b021cd3e5ae611baed1be9aebb0cbb20 passes Lint, Build and XCTest compilation; required suites pass 47/47 relation panel, 33/33 separator toggle, 13/13 presentation, 29/29 dependency decoding. Exactly 2 of 3087 tests fail: existing non-epic bob-cli-bv (RefsPanelModelTests:2312) and bob-cli-bw (inbox route argv:32); both corroborated with +1. Bundle/signature/smoke/install skipped due to those failures. No unrelated commits since repair creation in the three repositories; audited tips bob-cli d8a8f1f8, Mac 569cb36, plugins 21e9923. Parent-period inbox routes still use common commit_capture_batch, cache invalidation and after-success hides; theme cache, Highlights and Day strip changes do not require further repair integration. Shared vectors match byte-for-byte; 55 focused plugin relation tests pass. No epic-symbols for bj.12 or bj, and no symvision recipe in bob-cli. Remaining EPIC-CAUSED defect: scan.rs removes ANY aged .tmp and every noncurrent version. Exact workspace binary reproduced deletion of unrelated.tmp and future catalog-v999-<64 hex>.json in isolated scratch cache. Plan requires only obsolete catalog versions and owned atomic temps; finish a small tale to narrow matching and add preservation regressions before closing. Inherited DECISIONS honored; no memory edits.

[2026-10-25T00:42:52Z · bob-cli-bj.12.land] FOLLOW-UP TRIAGE before tale proposal: bj.12.1-.3 contain no PROPOSED FOLLOW-UP entries. Re-read all parent bj.1-.11 notes and parent land note 3; used sase_new_task, searched all task statuses, swept the past week, and inspected active epics. Outcomes: (1) bj.1#1, bj.3#2, bj.5#1, bj.6#1, bj.7#1, bj.8#1, bj.9#1, bj.10#1, bj.11#1 Task Relation sentence and bj.2#1 Relation label glossary entry remain consolidated in ready memory task bob-cli-bu; no duplicate and no memory edit. (2) bj.8#2 stage-ranker 16ms report remains bob-cli-3w with prior land corroboration; no fresh timing failure observed in this audit and no duplicate +1. (3) bj.3#3 rename snapshot invalidation proposal declined as completed by rename.rs:375 and :842. (4) bj.4#2, bj.5#2/#3, bj.6#2 old clean-base gate failures declined as resolved: theme/completion/help fixes landed in 09b26957 and current just check on d8a8f1f8 passed all 5641 tests (18 result records), fmt and clippy. (5) Revisited prior feature ineligibility: current task(feature) catalog explicitly says agents=yes. bj.4#1 reference-rename transaction reuse is now ready large feature bob-cli-bx, with related links to bob-cli-az and bob-cli-b8; it needs planning to preserve PDF moves, scan locks, rollback and identity behavior. bj.1#2 reliable macOS precommit verification is now ready large feature bob-cli-by, scoped to the missing AppKit/XCTest coverage rather than the already-solved Linux formatter availability. Neither is required for this cache repair. (6) Parent hidden-before-count notes 1/2 are fixed in 556bb67 and now verified by actual XCTest compilation. (7) Current CI failures remain existing ready bob-cli-bv and bob-cli-bw, each +1 corroborated from run 40146325983; no new tasks. Current repair defect (overbroad cache sweep) stays epic work in the proposed small tale. Carry these outcomes into the eventual close note.

[2026-10-25T00:55:13Z · bob-cli-bj.12.land] CLOSEOUT (relation-cache-pruning tale): Constrained the over-broad catalog sweep in src/native/relation_labels/scan.rs. sweep_catalog_cache now only acts on the generated basename catalog-v<version>-<64 hex>.json and on owned atomic-write temps .catalog-v<version>-<64 hex>.json.<pid>.tmp (numeric PID); all other names, including unrelated.tmp, are left alone. sweep_catalog_file deletes only versions older than CACHE_VERSION (hash-validated); future versions are preserved; current-version keeps the existing vanished-vault/keep-vault/malformed rules. Age check (10 min) applies only to eligible owned temps.

Regression: extended catalog_scan_prunes_vanished_vaults_and_sweeps_orphan_files to keep proving vanished-vault, stale-version, and stale current/older temp deletion, and to preserve an aged unrelated.tmp, a future-version catalog, an aged future-version atomic temp, malformed catalog names (short hash, non-numeric version), and malformed temps (non-numeric PID, short hash), plus the existing live-cache, unparseable, unrelated-text, and fresh-temp keeps. Real Catalog::load in scratch cache; XDG isolated; no new public API; no doc change (existing pruning sentence already describes intended behavior).

Verification: just check passes (fmt, clippy, 5641 tests across 18 result records incl. empty doctests, 0 failures).

Mac CI evidence (carried from bj.12.land audit): run 40146325983 on 569cb36 passes Lint, Build, XCTest compilation; 47/47 CaptureRelationPanel, 33/33 separator-toggle, 13/13 presentation, 29/29 dependency-decoding pass. Only bob-cli-bv and bob-cli-bw fail (pre-existing, outside this epic).

Drift review: bob-cli d8a8f1f8, bob-mac-capture 569cb36, bob-plugins 21e9923 unchanged since the repair audit; inbox routing still uses commit_capture_batch with invalidation + one-off hides; no integration edit needed.

Follow-up outcomes carried from bj.12 land notes: glossary proposals stay in bob-cli-bu; stage-ranker timing stays in bob-cli-3w; rename snapshot invalidation already resolved (rename.rs:375/:842); old theme/help/gate failures resolved (09b26957); ref-rename transaction proposal is now ready task bob-cli-bx; macOS precommit verification proposal is now ready task bob-cli-by; non-epic Mac failures remain bob-cli-bv and bob-cli-bw.

epic-symbols clean for bob-cli-bj.12 and bob-cli-bj; bob-cli justfile has no symvision recipe (explicitly unavailable).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-bj.12.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-bj.12.land.md) | [bob-cli-bj.12](bob-cli-bj.12.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`303d8d2`](https://github.com/bobs-org/bob-cli/commit/303d8d248aae658feff47d7be9415b0e26c2929a) | fix(relations): constrain catalog sweep to owned files and older versions | [bob-cli-bj.12](bob-cli-bj.12.md) | 2026-10-24 20:56:48 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-bj.12.1][1] | Need epic decisions and plan context | 1 |
| read-by | [agent:bob-cli-bj.12.2][2] | Need epic DECISIONS and scope for phase 12.2 | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.12.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-bj.12.2/README.md

<!-- sase:referenced-by:end -->
