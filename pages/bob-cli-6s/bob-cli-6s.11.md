# Bead: bob-cli-6s.11 — task-status-cycler and block-id-prompt

[Bead Pages](../README.md) / [bob-cli-6s](README.md) / bob-cli-6s.11

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.0z.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.0z.linker.w0.md) · **Assignee:** `bob-cli-6s.11` · **Size:** medium
**Created:** 2026-10-12 08:34:40 EDT · **Closed:** 2026-10-12 09:13:56 EDT
**Plan:** [202610/prj\_task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/prj_task_dep_links.md)

## Description

plugins-compat: cycler member recovery and refusal to hand-unblock project-blocked tasks; block-id-prompt consumes instead of force-linking dependency- or project-blocked targets.

## Notes

[2026-10-12T13:13:14Z · bob-cli-6s.11] PROPOSED FOLLOW-UP: Fix the 19 existing bob-plugins npm test failures in the clean base suite — the same failures reproduced before and after this phase changes (unblocked-glyph 4, keep-count 1, picker-single 2, successor-polish/wiring 12).

[2026-10-12T13:13:56Z · bob-cli-6s.11] Implemented project-blocked resident recovery and blocked-target gesture consumption. Verified npm run build, npm run validate, focused tests (147/147), git diff --check, plugin sync, and no remaining epic symbols. Full npm test has 19 failures reproduced identically on clean base; recorded as a proposed follow-up.

## Dependencies

- **Depends on:** [bob-cli-6s.1](bob-cli-6s.1.md) ✓ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6s.12](bob-cli-6s.12.md) ◐ · ⧖ 2026-10-12
- **Blocks:** [bob-cli-6s.13](bob-cli-6s.13.md) ◐ · ⧖ 2026-10-12

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-6s.11](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6s.11/README.md) | [bob-cli-6s.11](bob-cli-6s.11.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-6s.11][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-6s.11/README.md

<!-- sase:referenced-by:end -->
