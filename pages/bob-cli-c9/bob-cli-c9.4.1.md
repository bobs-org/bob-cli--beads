# Bead: bob-cli-c9.4.1 — In-place overwrite of unannotated references

[Bead Pages](../README.md) / [bob-cli-c9.4](bob-cli-c9.4.md) / bob-cli-c9.4.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.md) · **Assignee:** `bob-cli-c9.4.1.land`
**Created:** 2026-10-25 22:34:43 EDT · **Closed:** 2026-10-26 07:25:24 EDT
**Plan:** [202610/unannotated\_reference\_overwrite.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/unannotated_reference_overwrite.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/unannotated_reference_overwrite.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/unannotated_reference_overwrite.md

<!-- sase:links:end -->

## Description

Complete bob-cli-c9.4 with task-preserving overwrite on every capture route, inert prose archives, durable crash recovery, and verified code and documentation gates.

## Notes

[2026-10-26T07:35:11Z · bob-cli-c9.4.1.land] DISCOVERED ISSUE: (land agent) Several commands pre-sync through vault_sync::run_cycle_with_existing_lock_report without first checking for a pending host-local overwrite intent: ref rename (rename/plan.rs:248), task move, randomize, vault_rewrite, migrate_tasks, migrate_zorg, and the background bob vault-sync cycle. After a crash during an overwrite, any of them can commit the half-applied files. Recovery (overwrite/recovery.rs ~281-289) then refuses with 'vault moved', and every later ref create or ref scan fails until the intent is removed by hand. This breaks the plan's rule: 'Recover any earlier intent before any pre-sync can commit half-applied files.' The epic caused this, so the remaining-work plan covers it.

[2026-10-26T07:35:15Z · bob-cli-c9.4.1.land] FOLLOW-UP TRIAGE (land agent): (1) The capture_related lib timing flakes proposed by bob-cli-c9.4.1.3 #1, bob-cli-c9.4.1.6 #1, and bob-cli-c9.4.1.8 #1 (synthetic_vault_query_is_under_250ms and synthetic_vault_draft_contract_is_under_250ms) are not caused by the epic. They are filed as new task bob-cli-ca (flake, small), linked related to bob-cli-bo. 8.8 cited bob-cli-bo as already tracking this, but bo is closed and fixed only the sibling CLI gate tests/cli/capture/related.rs::draft_related_stays_under_the_debug_perf_gate, so bo was not +1'd or reopened. (2) No other PROPOSED FOLLOW-UP entries exist on the children.

[2026-10-26T07:38:25Z · bob-cli-c9.4.1.land] LAND REVIEW (land agent): The tree is 94abe3d9, in sync with origin/master. All 8 phases are closed, and every commit since the epic started is the epic's own (6196cea7..94abe3d9), so there was nothing to integrate. just check passed (exit 0). epic-symbols is empty for bob-cli-c9.4.1 and for bob-cli-c9.4. Code review against both plans found real gaps, so the epic stays open. A remaining-work child epic (phases selection -> output -> safety) is proposed with parent_bead bob-cli-c9.4.1. Contract gaps: -N is ignored on URL and collection overwrite (recapture.rs finish_selection never sets family.selected); disabled ingest does not refuse; the annotated refusal text differs from the contract; the reread 'still ready with 0 highlights' hint is missing; the task alias is rewritten even when the title is unchanged (adds '(v1)' to a family root); the task: line shows the pre -s state; explicit open -s on an archived task fails late with verify_failed; -s legacy is refused late; Markdown and vault-note overwrites drop the Play link; narration is lost on late failure; -a with a different extension is written into the old .mp3; aliases, topics, and research are dropped; docs/highlights-clip.md still says filed refs refuse even with --force. Safety gaps: no executor failpoint tests (required by the plan); selection is not rechecked after the locked pre-sync; gitignored files inside a .textbundle are deleted and break rollback; the intent validator accepts '.'; other pre-syncs can commit a crashed overwrite; blanket #[allow(dead_code)] on mod overwrite.

[2026-10-26T11:25:24Z · bob-cli-c9.4.1.9.land] Nested landing complete: all 8 phases (.1-.8) plus repair epic .9 verified closed. Repaired findings from 94abe3d9 review (selection, refusals, alias, audio, docs, transaction, failpoints) plus tale gaps (file-stem identity, post-listen preservation, live selector coverage, actual-write rollback proof). Decisions unchanged: legacy_force=no, keep_created=yes. Drift: only 17f3881c root-true grouping (no overwrite integration) plus epic commits through 66f9d67f and repair working tree. Gates: fmt/clippy clean, docs-gen/check pass, lib 3547 pass with only bob-cli-ca timing flake (passes isolated), cli 2194 pass. Follow-ups stay tracked by bob-cli-ca; bob-cli-bo stays closed. Epic-symbols empty, symvision absent.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.1.land.md) | [bob-cli-c9.4.1](bob-cli-c9.4.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-c9.4.1.1][1] | Need parent epic DECISIONS and phase list for shared primitives work | 1 |
| read-by | [agent:bob-cli-c9.4.1.4][2] | Need the child epic decisions governing the transaction phase | 1 |
| read-by | [agent:bob-cli-c9.4.1.5][3] | Need DECISIONS and prior phase status for local overwrite | 1 |
| read-by | [agent:bob-cli-c9.4.1.6][4] | parent epic scope for web phase | 1 |
| read-by | [agent:bob-cli-c9.4.1.8][5] | Need the parent epic DECISIONS and phase graph | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.6/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.8/README.md

<!-- sase:referenced-by:end -->
