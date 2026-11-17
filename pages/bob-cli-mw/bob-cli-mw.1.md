# Bead: bob-cli-mw.1 — bob-cli reads the Daily Headline and serves it

[Bead Pages](../README.md) / [bob-cli-mw](README.md) / bob-cli-mw.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1dq](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1dq.md) · **Assignee:** `bob-cli-mw.1` · **Size:** medium
**Created:** 2026-11-17 17:23:40 EST · **Closed:** 2026-11-17 18:03:07 EST
**Plan:** [202611/daily\_headline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/daily_headline.md)

## Description

cli: add the shared daily-headline parser, put `headline` on week-report day columns and children, day brief parts, and `capture-pomodoros --tasks`, update terminal output, docs, and tests.

## Notes

[2026-11-17T23:02:54Z · bob-cli-mw.1] PROPOSED FOLLOW-UP: docs/reference/json-outputs.md is 6112 words vs the 6000 reference cap — identical on clean HEAD 0e83df4c; this phase kept the count at 6112 (already tracked on bob-cli-ms notes #2/#7).

[2026-11-17T23:03:00Z · bob-cli-mw.1] PROPOSED FOLLOW-UP: three lib tests fail identically on clean HEAD 0e83df4c because bob records tidy is missing from catalog/completion/canonical paths — public_leaves_are_entries_or_excluded, every_value_arg_has_a_decision (records tidy:type), every_native_command_is_on_exactly_one_canonical_path 92 vs 91; causal epic bob-cli-ms (records-tidy cfc3177c).

[2026-11-17T23:03:07Z · bob-cli-mw.1] Shared daily-headline parser plus week-report day columns/children headline, brief day parts, and capture-pomodoros --tasks headline (schema 1, omit without --tasks, null when empty). Verified: just lint, cargo fmt --all -- --check, 8 parser tests, 21 pomodoros_agenda, week_report_and_brief_carry_day_headlines, docs_reference, 69 periods lib tests. HEAD-identical leftovers recorded as PROPOSED FOLLOW-UP (json-outputs 6112/6000 on bob-cli-ms; records tidy catalog/completion/canonical-path lib tests). epic-symbols empty. glossary:daily-headline added; decisions:daily-headline-is-bryans-line untouched.

## Dependencies

- **Blocks:** [bob-cli-mw.2](bob-cli-mw.2.md) ◐ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-mw.3](bob-cli-mw.3.md) ◐ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-mw.4](bob-cli-mw.4.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mw.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mw.1/README.md) | [bob-cli-mw.1](bob-cli-mw.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2a58d06`](https://github.com/bobs-org/bob-cli/commit/2a58d06701cc74324c055970e69eaa9de8757dba) | feat(periods): serve Daily Headline on week days and capture --tasks | [bob-cli-mw.1](bob-cli-mw.1.md) | 2026-11-17 18:04:26 EST |
