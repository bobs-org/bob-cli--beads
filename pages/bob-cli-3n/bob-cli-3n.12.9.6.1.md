# Bead: bob-cli-3n.12.9.6.1 — Fix the nav writer regressions and finish its missing tests

[Bead Pages](../README.md) / [bob-cli-3n.12.9.6](bob-cli-3n.12.9.6.md) / bob-cli-3n.12.9.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-3n.12.9.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-3n.12.9.land.md) · **Assignee:** `bob-cli-3n.12.9.6.1` · **Size:** medium
**Created:** 2026-10-03 02:54:24 EDT · **Closed:** 2026-10-03 03:08:35 EDT
**Plan:** [202610/task\_dep\_links\_landing\_remaining.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links_landing_remaining.md)

## Description

nav-writer-regressions: build the recovery snapshot for field-only clears and gate the hand-edit clear read, load source-linked notes in the counted vault path, make counted remove one transaction with the blockquote notice on every Ctrl+D path, align nav with DP30, and add the plugin-level writer tests the previous phase left out.

## Notes

[2026-10-03T07:08:25Z · bob-cli-3n.12.9.6.1] nav-writer-regressions done: main.js fixes (snapshot gate w/ field-only clears + add passthrough at both call sites; hand-edit clear [?]-gated read; counted vault add best-effort source-link loads; removeCountedDependency single-transaction refuse-before-write + changed-only counts; blockquote notices on single+counted Ctrl+D; DP30 row+ownership test, nav already agreed so test-only). Tests: writer 26/26, DP 28/28, full npm test 1366/1366, validate 6/6. Pre-fix probe (main.js stashed): 6 new tests fail with the predicted symptoms (field-clear recovers [ ] not [*]; 2 extra reads; target-not-found refusal; generic delete notice; dependsOn-not-set path; partial-write success). Manifest 1.62.0, README row bumped, deployed via bob plugins sync (2 copied).

[2026-10-03T07:08:35Z · bob-cli-3n.12.9.6.1] Verified: writer 26/26, DP vectors 28/28, full npm test 1366/1366 pass, validate 6/6, nav 1.62.0 deployed via bob plugins sync; 6 new tests fail on pre-fix main.js with the predicted symptoms (field-clear [ ] vs [*], 2 extra reads, target-not-found, generic notices, partial-write success). No epic-symbols left.

## Dependencies

- **Blocks:** [bob-cli-3n.12.9.6.2](bob-cli-3n.12.9.6.2.md) ✓ · ⧖ 2026-10-03
- **Blocks:** [bob-cli-3n.12.9.6.5](bob-cli-3n.12.9.6.5.md) ◐ · ⧖ 2026-10-03

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.12.9.6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.12.9.6.1/README.md) | [bob-cli-3n.12.9.6.1](bob-cli-3n.12.9.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f905e10`](https://github.com/bobs-org/bob-plugins/commit/f905e1042727d09527fadd7bad3fddfa125f74db) | fix(nav): close writer regressions — recovery snapshot gate, counted single-transaction remove, blockquote refusals, DP30 (1.62.0) | [bob-cli-3n.12.9.6.1](bob-cli-3n.12.9.6.1.md) | 2026-10-03 03:09:26 EDT |
