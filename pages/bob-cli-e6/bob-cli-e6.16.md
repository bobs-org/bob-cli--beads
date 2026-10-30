# Bead: bob-cli-e6.16 — Memory, config spelling, vectors cleanup, and acceptance

[Bead Pages](../README.md) / [bob-cli-e6](README.md) / bob-cli-e6.16

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2t.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2t.linker.w0.md) · **Assignee:** `bob-cli-e6.16` · **Size:** small
**Created:** 2026-10-29 16:16:34 EDT · **Closed:** 2026-10-30 01:54:02 EDT
**Plan:** [202610/task\_types.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_types.md)

## Description

closeout: rename the glossary strand, add the two decision records, switch chezmoi to types:, drop the retired write_rule vectors, sweep docs, and run the acceptance cases.

## Notes

[2026-10-30T05:33:44Z · bob-cli-e6.16] PROPOSED FOLLOW-UP: Installed Bob still exposes only `themes` (`bob --help` lists no `types`, and `bob types list -f json` is rejected), so the conditional chezmoi `themes:`→`types:` edit was not applicable; leave home config unchanged until the installed CLI supports the alias.

[2026-10-30T05:33:49Z · bob-cli-e6.16] PROPOSED FOLLOW-UP: Retain the deprecated `api.themes.planThemeChange` wrapper for now: live block-id-prompt callers still read `opts.planThemeChange`; remove it only after those callers migrate.

[2026-10-30T05:38:26Z · bob-cli-e6.16] PROPOSED FOLLOW-UP: `bob-plugins` `npm test` fails identically on the clean base and this phase tree in `scripts/test-task-status-cycler-successor-wiring.cjs` (successor type writes and project-finished type transform assertions; actual tasks remain unchanged). This is pre-existing task-status-cycler acceptance drift; no matching task bead was found.

[2026-10-30T05:47:48Z · bob-cli-e6.16] PROPOSED FOLLOW-UP: A final source-doc scan found remaining user-facing “Pomodoro themes” manager names/notices in bob-navigation-hotkeys (e.g. src/490-plugin-lifecycle.js and src/202-pomodoro-themes-manager.js), plus stale theme-era API wording. This phase covered the docs sweep and retired vectors; update the remaining UI copy in a later scoped change.

[2026-10-30T05:54:02Z · bob-cli-e6.16] Renamed the authorized glossary strand and links; removed retired write_rule vectors/checks; swept task-type docs; verified D7/D8 routing vectors, typed placement, inherited-type relocation, docs-gen/docs-check, and plugin docs-check/sync. Installed Bob lacks , so chezmoi stayed unchanged per plan; npm test failures reproduced identically on clean base and were recorded as follow-ups.

## Dependencies

- **Depends on:** [bob-cli-e6.11](bob-cli-e6.11.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.12](bob-cli-e6.12.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.14](bob-cli-e6.14.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.15](bob-cli-e6.15.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.3](bob-cli-e6.3.md) ✓ · ⧖ 2026-10-29
- **Depends on:** [bob-cli-e6.9](bob-cli-e6.9.md) ✓ · ⧖ 2026-10-29

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-e6.16](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-e6.16/README.md) | [bob-cli-e6.16](bob-cli-e6.16.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3aa31b3`](https://github.com/bobs-org/bob-cli/commit/3aa31b349ab2dd1e290bb7f26e2c43c74f9657df) | chore(types): close out glossary docs and vectors | [bob-cli-e6.16](bob-cli-e6.16.md) | 2026-10-30 01:55:16 EDT |
