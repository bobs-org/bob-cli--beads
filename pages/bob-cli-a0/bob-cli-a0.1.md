# Bead: bob-cli-a0.1 — Licenses and stale public claims

[Bead Pages](../README.md) / [bob-cli-a0](README.md) / bob-cli-a0.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.md) · **Assignee:** `bob-cli-a0.1` · **Size:** small
**Created:** 2026-10-19 18:55:41 EDT · **Closed:** 2026-10-19 19:01:11 EDT
**Plan:** [202610/bob\_public\_docs\_site.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_public_docs_site.md)

## Description

prereqs: add LICENSE files to bob-cli and bob-mac-capture and correct the bob-plugins README's stale public claims.

## Notes

[2026-10-19T23:00:57Z · bob-cli-a0.1] PROPOSED FOLLOW-UP: bob-plugins npm test has 6 pre-existing failures on the clean base tree (test-ledger-tools-unblocked-glyph.cjs x4, test-navigation-decision-card-handlers.cjs keeps, test-navigation-hotkeys-forward-promotion.cjs x1); verified identical with changes stashed

[2026-10-19T23:01:11Z · bob-cli-a0.1] MIT LICENSE added to bob-cli and bob-mac-capture (holder Copyright (c) 2026, Bryan M Bugyi, matching bob-plugins); license=MIT in bob-cli Cargo.toml plus /LICENSE* in package include; cargo package --list --allow-dirty exit 0 with LICENSE listed. bob-plugins README corrected: seven plugins, bob-articles row (0.2.1), nav-hotkeys 2.46.1, bobs-org/bob-cli link, seven-plugin deploy comment, public monorepo scope, bob-articles in layout and styles.css lists; npm run validate 7/7 valid; bob plugins sync exit 0. npm test: 6 failures reproduce identically on clean tree (recorded as PROPOSED FOLLOW-UP); 7th was flaky perf timing, passes in isolation.

## Dependencies

- **Blocks:** [bob-cli-a0.5](bob-cli-a0.5.md) ◐ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.1/README.md) | [bob-cli-a0.1](bob-cli-a0.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c7df845`](https://github.com/bobs-org/bob-cli/commit/c7df845f34b8301434ebb616516da0578dd80073) | docs(license): adopt MIT license for public docs site | [bob-cli-a0.1](bob-cli-a0.1.md) | 2026-10-19 19:02:17 EDT |
| bob-mac-capture | [`bob-mac-capture@065908f`](https://github.com/bobs-org/bob-mac-capture/commit/065908f89c1646dcbf77dad90e4de0f4cbdb4607) | docs(license): adopt MIT license | [bob-cli-a0.1](bob-cli-a0.1.md) | 2026-10-19 19:03:17 EDT |
