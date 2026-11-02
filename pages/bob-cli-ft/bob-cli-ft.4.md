# Bead: bob-cli-ft.4 — Fold the priority bars on digit rows and the project tag on ^ rows

[Bead Pages](../README.md) / [bob-cli-ft](README.md) / bob-cli-ft.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.16w](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.16w.md) · **Assignee:** `bob-cli-ft.4` · **Size:** small
**Created:** 2026-11-02 06:28:11 EST · **Closed:** 2026-11-02 12:07:21 EST
**Plan:** [202611/blocked\_reason\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/blocked_reason_marks.md)

## Description

redundancy_folds: where the checkbox digit already says the priority, fold the signal bars. Where the ^ mark already says the project is blocked, fold the #prj_is_blocked pill. Applies in Live Preview and reading view, keeps cursor reveal, and is gated on both toggles.

## Notes

[2026-11-02T17:07:05Z · bob-cli-ft.4] PROPOSED FOLLOW-UP: Pre-existing npm test failures on clean bob-plugins master (same 5 as this phase): freshness-namespace due-key reload (bob-cli-et), keep-inbox forced-check 12:30 vs 16:30 (bob-cli-f7), note-ready startup storm + relationIndex layout-ready (bob-cli-eh), schedule-work-log Pending future-date when today is 2026-11-02

[2026-11-02T17:07:21Z · bob-cli-ft.4] redundancy_folds in bob-ledger-tools 1.91.0: digit p1–p4 rows fold priority bars (data-folded, both gates); prj rows fold #prj_is_blocked (LP replace widget, reading data-bob-block-folded clip hide); cursor/click reveal; BM8/BM9 keep bars; BM19 keeps pill; Tasks rows skipped. Verified npm build, PM18/PM19 + BM fold unit/editor/reading/contrast tests, docs:gen, docs:check, vault sync. Full npm test 5 fails reproduce on clean master (bob-cli-et, bob-cli-f7, bob-cli-eh, date-sensitive schedule-work-log). No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-ft.3](bob-cli-ft.3.md) ✓ · ⧖ 2026-11-02
- **Blocks:** [bob-cli-ft.5](bob-cli-ft.5.md) ✓ · ⧖ 2026-11-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ft.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.4/README.md) | [bob-cli-ft.4](bob-cli-ft.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b64a433`](https://github.com/bobs-org/bob-plugins/commit/b64a4332a93f2f3fb20a0b13d2cf9021763fdb0e) | feat(ledger-tools): fold digit bars and project-blocked pills | [bob-cli-ft.4](bob-cli-ft.4.md) | 2026-11-02 12:16:04 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ft.4][1] | Need the phase scope and design file | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ft.4/README.md

<!-- sase:referenced-by:end -->
