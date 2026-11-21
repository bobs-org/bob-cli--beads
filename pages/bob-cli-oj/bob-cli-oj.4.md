# Bead: bob-cli-oj.4 — Grouped record walk model and the record group provider

[Bead Pages](../README.md) / [bob-cli-oj](README.md) / bob-cli-oj.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1es](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1es.md) · **Assignee:** `bob-cli-oj.4` · **Size:** medium
**Created:** 2026-11-21 07:41:35 EST
**Plan:** [202611/bracket\_n\_group\_jumps.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bracket_n_group_jumps.md)

## Description

record-groups: in bob-ledger-tools, mirror bob's group-major order in the record walk model from the shared vectors, gate sync requests on bob's capability, and extend `api.navGroups` with record group stops (heads of the neighboring occupied groups, wrapping).

## Notes

[2026-11-21T16:48:26Z · bob-cli-oj.4--1] PROPOSED FOLLOW-UP: Record the deferred `memory_decision_group_stops` decision if the policy becomes accepted; this phase intentionally did not edit the decisions web because the plan selected no.

[2026-11-21T16:48:31Z · bob-cli-oj.4--1] PROPOSED FOLLOW-UP: Fix docs-check base lint budgets in `docs/develop/plugins/plugin-apis.md` (8165/8000 words) and `docs/reference/vault-format.md` (6016/6000 words); `npm run docs:check` reproduced both warnings with the plugin checkout clean.

## Dependencies

- **Depends on:** [bob-cli-oj.2](bob-cli-oj.2.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-oj.3](bob-cli-oj.3.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.5](bob-cli-oj.5.md) ◐ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-oj.6](bob-cli-oj.6.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-oj.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-oj.4.md) | [bob-cli-oj.4](bob-cli-oj.4.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@d8dc11e`](https://github.com/bobs-org/bob-plugins/commit/d8dc11eafae367bf05b464be86ed4d1a10cfe05b) | feat(ledger-tools): add grouped record navigation | [bob-cli-oj.4](bob-cli-oj.4.md) | 2026-11-21 11:42:38 EST |
| bob-plugins | [`bob-plugins@bd8f2d4`](https://github.com/bobs-org/bob-plugins/commit/bd8f2d46219b794996e8563e3410bbc6e7e58e3c) | docs(plugins): refresh ledger tools inventory for 1.149.2 | [bob-cli-oj.4](bob-cli-oj.4.md) | 2026-11-21 11:56:43 EST |
