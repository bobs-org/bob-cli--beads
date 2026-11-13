# Bead: bob-cli-kx.2.1 — Gmail archive-on-close core

[Bead Pages](../README.md) / [bob-cli-kx.2](bob-cli-kx.2.md) / bob-cli-kx.2.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kx.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.md) · **Assignee:** `bob-cli-kx.2.1.land`
**Created:** 2026-11-12 11:37:44 EST
**Plan:** [202611/gmail\_archive\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_core.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_archive_core.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_archive_core.md

<!-- sase:links:end -->

## Description

Complete bob-cli-kx.2 with opt-in one-shot Gmail archiving, positive closed-task evidence, constrained label writes, crash recovery, digest-confirmed backlog and burst handling, accurate reports, and verified documentation.

## Notes

[2026-11-13T04:45:43Z · bob-cli-kx.2.1.land] LANDING FOLLOW-UP TRIAGE (bob-cli-kx.2.1.land): Every child PROPOSED FOLLOW-UP was reviewed. (1) kx.2.1.1 #1, the mounted bob-plugins validation.md -> bob-vim-yank-flash.md#verification link: declined, because the bob-cli-kb landing already repaired it (kb landing notes record the validation.md fix); not caused by this epic. (2) kx.2.1.2 #1, parallel-load flakes: subprocess_runner pipe-drain reproduced in this landing's just check and passed alone, so bob-cli-kl got a +1. The complete_themes flake is already tracked by bob-cli-g8, but it was not reproduced in this run, so g8 got no +1. (3) kx.2.1.4 #1 and kx.2.1.5 #2, the 44-45 lib and 2 CLI clean-base failures in albums/bank/record/capture/gcal: declined as already fixed on master (b7f74b58 and other later commits). This landing's just check at 1863b39b fails only 2 lib and 1 CLI tests, none of them in those areas. (4) kx.2.1.5 #1, lychee mac-capture/event-notes: duplicate of bob-cli-l7. The bad link is still at docs/gcal-notes.md:17, so l7 got a +1. (5) kx.2.1.7 #1, event-ack.md has no front matter, blocking docs-gen/docs-check: caused by active epic bob-cli-l5 (b6ed0e59, l5.1), recorded as a DISCOVERED ISSUE note on bob-cli-l5. (6) kx.2.1.7 #2, gcal sync_args alias test: duplicate of bob-cli-l2, reproduced, +1. (7) New in this landing: tests/cli/catalog.rs expects 97 entries but the catalog has 98 after 1863b39b (bob-cli-l5.3.1.2). Recorded as a DISCOVERED ISSUE note on active epic bob-cli-l5.3.1. Integration: the post-start commits are all gcal/albums/records/glossary work, and none consumes or conflicts with the archive feature, so no integration edits were needed. epic-symbols: none.

[2026-11-13T04:49:01Z · bob-cli-kx.2.1.land] LAND AUDIT: NOT READY TO CLOSE. Verified all seven phases' commits (677e7407, 92b52e4f, 4c2cb878, 8e78584d, 0b806ae8, 62ad26d7, 54fc8c61) against plan:202611/gmail_archive_core.md and confirmed these epic-caused defects in source. (a) Planning, apply, and recovery compute A/U from the current scan's saved_ids, never the close's frozen saved_ids, so a save between retries archives unfrozen mail, the journal rejects the event, apply returns Ok silently, and the receipt is left unowned. (b) Terminal-event None after a successful remote write is silently Ok across archive, recovery, and let-go. (c) First-use archives journal the receipt label with id None, and let-go/recovery match message label IDs against names, so let-go records release without removing the receipt. (d) An archive_label change after enablement is never re-baselined, so archives go unjournaled. (e) A [?] linker writes an open observation that parse_open_observation rejects, holding the thread forever. (f) The boundary revalidation compares a row with the same scan it came from: no lock and no re-read. (g) The live loop ignores each row's planned decision and creates the label even when only Kept rows exist. (h) Recovery is shadowed by the consent/unsaved checks. (i) Let-go reaches beyond the recorded IDs and is skipped while the gate is paused. (j) apply_live(...)? drops the filing/watch report, and archiving still runs after failed or incomplete filing. (k) Saved IDs are captured after watch hydration. (l) A dry-run before enablement shows nothing. (m) A supplied mismatched -c is ignored when confirmation is not required. (n) A -q live run leaks the digest, and kept/let_go rows are hollow. (o) Sync help still says 'Sync is read-only in Gmail', several docs are stale, and json-outputs.md lost text in 54fc8c61. (p) There are no real property tests. Remaining work is planned as the child epic sase_plan_gmail_archive_landing_repairs.md (phases ownership -> boundary -> integration -> surfaces) with parent_bead bob-cli-kx.2.1. just check at 1863b39b fails only 2 lib and 1 CLI tests: the gcal alias test (bob-cli-l2), the subprocess pipe-drain flake (bob-cli-kl), and the catalog 98-vs-97 count (bob-cli-l5.3.1). None is caused by this epic.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kx.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kx.2.1.land.md) | [bob-cli-kx.2.1](bob-cli-kx.2.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kx.2.1.1][1] | Need binding parent decisions and any earlier phase notes before implementing access | 1 |
| read-by | [agent:bob-cli-kx.2.1.2][2] | parent epic scope and decisions | 2 |
| read-by | [agent:bob-cli-kx.2.1.6][3] | Need epic scope and decisions for phase work | 1 |
| read-by | [agent:bob-cli-kx.2.1.7][4] | Need inherited epic decisions and phase context for reports and conformance audit | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.6/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kx.2.1.7/README.md

<!-- sase:referenced-by:end -->
