# Bead: bob-cli-ii.3.1 — Gmail sync discovery, enrollment, and routed filing

[Bead Pages](../README.md) / [bob-cli-ii.3](bob-cli-ii.3.md) / bob-cli-ii.3.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ii.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.3.md) · **Assignee:** `bob-cli-ii.3.1.land`
**Created:** 2026-11-07 18:12:56 EST
**Plan:** [202611/gmail\_sync\_filing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_filing.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gmail_sync_filing.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_sync_filing.md

<!-- sase:links:end -->

## Description

Complete bob-cli-ii.3 with idempotent label-routed task filing, local watch membership, adoption, bounded retries, one scoped transaction, clear reports, and a behavior-identical hidden pull alias.

## Notes

[2026-11-08T03:19:38Z · bob-cli-ii.3.1.land] LANDING REVIEW (HEAD 5df6b9d5): Read the epic and all four phase beads and every note, audited both linked plans, and reviewed commits 343b4d8f, 39122cb2, d5c61ee5, 5df6b9d5 against the source. The shared enrollment/scan, route resolver, prepared save/capture writer, hidden pull alias, catalog/completion, and approved Inbox File glossary correction are present. Decisions remain cron_enabled=no, gmail_watch_record=no, reply_hold_record=yes owned by outer watch, inbox_glossary=yes. No unrelated commits landed after 343b4d8f; fetched origin/master equals HEAD. Also reviewed sibling turn commit 47341462 (after epic creation, before first child commit): sync retains its turn metadata and canonical mail.base upgrade through shared save planning. No epic-symbol entries exist; this justfile currently has no symvision recipe. Remaining epic-caused defects from source review: (1) select_candidates filters only EnrollmentFold before applying -l, so local adoptions consume filing slots and are needlessly fetched; (2) discover_ids bypasses pacing/retries, and pace_before_request plus zero SharedBudget can defer healthy later candidates at -r 0; exhausted transient metadata failures disappear into deferred/warnings so command can report ok=true; (3) report counts every problem result as pulled/watching, including failed fetches with no durable task, uses the pre-apply watch scan, and drops filing-failure details and human route explanations; (4) commit-failure replay adopts and commits only mail/task paths, losing auxiliary/image recovery and deferred save/origin events; (5) the phone guide still forwards mail instead of documenting bob plus one #/note on the original conversation, and temporary broad dead-code allowances and planned acceptance cases remain. These require a bounded repair tale before landing. Findings are static review evidence; this turn has not claimed a new test pass.

[2026-11-08T03:19:42Z · bob-cli-ii.3.1.land] FOLLOW-UP TRIAGE COMPLETE: All four child notes reviewed; none contains a PROPOSED FOLLOW-UP entry. No independent unrelated defect was established, so no /sase_new_task action was warranted and no proposal was declined. The phase .3 note reports one guard-contention test failure followed by an isolated pass and a full rerun pass; treat deterministic coverage of the new sync guard as part of the epic repair verification, not as an unrelated task. All landing findings are caused by this epic and stay in its remaining-work tale. Its coder must finish this epic and parent phase bob-cli-ii.3 normally; the outer bob-cli-ii remains for its waiting land agent.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ii.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ii.3.1.land.md) | [bob-cli-ii.3.1](bob-cli-ii.3.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f904135`](https://github.com/bobs-org/bob-cli/commit/f9041354c191eb8bb781abc000821675f9bb7cdb) | fix(gmail): repair sync landing gaps for filing, coordination, reports, and recovery | [bob-cli-ii.3.1](bob-cli-ii.3.1.md) | 2026-11-07 23:18:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ii.3.1.1][1] | Need epic decisions and notes | 1 |
| read-by | [agent:bob-cli-ii.3.1.3][2] | Need parent epic decisions and phase constraints before implementation | 1 |
| read-by | [agent:bob-cli-ii.3.1.4][3] | Need DECISIONS, design files, notes, and parent epic contract | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.3.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ii.3.1.4/README.md

<!-- sase:referenced-by:end -->
