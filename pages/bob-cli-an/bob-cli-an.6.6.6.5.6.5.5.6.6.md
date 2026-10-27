# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6 — Backlog batch 10: port-dedupe ports, capture help, ref doctor, Mermaid pdftotext, and StartPending recheck

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6](bob-cli-an.6.6.6.5.6.5.5.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.land`
**Created:** 2026-10-25 10:04:06 EDT · **Closed:** 2026-10-25 11:02:20 EDT
**Plan:** [202610/backlog\_batch10\_port\_help\_doctor\_mermaid\_startpending.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch10_port_help_doctor_mermaid_startpending.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/backlog_batch10_port_help_doctor_mermaid_startpending.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch10_port_help_doctor_mermaid_startpending.md

<!-- sase:links:end -->

## Description

Close five backlog tasks by keeping explicit non-default ports in URL identity, correcting capture help, deciding ref doctor scope, making Mermaid PDF tests pass without pdftotext, and rechecking the StartPending flake for closeable non-reproduction.

## Notes

[2026-10-25T15:02:20Z · bob-cli-an.6.6.6.5.6.5.5.6.6.land] LANDER VERIFY (bob-cli-an.6.6.6.5.6.5.5.6.6.land). All 5 phases were reviewed against their notes and source; no phase recorded a PROPOSED FOLLOW-UP. Phase .1, 7e8ffedd: dedupe_key_for and display_url keep url.port(), with tests; closed c3. Phase .2, 633bc3f6: TEXT help corrected in 5 commands and CLI docs regenerated; closed c4. Phase .4, 3eebe47f: raw-PDF fallback removed and pdftotext gated; closed 9i. Phase .5: 4k was already closed done by the phase with a 4-pass macOS CI evidence chain, re-confirmed via gh (461f46c run 40195734261 success, still the newest master run). Phase .3, 89945148: the ref doctor reference-ids row, decided IMPLEMENT. EPIC-CAUSED DEFECT FIXED: the new repair test needed pandoc, and CI run 40202985199 on 89945148 failed on ubuntu and macOS. Fixed in ba523746 with a marker-PDF plus ref sync setup; doctor_library is 15/15 with and without pandoc. INTEGRATION, also in ba523746: duplicate-id folding switched to ASCII to match the docs and resolve.rs; the CLI Mermaid render-only tests are no longer pdftotext-gated (lib 19/19 and CLI 12/12 with pdftotext hidden); the redundant pdftotext check was dropped; docs/capture.md saved_templates_unknown_flag wording was fixed. Gates: just check 18 suites, 5657 passed, 0 failed; just docs-check passed. Release run 40202947018 failed only on a non-fast-forward push race (master advanced mid-run); the next scheduled train retries. b8 stays OPEN: the code half is done, but the live-vault repair is forbidden by the working rules and goes to batch 11 behind a Bryan-approved /sase_gate (see the b8 note). DRIFT: fd0fc2e5 (docs refresh) reported 3 source follow-ups. The port and capture-help ones are fixed by this epic. The Day strip openStatsForDay newLeaf defect was confirmed in bob-plugins 3bac436 and filed via /sase_new_task as bob-cli-c6 (bug, small), with no duplicate and related, not caused, to active epic bob-cli-c5. 0cf45b8c (homes rollup retirement) does not overlap this epic. epic-symbols: none. No symvision recipe exists.

[2026-10-25T15:26:25Z · bob-cli-an.6.6.6.5.6.5.5.6.6.land] LANDER ADDENDUM: while preparing the batch-11 b8 phase, the lander found a second epic-caused defect in 89945148. id_stem_mismatch flagged the decision-allowed <stem>_N duplicate-avoiding suffix that bob ref rename itself allocates (tests/cli/ref_library/rename.rs colliding_reference_ids_receive_the_first_available_suffix), so the advised same-stem repair could never clear it. Fixed in 41cd3748: the suffix is accepted while another note records <stem>, with a new doctor_library test and a docs/highlights-ref-sync.md update. Verified with just check (5658 passed, 0 failed) and just docs-check. A read-only bob ref list on the live vault now shows 1 duplicate id (BryanBugyi_CV_extended x2) and 2 mismatches (BryanBugyi_CV_extended_v2, obsidian_sync_footprint_audit_bob-cli-1l). ref/papers/harness_engineering.md (id harness_engineering_2 next to ref/blogs/harness_engineering.md) is decision-compliant.

[2026-10-25T15:33:34Z · bob-cli-an.6.6.6.5.6.5.5.6.6.land] CONTINUATION: the lander proposes batch-11 epic scratch sase_plan_backlog_batch11_ref_repair_taskcard_popout_gkeep_again.md (parent_bead bob-cli-an.6.6.6.5.6.5.5.6.6). It assigns b8 (live ref-id repair, only through a Bryan-approved /sase_gate turn), 4e (Task Card onClose cleanup), 9q (popout mark gates), 2m (gkeep stdin EPIPE), and bn (start-name again order). The three bob-plugins phases are serialized for safe bob plugins sync deploys. Fresh unresolved count: 123 (119 ready + 4 snoozed 3o/6q/aa/ah), including the new c6. Deferred: 8r (root-level athena hardening), c6 (waits for active epic bob-cli-c5 on openStatsForDay), 5m/5n (sase-tool defects), v (resized scope noted on the bead), large flakes 5o/b9/67 (no root cause). CI: ba523746 run 40204868955 and 41cd3748 run 40206835393 passed. Ownership passes to the batch-11 lander on propose.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ba52374`](https://github.com/bobs-org/bob-cli/commit/ba523746df6fd21308193bbc14f7b59a76ba9529) | fix(ref-doctor): fold reference ids ASCII-only and drop pandoc from the repair test | [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) | 2026-10-25 11:00:19 EDT |
| bob-cli--plans | [`bob-cli--plans@2d0fa85`](https://github.com/bobs-org/bob-cli--plans/commit/2d0fa854ce4865da83ebf775b6f936b28cd07e43) | chore(plans): mark backlog batch 10 plan done | [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) | 2026-10-25 11:02:33 EDT |
| bob-cli | [`41cd374`](https://github.com/bobs-org/bob-cli/commit/41cd37487779a54187675445531557d3ab26879d) | fix(ref-doctor): accept the duplicate-avoiding \_N id suffix | [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) | 2026-10-25 11:25:05 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.1][1] | epic decisions and scope | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.3][2] | Need epic DECISIONS | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land][3] | Landing: check plan-ancestor closure status | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.land][4] | Need the parent link and parent epic status | 2 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.land][5] | Need the epic scope, children, and linked plan file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.land.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land.md

<!-- sase:referenced-by:end -->
