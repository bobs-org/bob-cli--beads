# Bead: bob-cli-6s.1 — Project-dependency contract and PD vectors

[Bead Pages](../README.md) / [bob-cli-6s](README.md) / bob-cli-6s.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0z.linker.w0.md) · **Assignee:** `bob-cli-6s.1` · **Size:** medium
**Created:** 2026-10-12 08:34:40 EDT · **Closed:** 2026-10-12 08:53:26 EDT
**Plan:** [202610/prj\_task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_task_dep_links.md)

## Description

contract: add docs/task-dependencies.md §13 (storage, R0 hoist, ^prj R-rules, inherited Blocked, consumption, guards) with PD vectors, and amend the sections it makes false.

## Notes

[2026-10-12T12:52:10Z · bob-cli-6s.1] PROPOSED FOLLOW-UP: percent-listen CLI tests fail on clean master — capture::r#ref::failed_percent_listen_worker_keeps_listen_retry_guidance (listen runner was invoked) and percent_listen_reference_runs_existing_worker_and_installs_audio (listen.log NotFound); reproduced identically after stashing this phase's docs; already tracked by bob-cli-6m

[2026-10-12T12:53:26Z · bob-cli-6s.1] Added docs/task-dependencies.md §13 (storage, R0 hoist, ^prj R-rules, inherited Blocked, consumption, guards) with PDP/PDW/PDR/PDB/PDL/PDG/PDC/PDF vectors; amended §§1–2.1, 4.2–4.3, 5, 6.1, 6.4, 8, 10, 11, 12.2, 12.5–12.6; pointers in docs/task-status-hooks.md Derived Blocked and docs/projects.md. just all: fmt+clippy green; 1365 cli tests passed; 2 percent-listen failures reproduce on clean master (bob-cli-6m). epic-symbols: none leftover.

## Dependencies

- **Blocks:** [bob-cli-6s.11](bob-cli-6s.11.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6s.2](bob-cli-6s.2.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6s.8](bob-cli-6s.8.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6s.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6s.1/README.md) | [bob-cli-6s.1](bob-cli-6s.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`75e323b`](https://github.com/bobs-org/bob-cli/commit/75e323b2d6c59899a0b739b8079e2087fbfbb90e) | docs(task-deps): add §13 project-dependency contract and PD vectors | [bob-cli-6s.1](bob-cli-6s.1.md) | 2026-10-12 08:54:38 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6s.1][1] | Need full description, notes, and remaining work | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6s.1/README.md

<!-- sase:referenced-by:end -->
