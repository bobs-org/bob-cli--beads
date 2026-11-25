# Bead: bob-cli-q4.8.1.1 — Port the pure settle transform and pin Rust parity

[Bead Pages](../README.md) / [bob-cli-q4.8.1](bob-cli-q4.8.1.md) / bob-cli-q4.8.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q4.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q4.8.md) · **Assignee:** `bob-cli-q4.8.1.1` · **Size:** medium
**Created:** 2026-11-25 10:27:08 EST · **Closed:** 2026-11-25 11:09:22 EST
**Plan:** [202611/task\_settle\_twin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/task_settle_twin.md)

## Description

pure-twin: port the Rust schedule, grouping, badge, and surviving-line-map behavior into pure bob-ledger-tools fragments. Run all canonical settle vectors through the built bundle and enforce byte-identical fixture copies. Export testable helpers without advertising an incomplete taskSettle v1 namespace.

## Notes

[2026-11-25T16:08:42Z · bob-cli-q4.8.1.1] PROPOSED FOLLOW-UP: 10 pre-existing task-status-cycler unit failures reproduce identically on the clean base (bob-plugins HEAD 5ed3bd22, verified in a detached worktree): test-task-status-cycler-open-line.cjs "creating a notes drawer before a work-log origin shifts origin by two", plus 9 req failures in test-task-status-cycler-req-toggle.cjs and test-task-status-cycler-task-reqs-vectors.cjs (NOTES drawer landing, missing-final-newline, CRLF tidy). Unrelated to the pure-twin change (cycler bundle byte-identical).

[2026-11-25T16:08:48Z · bob-cli-q4.8.1.1] PROPOSED FOLLOW-UP: bob-plugins npm run docs:check lint fails on word budgets in files untouched by this phase (docs/develop/plugins/plugin-apis.md 9287 words vs 8000 cap; docs/reference/plugins/bob-navigation-hotkeys.md 6068 vs 6000 cap). Pre-existing; needs a docs-budget pass.

[2026-11-25T16:09:06Z · bob-cli-q4.8.1.1] PROPOSED FOLLOW-UP: test-ledger-tools-frees-marks.cjs "200-link / 2000-task build stays within the 25 ms budget" failed once in the full-suite run but passes in isolation on both base and current trees; treat as load flake, consider raising the budget or isolating the perf file.

[2026-11-25T16:09:22Z · bob-cli-q4.8.1.1] pure-twin done: 4 new ledger-tools fragments (139a model/classification/eligibility, 139b grouping parser, 139c grouping emitter, 139d settle+Myers line-map) with test exports in 351-exports-task-settle. All 18 canonical settle vectors pass through the built bundle (bytes, changed, line maps, warnings, second-pass no-op); Rust settle_vectors + 61 task_status_groups tests pass. Fixture dir copied byte-identical with update-bob-cli-first README note; 3 new test files registered and passing (10/10); manifest bumped 1.157.1->1.158.0, build:check and docs inventory green, deployed via bob plugins sync -p. No v1 namespace published. 10 cycler + docs-lint + 1 perf-flake failures recorded as PROPOSED FOLLOW-UP (reproduce on clean base).

## Dependencies

- **Blocks:** [bob-cli-q4.8.1.2](bob-cli-q4.8.1.2.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q4.8.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.1/README.md) | [bob-cli-q4.8.1.1](bob-cli-q4.8.1.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5c0f816`](https://github.com/bobs-org/bob-cli/commit/5c0f81608f94cd41ceddb726736a79ea944030bd) | feat(task-settle): add canonical task-settle fixture README | [bob-cli-q4.8.1.1](bob-cli-q4.8.1.1.md) | 2026-11-25 11:10:42 EST |
| bob-plugins | [`bob-plugins@824d8e4`](https://github.com/bobs-org/bob-plugins/commit/824d8e4951ef11c492cf515b4200390b4c0a35fd) | feat(ledger-tools): port task-settle to pure-twin fragments 139a-d | [bob-cli-q4.8.1.1](bob-cli-q4.8.1.1.md) | 2026-11-25 11:11:20 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q4.8.1.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-q4.8.1.1/README.md

<!-- sase:referenced-by:end -->
