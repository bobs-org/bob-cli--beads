# Bead: bob-cli-kx.2.1.8 — Gmail archive-on-close landing repairs

[Bead Pages](../README.md) / [bob-cli-kx.2.1](bob-cli-kx.2.1.md) / bob-cli-kx.2.1.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.1.land.md) · **Assignee:** `bob-cli-kx.2.1.8.land`
**Created:** 2026-11-12 23:51:15 EST · **Closed:** 2026-11-13 07:47:33 EST
**Plan:** [202611/gmail\_archive\_landing\_repairs.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_landing_repairs.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_archive_landing_repairs.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:1e7c765d5bd3a77bc9aa19a1 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_landing_repairs.md

<!-- sase:links:end -->

## Description

Finish epic bob-cli-kx.2.1 by repairing the land-audit defects in the Gmail archive core: frozen saved IDs, journaled-before-mutation ownership, receipt label identity, boundary revalidation, filing-safe error reporting, preview parity, and accurate reports, help, and docs.

## Notes

[2026-11-13T11:59:02Z · bob-cli-kx.2.1.8.land] FOLLOW-UP TRIAGE: Reviewed all four child beads and every note. The only PROPOSED FOLLOW-UP is bob-cli-kx.2.1.8.4 note #1 (docs-check offline lychee mac-capture/event-notes). Under /sase_new_task, searched ci tasks across all statuses, swept the last week, read bob-cli-l7, and inspected active epic scopes. It is the existing bob-cli-l7 root cause: docs/gcal-notes.md:22 still uses ../reference/mac-capture/event-notes.md from the docs root, introduced by 23e7f90d before these Gmail repairs. Corroborated l7 with +1; no new task and no proposal declined. No active epic has a causal link to that original bad path. Gmail defects found in this landing remain epic work and will be included in the repair tale.

[2026-11-13T12:04:09Z · bob-cli-kx.2.1.8.land] LAND AUDIT at f508aa46: NOT READY TO CLOSE. Read all four children and every note, both repair/core plans, parent landing notes, original children, and binding DECISIONS on kx.2. Reviewed repair commits dcd908ab, 642e1580, 6b9261a7, a8dd8204 and actual apply/preview/scan/state/transport/report orchestration. Frozen IDs, real receipt IDs, rename baseline, [?], journal preplanning, scoped let-go, hydration capture, filing preservation and surfaces are present. Remaining epic defects: (1) the per-thread fresh scan extracts evidence without checking scan_complete, ignoring newly unreadable vault notes; its reopen test is a production environment shortcut that returns the desired hold before performing revalidation, not an actual race test; the forced-archivable test similarly overrides the verdict. (2) apply_live loses accumulated successful rows on Err, and command.rs discards the outcome, hiding earlier same-run archives on later auth/journal failure; the auth test only preserves a previous runs archive. (3) preview marks only HOLD_FETCH_FAILED unsuccessful, so a fresh HOLD_UNRESOLVABLE close can exit successfully. (4) invalid_grant remains runtime exit 1, and the new test asserts 1, contrary to the repair plan auth exit 2. (5) the new proptest generator can alias enrollment Label_1 and panic: PROPTEST_CASES=65536 PROPTEST_DISABLE_FAILURE_PERSISTENCE=1 cargo test --lib label_diff_properties_hold_for_independent_message_labels -- --nocapture failed after 1793 successes, shrinking to cases=[(0,{})], label_suffix=1, name_suffix=comma; evidence file:explicit:1e7c765d5bd3a77bc9aa19a1. Its generic random label sets also never contain INBOX or the actual receipt. These are remaining epic work, covered by the medium tale sase_plan_gmail_archive_finish.md, including real fake-transport faults and full nested closeout. Integration: non-epic commits after dcd908ab are 78c0e085 capture field completion and f508aa46 album test evidence; neither consumes/conflicts with archive. Shared JSON docs preserve grammar 27. No integration edits required. Follow-up triage is recorded in the preceding note (l7 +1 only). epic-symbols lists no entries; justfile has no symvision recipe. No epic or plan marked done; no just check-full run.

[2026-11-13T12:47:33Z · bob-cli-kx.2.1.8.land] Implemented the remaining approved Gmail archive landing repairs: fresh vault scans must be complete before mutation; fake-gog race hooks now mutate synthetic vault/remote state at the boundary; live outcomes retain prior successful rows across later fatal errors; archive invalid_grant reports exit 2 and a modify-login hint; unresolvable fresh rows fail in preview and live; property generation excludes enrollment aliases while covering INBOX, receipt, enrollment, and unrelated labels. Verified 65,536 proptest cases, all 184 tests across the 11 Gmail integration targets, gmail_archive_apply (30), just docs-gen, and docs-check lint/generated/build/URL stages. just check remains red only on the known bob-cli-l2 GCal assertion and bob-cli-kl pipe-drain flake; exact rerun of kl passed. docs-check's offline lychee stage still reports the known bob-cli-l7 mac-capture relative link. No symvision recipe or epic-symbol entries.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2.1.8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.1.8.land.md) | [bob-cli-kx.2.1.8](bob-cli-kx.2.1.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`fada115`](https://github.com/bobs-org/bob-cli/commit/fada115450d2ab8fc55c461c59401014f97ebd35) | fix(gmail)!: fail closed at archive mutation boundaries | [bob-cli-kx.2.1.8](bob-cli-kx.2.1.8.md) | 2026-11-13 07:55:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.8.3][1] | Need the epic decisions and cross-phase integration contract before implementing this phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.8.3/README.md

<!-- sase:referenced-by:end -->
