# Bead: bob-cli-n5.3 — Keep record field punctuation literal during rewrite

[Bead Pages](../README.md) / [bob-cli-n5](README.md) / bob-cli-n5.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-my.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-my.land.md) · **Assignee:** `bob-cli-n5.3` · **Size:** medium
**Created:** 2026-11-17 22:21:55 EST · **Closed:** 2026-11-18 00:44:26 EST
**Plan:** [202611/backlog\_triage\_t3.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t3.md)

## Description

record-literals: Resolve bob-cli-ja at the shared rewrite/completion boundary with record-value parity tests.

## Notes

[2026-11-18T05:44:26Z · bob-cli-n5.3] Fixed bob-cli-ja: spaced ./; inside first-level record key:: values stay literal (shared rewrite/completion parity). Verified: current-binary repro before (rewrote to */@) vs after (literal); new rewrite test (create/explicit-stem/update, multi-field, earlier-field cursor, non-ASCII, ordinary-task controls, item-start dot) and capture-complete record_value parity test pass; rewrite/record/capture-complete suites green; dry-run and real throwaway-vault captures preserve literal field bytes (sushi ; / sushi .); full check via sase tool run check exit 0. No epic-symbols; task bead bob-cli-ja left for lander.

## Dependencies

- **Depends on:** [bob-cli-n5.2](bob-cli-n5.2.md) ✓ · ⧖ 2026-11-17
- **Blocks:** [bob-cli-n5.4](bob-cli-n5.4.md) ◐ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-n5.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-n5.3/README.md) | [bob-cli-n5.3](bob-cli-n5.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`612d134`](https://github.com/bobs-org/bob-cli/commit/612d134278173c650dadfe5f63b14e9690c78b6e) | fix(capture): keep record field punctuation literal during rewrite | [bob-cli-n5.3](bob-cli-n5.3.md) | 2026-11-18 00:46:18 EST |
