# Bead: bob-cli-3v.3 — Exact explicit-keep counting

[Bead Pages](../README.md) / [bob-cli-3v](README.md) / bob-cli-3v.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.4o](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4o.md) · **Assignee:** `bob-cli-3v.3` · **Size:** medium
**Created:** 2026-10-03 10:36:59 EDT · **Closed:** 2026-10-03 11:23:40 EDT
**Plan:** [202610/rotten\_keep\_streak.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/rotten_keep_streak.md)

## Description

nav-counting: wire single, counted, and Task Link refreshes through exact pre-write matching, atomic writes, accurate notices, and cache-lag regressions.

## Notes

[2026-10-03T15:23:40Z · bob-cli-3v.3] nav-counting done: strict exact-eligibility predicate (path+line+raw+ready+rotten/returned, exactly one row) drives per-target counted decisions through keepLine in single, counted, and Task Link flows; stale/ambiguous/lane/NEW shapes stamp uncounted and preserve; v5-missing/throwing keepLine fails without writing, pre-v5 falls back to old stamper; duplicate Task Links dedupe; Fresh notice gains kept Nx from actual increments, never promises next review asks; nav manifest 1.68.0; trial-neutral milestone noted in docs/freshness.md. Verified: new 28-test test-navigation-keep-counting.cjs (helpers + real handlers: stale source, multi-note preimage refusal, rollback, CRLF, one transaction, dual-route key) registered in npm test; full npm test 1513 pass/0 fail; npm run validate 6/6; neighbor suites (freshness/stamps/cycler/block-id-prompt/roll-decay) 475 pass. No epic symbols.

## Dependencies

- **Depends on:** [bob-cli-3v.2](bob-cli-3v.2.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3v.4](bob-cli-3v.4.md) ✓ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-3v.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-3v.3/README.md) | [bob-cli-3v.3](bob-cli-3v.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d6b63e8`](https://github.com/bobs-org/bob-cli/commit/d6b63e864c3b29b15f89a98cd9859184bb53ced5) | docs(freshness): record keep-counting as trial-neutral first milestone | [bob-cli-3v.3](bob-cli-3v.3.md) | 2026-10-03 11:25:19 EDT |
| bob-plugins | [`bob-plugins@9a86df4`](https://github.com/bobs-org/bob-plugins/commit/9a86df48e4537b4b3ac80682d8377f49f38573c1) | feat(nav-hotkeys): count eligible fresh stamps through keepLine with exact pre-write match | [bob-cli-3v.3](bob-cli-3v.3.md) | 2026-10-03 11:25:51 EDT |
