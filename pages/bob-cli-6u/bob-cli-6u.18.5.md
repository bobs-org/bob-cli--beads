# Bead: bob-cli-6u.18.5 — Task-status-cycler and block-id-prompt project-blocking fixes

[Bead Pages](../README.md) / [bob-cli-6u.18](bob-cli-6u.18.md) / bob-cli-6u.18.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-6u.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-6u.land.md) · **Assignee:** `bob-cli-6u.18.5` · **Size:** small
**Created:** 2026-10-12 18:07:06 EDT · **Closed:** 2026-10-12 18:18:07 EDT
**Plan:** [202610/prj\_line\_blocking\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_line_blocking_landing_fixes.md)

## Description

cycler-blockid: strip the tag from every resident when the project recovers, recover without [unblocked::] when ledger freshness v12 is missing, pass the out-of-scope skip flags, collapse redundant inline-date checks, block-id-prompt refusal scope and order, README rows.

## Notes

[2026-10-12T22:17:52Z · bob-cli-6u.18.5] Verified and fixed the cycler and block-id-prompt phase scope: project recovery strips #prj_is_blocked from every open resident, including residents that stay [?] for their own reasons; Ready recoveries proceed without ledger freshness v12 and warn when it is absent; daily-note and Today skip flags reach markUnblockedLine. Removed the redundant inline project-date checks. Block ID Prompt now reports dependency reasons before schedule reasons and refuses a future-dated ^prj link only when its date is the sole reason; direct Task Links raise Ready ^prj to Next. Updated plugin README rows and manifest versions (task-status-cycler 1.32.0, block-id-prompt 1.28.0), plus docs/task-dependencies.md §5 and §13.4 for the direct-link rule. The recurring-helper audit finding was already covered by bob-ledger-tools freshnessMarkUnblockedLine/freshnessHasRepeatField; no cycler lineIsRecurring helper exists in this checkout. Build passed; focused suites passed 128/128; validate passed 6/6. Full npm test: 2512 passed, with only the allowed tracked failures: four bob-cli-6v unblocked-glyph cases, bob-cli-6w Keep counts once, and bob-cli-3w stage-ranker timing. Deployed both plugins to this host; bob plugins list -n against the opened repo reports 6 synced, 0 drift.

[2026-10-12T22:17:57Z · bob-cli-6u.18.5] PROPOSED FOLLOW-UP: Revisit the known pre-epic full-suite failures tracked by bob-cli-6v (four unblocked-glyph cases), bob-cli-6w (Keep counts once), and bob-cli-3w (stage-ranker timing flake); npm test reports only these six failures after this phase.

[2026-10-12T22:18:07Z · bob-cli-6u.18.5] Verified project resident tag cleanup and recovery skip flags, block-id refusal and direct-^prj-link behavior; focused tests 128/128 and validate 6/6 pass. Full suite has only the six known bob-cli-6v/6w/3w failures; both plugins are deployed and synced on this host.

## Dependencies

- **Blocks:** [bob-cli-6u.18.6](bob-cli-6u.18.6.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6u.18.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6u.18.5/README.md) | [bob-cli-6u.18.5](bob-cli-6u.18.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`414b802`](https://github.com/bobs-org/bob-cli/commit/414b802b915c9ec7e89f6cfbdded0cced5a84422) | docs(task-dependencies): clarify direct project task links | [bob-cli-6u.18.5](bob-cli-6u.18.5.md) | 2026-10-12 18:18:56 EDT |
| bob-plugins | [`bob-plugins@f1d5a4e`](https://github.com/bobs-org/bob-plugins/commit/f1d5a4e05ff9cbd64cbe66b8651efeb8c3b5ef9e) | fix(project-blocking): repair cycler and block id prompt | [bob-cli-6u.18.5](bob-cli-6u.18.5.md) | 2026-10-12 18:20:17 EDT |
