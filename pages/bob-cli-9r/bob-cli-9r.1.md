# Bead: bob-cli-9r.1 — Today marks display contract in bob-cli docs

[Bead Pages](../README.md) / [bob-cli-9r](README.md) / bob-cli-9r.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.11r](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.11r.md) · **Assignee:** `bob-cli-9r.1` · **Size:** small
**Created:** 2026-10-19 09:47:17 EDT · **Closed:** 2026-10-19 09:54:04 EDT
**Plan:** [202610/today\_marks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/today_marks.md)

## Description

contract: write the authoritative docs/today-marks.md display contract with conformance vectors TM1–TM23, link it from docs/README.md and docs/plan.md §Today, and (only if the memory decision is yes) add the decisions-web record.

## Notes

[2026-10-19T13:53:42Z · bob-cli-9r.1] PROPOSED FOLLOW-UP: Record the Today mark design as decisions:today-mark-shows-ledger-today; this phase DECISIONS selected memory_today_mark_record = no, so the authorized docs-only work leaves memory unchanged.

[2026-10-19T13:54:04Z · bob-cli-9r.1] Added docs/today-marks.md with the Today display contract and TM1–TM23; linked it from docs/README.md and docs/plan.md §Today. Verified all 23 vectors exactly match the plan, local Markdown links resolve, git diff --check is clean, recorded the memory decision follow-up, and epic-symbol check found none.

## Dependencies

- **Blocks:** [bob-cli-9r.4](bob-cli-9r.4.md) ◐ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9r.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9r.1/README.md) | [bob-cli-9r.1](bob-cli-9r.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1b158e6`](https://github.com/bobs-org/bob-cli/commit/1b158e662364485fbc591aa8def3cceeb8951ea7) | docs(today-marks): document the display contract | [bob-cli-9r.1](bob-cli-9r.1.md) | 2026-10-19 09:54:40 EDT |
