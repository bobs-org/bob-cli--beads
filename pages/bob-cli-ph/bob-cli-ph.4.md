# Bead: bob-cli-ph.4 — Every bob-cli writer emits bold drawer headers

[Bead Pages](../README.md) / [bob-cli-ph](README.md) / bob-cli-ph.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5x.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5x.linker.w0.md) · **Assignee:** `bob-cli-ph.4` · **Size:** medium
**Created:** 2026-11-22 17:36:48 EST · **Closed:** 2026-11-25 08:25:42 EST
**Plan:** [202611/true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/true_case_drawers.md)

## Description

bob-writers: every bob-cli writer creates `- **Title**` and `- **Notes**` headers, leaves existing headers untouched, and flips the writer vectors.

## Notes

[2026-11-25T13:25:16Z · bob-cli-ph.4] PROPOSED FOLLOW-UP: docs-check lint fails on clean tree (word budgets: plugin-apis.md 9287>8000, bob-navigation-hotkeys.md 6029>6000); unrelated to bob-writers, needs an owner

[2026-11-25T13:25:42Z · bob-cli-ph.4] bob-writers done: ensure_drawer writes `- **Title**` via new drawer_header_body/line helpers, NOTES_TITLE=Notes, tidy writes `- **Notes**`, new-task drafts resolve to bold (ALL-CAPS kept as typed inside marker). Legacy headers reused untouched (pinned by new legacy_notes test + keep-cases in fixtures). Vectors flipped (RL 5, RW 6, SP 3 cases, created-only). Docs updated (task-drawers, task-requirements; vault-format links only). Verified: cargo fmt clean, lib 8103 pass, cli 4134 pass, parity/gcal/gkeep/gmail/randomize/doc all pass, docs-gen clean. docs-check lint fails identically on clean tree (recorded as PROPOSED FOLLOW-UP). No epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-ph.3](bob-cli-ph.3.md) ✓ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.5](bob-cli-ph.5.md) ◐ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.6](bob-cli-ph.6.md) ◐ · ⧖ 2026-11-22
- **Blocks:** [bob-cli-ph.7](bob-cli-ph.7.md) ◐ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.4/README.md) | [bob-cli-ph.4](bob-cli-ph.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8f88a52`](https://github.com/bobs-org/bob-cli/commit/8f88a52c1cfc59236d6ddc4bd36ee6f11de95afd) | feat(task-drawers): emit bold drawer headers from every writer | [bob-cli-ph.4](bob-cli-ph.4.md) | 2026-11-25 08:27:23 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ph.4][1] | Need the phase scope and design file | 1 |
| read-by | [agent:g1][2] | Check whether phase is blocked on the release gate | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ph.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.g1/README.md

<!-- sase:referenced-by:end -->
