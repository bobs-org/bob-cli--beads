# Bead: bob-cli-e2.5 — Obsidian homes mirror and Stats cleanup

[Bead Pages](../README.md) / [bob-cli-e2](README.md) / bob-cli-e2.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.15o](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.15o.md) · **Assignee:** `bob-cli-e2.5` · **Size:** medium
**Created:** 2026-10-28 22:26:43 EDT · **Closed:** 2026-10-29 01:27:42 EDT
**Plan:** [202610/task\_root\_fields.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_root_fields.md)

## Description

plugin-mirror: bring the JS homes mirror and theme suggester to the new contract, drop @daily, @review, and short_label handling from Stats and the Day strip, sync shared vectors, add root-mark parity, and deploy.

## Notes

[2026-10-29T05:27:32Z · bob-cli-e2.5--2] PROPOSED FOLLOW-UP: Reconcile the protected bob-navigation-hotkeys deployment from the other checkout, then review and deploy this checkout’s review-label cleanup without overwriting uncommitted changes.

[2026-10-29T05:27:42Z · bob-cli-e2.5--2] Verified npm run build, npm test (4190 pass), npm run validate, and BOB_CLI_DIR=<workspace> npm run docs:check; build:check passed. Regenerated docs/reference/glossary.md. bob plugins sync deployed and confirmed block-id-prompt and bob-ledger-tools up to date. The broad sync protected bob-navigation-hotkeys and task-status-cycler deployments from another checkout; no force overwrite was used, and the navigation deployment follow-up is recorded.

## Dependencies

- **Depends on:** [bob-cli-e2.2](bob-cli-e2.2.md) ✓ · ⧖ 2026-10-28
- **Depends on:** [bob-cli-e2.4](bob-cli-e2.4.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-e2.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-e2.5.md) | [bob-cli-e2.5](bob-cli-e2.5.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`48da763`](https://github.com/bobs-org/bob-cli/commit/48da7636e7eed1f32161fa039aa99b80b614b015) | docs: regenerate root parent glossary | [bob-cli-e2.5](bob-cli-e2.5.md) | 2026-10-29 01:28:29 EDT |
| bob-plugins | [`bob-plugins@06cda80`](https://github.com/bobs-org/bob-plugins/commit/06cda805dd71310c46f047ad50c514ede221b51b) | feat(plugins)!: mirror root fields and retire review buckets | [bob-cli-e2.5](bob-cli-e2.5.md) | 2026-10-29 01:30:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.land][1] | Check whether e2.5 deploys ledger-tools root marks and syncs theme vectors | 1 |
| read-by | [agent:bob-cli-e2.5--2][2] | Need phase scope, design file, and notes before continuing verification | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-dm.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-e2.5.md

<!-- sase:referenced-by:end -->
