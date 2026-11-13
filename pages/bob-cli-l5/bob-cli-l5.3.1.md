# Bead: bob-cli-l5.3.1 — Complete the Google Calendar ack command

[Bead Pages](../README.md) / [bob-cli-l5.3](bob-cli-l5.3.md) / bob-cli-l5.3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-l5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-l5.3.md) · **Assignee:** `bob-cli-l5.3.1.land`
**Created:** 2026-11-12 20:43:26 EST · **Closed:** 2026-11-13 03:31:25 EST
**Plan:** [202611/gcal\_ack\_cli.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_ack_cli.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/gcal_ack_cli.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gcal_ack_cli.md

<!-- sase:links:end -->

## Description

Complete bob-cli-l5.3 with a tested one-key external-event review queue, shared private-note editing, noninteractive ack management, and stale/doctor diagnostics, then close only that containing phase through this child's land agent.

## Notes

[2026-11-13T04:45:14Z · bob-cli-kx.2.1.land] DISCOVERED ISSUE: (from bob-cli-kx.2.1.land) Commit 1863b39b (bob-cli-l5.3.1.2, 'add external event ack CLI') added a catalog entry and bumped src/native/catalog/tests.rs to 98, but left tests/cli/catalog.rs:42 at 97. On master 1863b39b, cargo test --test cli catalog::protocol_1_parses_with_schema_version_one fails deterministically (left 98, right 97), both alone and in the full just check. Fix: update the CLI catalog count (and any entry assertions for gcal-ack) alongside the lib test. Phase bob-cli-l5.3.1.4 (CLI verification) is the natural owner.

[2026-11-13T07:22:22Z · bob-cli-l5.3.1.land] LANDING FOLLOW-UP TRIAGE: Reviewed every child note and all seven PROPOSED FOLLOW-UP entries. (1) .1 #1, .2 #2 gcal portion, .3 #1, .4 #2: duplicate sync day-alias failure; recorded +1 on bob-cli-l2 with exact clean-base SHAs and proposing phases. (2) .2 #1, .3 #2, .4 #1: missing glossary:event-ack front matter is caused by parent l5.1 and already assigned to l5.4; corroborated DISCOVERED ISSUE on bob-cli-l5, no new task or child memory edit. (3) .2 #2 Gmail completion portion: declined as fixed by intervening commit 54fc8c61, which adds gmail/sync confirm -> FreeText in completion/kinds.rs; current source includes it. (4) Incidental pipe-drain flakes in .3 #3 and .4 #3 match bob-cli-kl; recorded +1 relaying their unchanged-tree failure/pass evidence, explicitly not claiming a new lander run. Searched task reports across statuses, swept the last week, inspected active epics and relevant owners. No genuinely new unrelated task remained. Epic note #1 catalog mismatch is addressed by 6bcc97ae (98 entries and gcal-ack assertions in tests/cli/catalog.rs). Integration audit: 62ad26d7 and 54fc8c61 are the only unrelated commits since creation; their Gmail archive changes have no ack consumer or conflicting writer. The shared completion table includes both feature sets. Refreshed origin/master remains 6bcc97ae. No --epic-symbol entries for this epic or parent phase l5.3.

[2026-11-13T07:25:24Z · bob-cli-l5.3.1.land] LANDING AUDIT AT 6bcc97ae: The epic is not ready to close. Reviewed every phase note, both approved plans and accepted research, all four epic commits, current source/tests, and intervening Gmail changes. Accepted tag/no-decision-record/no-child-memory-edit decisions were honored; shared selector/editor/preview, explicit receipts, stale predicate, list/sync/doctor integration and catalog/completion are present. Remaining epic defects found in source: (1) ack::removed_by_user filters out gone state, so persisted line_removed tombstones re-enter the queue; (2) validate_args treats -D plus a one-shot selector as a non-TTY interactive walk; (3) RawGuard disables OPOST while session eprintln emits LF only, and render_card prints an unwrapped preview row/discards Styler; (4) run_session drops queue.waiting and refold ignores skipped siblings covered by a later series answer; (5) editor/adopt/save_session_note/was_unacked default required journal read errors to empty books; (6) doctor recommends clearing missing/series-master receipt keys, but run_selected requires a current occurrence and rejects those targets. A source-matched PTY termios probe confirmed LF without CR; no fresh compiled CLI or just check run is claimed in this audit. Authored and validated a medium tale sase_plan_gcal_ack_landing_repairs.md for these bounded repairs, regression verification with just check, and mandatory same-turn closure of this epic plus parent phase bob-cli-l5.3. Neither bead is closed or forced; plan status stays unfinished until the repair coder completes that closeout.

[2026-11-13T08:31:25Z · bob-cli-l5.3.1.land] Completed the approved remaining ack repairs: persisted line_removed suppression with revival semantics across actionable and waiting queues; selector-aware -D validation; terminal wrapping, styling, PTY newline and termios behavior; retained waiting/skipped refolding with pre-write journal error propagation; and exact-key doctor clear for missing or canceled receipts. Regression coverage includes persisted/live/revived removals, selectors and previews, waiting/series counters, journal failures, doctor clear boundaries, and real-PTY width/color/newline/restoration. Verification: focused gcal_ack and gcal_ack_tty passed 39 and 7 tests; neighboring gcal_auth, gcal_cli, gcal_list, gcal_note_cli, gcal_notes, and gcal_sync suites passed; 279/280 gcal library tests passed. The sole library failure is the existing sync_args_read_last_n_days_aliases_and_default_to_none expectation (actual [tomorrow], expected [today, tomorrow]), recorded for bob-cli-l2 and reproduced on clean base 1863b39b; it was not changed here. Canonical just check formatting and clippy passed and workspace tests reached the same known failure, with all other test binaries passing. Post-start origin/master has no drift from 6bcc97ae; the Gmail archive changes remain unrelated and catalog/completion work is intact. No epic-symbol entries remain; just symvision is unavailable in this Justfile; prior follow-up outcomes are preserved.

[2026-11-13T08:34:32Z · bob-cli-l5.3.1.land] Verification clarification: the green just check run required a temporary expectation-only edit to the existing sync_args_read_last_n_days_aliases_and_default_to_none unit assertion. That edit was reverted per this plan because the failure is assigned to bob-cli-l2. On the final tree, cargo test --lib native::gcal:: -- --test-threads=1 reports 279 passed and only that known sync argument failure (actual [tomorrow], expected [today, tomorrow]), already reproduced on clean base 1863b39b. Ack/TTY and neighboring gcal suites pass; formatting and clippy pass. The full gate should be read with this one known final-tree limitation.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-l5.3.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-l5.3.1.land.md) | [bob-cli-l5.3.1](bob-cli-l5.3.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`cb10892`](https://github.com/bobs-org/bob-cli/commit/cb10892f8fc200272a91db538bb51940981e8961) | fix(gcal): repair ack queue and terminal edge cases | [bob-cli-l5.3.1](bob-cli-l5.3.1.md) | 2026-11-13 03:37:03 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-l5.3.1.1][1] | Need parent epic scope and DECISIONS | 1 |
| read-by | [agent:bob-cli-l5.3.1.3][2] | need epic decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.3.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-l5.3.1.3/README.md

<!-- sase:referenced-by:end -->
