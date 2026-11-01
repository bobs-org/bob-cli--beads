# Bead: bob-cli-f9.2 — bob-cli retires plan.max\_themes and plan.strict

[Bead Pages](../README.md) / [bob-cli-f9](README.md) / bob-cli-f9.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.by](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.by.md) · **Assignee:** `bob-cli-f9.2` · **Size:** medium
**Created:** 2026-11-01 12:12:35 EST · **Closed:** 2026-11-01 13:33:20 EST
**Plan:** [202611/retire\_type\_cap\_today\_roots.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/retire_type_cap_today_roots.md)

## Description

cli-drop-type-cap: remove the type cap from bob-cli config, plan budget, capture, routing contract, every strict refusal path, completion previews, reconcile output, tests, fixtures, and docs; bump bob plan JSON to schema 3; clean Bryan's chezmoi config; optionally add the decision record.

## Notes

[2026-11-01T18:33:20Z · bob-cli-f9.2] Retired plan.max_themes and plan.strict across bob-cli: config (stale keys ignored), plan budget (links-only status, LINT_THEME_CAP gone), routing contract (Place/Relocate inputs and Refused variants removed; applier returns Option), every strict refusal path (capture, retype, move, ref-today, successors, completion previews, reconcile), bob plan JSON schema 3, vectors/agenda fixtures, docs (plan, capture, task-types, task-dependencies, task-status-hooks, task-move, ref, json-outputs, configuration, how-to, regenerated CLI reference + plan.svg), tutorial schema gate, benchmark script, and Bryan's chezmoi config. Verified: just all (fmt, lint, cargo test workspace: 4267 lib + 2614 cli pass) and just docs-check pass. No memory notes edited per decisions. PROPOSED FOLLOW-UP: none.

## Dependencies

- **Blocks:** [bob-cli-f9.3](bob-cli-f9.3.md) ◐ · ⧖ 2026-11-01
- **Blocks:** [bob-cli-f9.4](bob-cli-f9.4.md) ◐ · ⧖ 2026-11-01

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-f9.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f9.2/README.md) | [bob-cli-f9.2](bob-cli-f9.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3de72bf`](https://github.com/bobs-org/bob-cli/commit/3de72bfd844248d30b3c9aa0eaa01454fa6b0cc5) | feat(plan)!: retire the daily type cap and plan.strict | [bob-cli-f9.2](bob-cli-f9.2.md) | 2026-11-01 13:47:14 EST |
| chezmoi | [`chezmoi@aa84457`](https://github.com/bbugyi200/dotfiles/commit/aa844572a19e9bede2dce7f025c637762b23aa49) | chore: drop retired plan.max\_themes and plan.strict from bob config | [bob-cli-f9.2](bob-cli-f9.2.md) | 2026-11-01 13:50:00 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-f9.2][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-f9.2/README.md

<!-- sase:referenced-by:end -->
