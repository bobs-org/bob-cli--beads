# Bead: bob-cli-an.6.6.6.5.4 — Do not relocate a completed Task Link into a Pomodoro that already has it

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5](bob-cli-an.6.6.6.5.md) / bob-cli-an.6.6.6.5.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.4` · **Size:** medium
**Created:** 2026-10-24 07:37:07 EDT · **Closed:** 2026-10-24 08:00:22 EDT
**Plan:** [202610/backlog\_batch5\_highlights\_render\_pomodoro\_name\_duplicate\_link\_mac\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch5_highlights_render_pomodoro_name_duplicate_link_mac_ci.md)

## Description

completed-link-dedupe: resolve bob-cli-2l by passing dedupe_into_destination from reconcile and matching that contract in the bob-plugins task-status-cycler.

## Notes

[2026-10-24T12:00:22Z · bob-cli-an.6.6.6.5.4] 2l dedupe landed and verified. Rust: reconcile (task_status_hooks/sync.rs) now passes dedupe_into_destination=true, matching capture-side retirement; stale 'Reconcile passes false' comment and docs/task-status-hooks.md updated to the shared contract (first copy moved to completed fallback keeps tomato marker; duplicates dropped). New Rust regression mirrors the bead repro (completed entry already linking task + open untimed placeholder, no open timed): single struck marked link, placeholder dropped, moved empty. bob-plugins: exhaustive search proved the cycler never moves/inserts daily plain-link bullets on task close (vault-wide retirement handles embeds only; active strike is in-place and idempotent), so no src change was needed for parity; added a cycler regression test locking in the no-duplicate contract. Verified: just check green (5397 passed/0 failed), just docs-check green (447 passed), full bob-plugins npm test green (3530 passed/0 failed). No plugin deploy needed (main.js untouched, test script only); no epic-symbol leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.4/README.md) | [bob-cli-an.6.6.6.5.4](bob-cli-an.6.6.6.5.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`ae025fd`](https://github.com/bobs-org/bob-cli/commit/ae025fd0f374225350ac8edbf74bca0ad89bd05a) | fix(task-status-hooks): dedupe completed Task Link into occupied Pomodoro | [bob-cli-an.6.6.6.5.4](bob-cli-an.6.6.6.5.4.md) | 2026-10-24 08:01:57 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.4][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-an.6.6.6.5.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.land.md

<!-- sase:referenced-by:end -->
