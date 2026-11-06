# Bead: bob-cli-ho.2 — Relative period ids (last-week, last-quarter, last-year) in bob periods

[Bead Pages](../README.md) / [bob-cli-ho](README.md) / bob-cli-ho.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.193](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.193.md) · **Assignee:** `bob-cli-ho.2` · **Size:** small
**Created:** 2026-11-05 18:44:51 EST · **Closed:** 2026-11-05 19:11:43 EST
**Plan:** [202611/gtd\_checklist\_stages.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gtd_checklist_stages.md)

## Description

period_ids: accept last-week, last-quarter, and last-year wherever bob periods show, brief, and draft take a PERIOD, resolved against today, so the launch rows can carry one paste-ready agent prompt forever.

## Notes

[2026-11-06T00:11:22Z · bob-cli-ho.2] PROPOSED FOLLOW-UP: docs-check fails on 4 undocumented BOB_GMAIL_* env names from the gmail phase; fails identically on the clean base tree

[2026-11-06T00:11:27Z · bob-cli-ho.2] PROPOSED FOLLOW-UP: lib tests completion::kinds every_table_entry_matches_the_tree and catalog public_leaves_are_entries_or_excluded fail on clipboard:count duplicate entries; fail identically on the clean base tree

[2026-11-06T00:11:31Z · bob-cli-ho.2] PROPOSED FOLLOW-UP: ref_library extra_pass_and_additive_id_resolution test flaked once under full-suite load but passes in isolation on this tree; watch for a flaky-test pattern

[2026-11-06T00:11:43Z · bob-cli-ho.2] period_ids done: PeriodId::resolve maps last-week/quarter/year (case- and _-insensitive) via prev() in show/brief/draft; human show prints canonical id + note path; PERIOD help + docs/periods.md + regenerated CLI reference updated. Verified: new calendar unit test (PI1-PI6) and CLI integration test pass; manual BOB_NOW spot checks match PI1-PI4 exactly; cargo fmt + clippy clean; full lib suite green except 2 clipboard failures + docs-check gmail lints that fail identically on base (recorded as follow-ups) and one ref_library timing flake that passes in isolation. No epic symbols. Work left uncommitted in the workspace for review.

## Dependencies

- **Blocks:** [bob-cli-ho.6](bob-cli-ho.6.md) ◐ · ⧖ 2026-11-05

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ho.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ho.2/README.md) | [bob-cli-ho.2](bob-cli-ho.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8feca27`](https://github.com/bobs-org/bob-cli/commit/8feca277a8ada6108bef340c4cddaf3e62220b47) | feat(periods): support last-week, last-quarter, and last-year relative period ids | [bob-cli-ho.2](bob-cli-ho.2.md) | 2026-11-05 19:12:50 EST |
