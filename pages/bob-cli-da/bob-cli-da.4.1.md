# Bead: bob-cli-da.4.1 — Split embedded assets into a release-managed workspace crate

[Bead Pages](../README.md) / [bob-cli-da.4](bob-cli-da.4.md) / bob-cli-da.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-da.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.4.md) · **Assignee:** `bob-cli-da.4.1.land`
**Created:** 2026-10-27 16:43:43 EDT · **Closed:** 2026-10-27 18:40:59 EDT
**Plan:** [202610/embedded\_assets\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/embedded_assets_split.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/embedded_assets_split.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/embedded_assets_split.md

<!-- sase:links:end -->

## Description

Complete bob-cli-da.4 with byte-identical embedded assets in a separate crate, both archives verified below their size budgets, and the daily release train supporting the workspace without changing Bob's installed behavior.

## Notes

[2026-10-27T22:08:44Z · bob-cli-da.4.1.land] LAND AUDIT at 3cc63511: reviewed this epic (no pre-existing notes), every note on closed children bob-cli-da.4.1.1 and bob-cli-da.4.1.2, both implementation commits b63e5a04 and 3cc63511, and plan:202610/embedded_assets_split.md. Parent DECISIONS assets_split=split_now is honored; b9_close_gate belongs to the sibling phase. Compared every one of the 24 relocated font/vendor/license/provenance files byte-for-byte against b63e5a04^: all equal and no original-path duplicates remain. All 27 src/scripts.rs installed paths/executable flags are unchanged; print-font facade and 11-of-13 sharing tests remain. Reviewed Cargo workspace/dependency/manifests, Rust embedding, three Python fallback consumers, docs generators, package gate, release config/workflow, outputs, previews, and tests. Root remains 0.4.0; assets 0.1.0 is independent, unique tags and assets git_release_enable=false preserve the root contract; git_only and schedule are unchanged; CHANGELOG.md is untouched. Post-start drift reviewed: f6287847 PLAN/daily-home change, 6b0a30bf Mermaid extraction fix, a6a359b8 theme split. Mermaid edits coexist with crate asset fallback, and other changes need no assets integration. Current branch equals origin/master. Fresh cargo fmt --all -- --check and just check-release-tools (108 tests) pass. Both epic-symbol queries (this epic and bob-cli-da.4) report none; no just symvision recipe currently exists. Child reports record full package verification, source/installed adapter checks, docs gates, and pinned release-plz 0.3.173 rehearsals; final integrated just check, docs, adapter and full package gates still belong to the closeout tale. DISCOVERED ISSUE: test_package_check.py has no missing-archive main-path test; test_size_failure_applies_to_either_archive only calls size_level and does not exercise either package through main. The original plan explicitly requires these cases, so finish them in this epic rather than filing a task.

[2026-10-27T22:08:48Z · bob-cli-da.4.1.land] FOLLOW-UP TRIAGE COMPLETE before tale proposal: collected both PROPOSED FOLLOW-UP entries from bob-cli-da.4.1.2 (the only child proposals). Used sase_new_task, searched same-type memory and then all task types, swept last-week tasks, and reviewed active epic scopes plus parent bob-cli-da / phase bob-cli-da.4 / existing task bob-cli-ai. (1) Child .2 note #1, how-the-release-train-works.md still calls assets splitting a future choice: ACCEPTED AS REMAINING EPIC WORK, not a new task. The split made that sentence stale; the closeout tale will update this guide and directly affected root/assets release wording. (2) Child .2 note #2, create a successor to decisions:bob-cli-releases-ride-a-daily-train merely because its assets-size reopening trigger occurred: DECLINED. Read the accepted record and reviewed the trigger against the approved embedded_assets_split fixed design. Reopening means reconsideration, not automatic supersession; the selected design deliberately retains the scheduled train, root once-per-New-York-day guard, exact-SHA CI, release-plz version/changelog ownership, and root binary-release contract. No accepted policy claim was reversed, so a successor record is unwarranted. The workspace/tag/package details already belong to the updated release reference and approved plan. The accepted decision remains immutable. No genuinely distinct non-epic follow-up was found; no new task or duplicate +1 was warranted. Copy these outcomes into the eventual close note. Leave bob-cli-ai and containing epic bob-cli-da for their parent lander as required by the approved child plan.

[2026-10-27T22:40:59Z · bob-cli-da.4.1.land--1] Completed the approved assets split closeout at 3cc6351158e074791330ad539761ad9dbcadd2f6. Audited all 24 relocated payload, notice, and provenance files as byte-identical to the pre-move tree with no old-path duplicates; all 27 installed asset paths and executable flags remain unchanged, and the print-font facade preserves its 11-of-13 shared reader faces. Reviewed Rust embedding, Cargo package metadata, Python source fallbacks, docs generators, release configuration/workflow, previews, outputs, and tests; reviewed drift f6287847, 6b0a30bf, and a6a359b8, preserving Mermaid fallback behavior. Added package_check.main coverage for a missing archive and independent size failure for each package, warning-with-success, and full verification as the default. Updated the stale release guide and clarified independent package release wording and root-only binary selection. Gates: cargo fmt --all -- --check passed; just check-release-tools passed 110 tests; just check-web-clip-adapter passed for source and installed paths; just docs-check passed 447 tests with one font-generation dependency skip; full just package-check verified both archives. bob-obsidian is 3,227,889 bytes (3.08 MiB; 5,160,719 bytes / 4.92 MiB below the 8 MiB warning); bob-obsidian-assets is 5,004,754 bytes (4.77 MiB; 3,383,854 bytes / 3.23 MiB below warning), versus the 8,220,034-byte pre-split root baseline. The existing just check ToolRun 4cb40f0989e9f203cd9e4c99fc4b6dfc has two themes split catalog/completion failures tracked on bob-cli-db; source and test files are outside this scope, so the failure is preserved. epic-symbols is clean and no just symvision recipe exists. Follow-up #1, the stale guide, was accepted and resolved here without a separate task. Follow-up #2, a successor daily-train decision, was declined after review: the trigger warranted reconsideration, but the approved design retains the train and no accepted policy claim reversed. No distinct non-epic follow-up or duplicate +1 was warranted. Leave bob-cli-da and bob-cli-ai open for the containing epic lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-da.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.4.1.land.md) | [bob-cli-da.4.1](bob-cli-da.4.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`232d68c`](https://github.com/bobs-org/bob-cli/commit/232d68c0058bed3d83af0f714901bd2067ad039f) | test(release): cover split package checks and clarify release docs | [bob-cli-da.4.1](bob-cli-da.4.1.md) | 2026-10-27 18:42:58 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-da.4.1.1][1] | Check parent epic decisions before closing phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-da.4.1.1/README.md

<!-- sase:referenced-by:end -->
