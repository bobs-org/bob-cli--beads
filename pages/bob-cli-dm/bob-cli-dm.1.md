# Bead: bob-cli-dm.1 — bob-cli suggestion rule, task field, and \`bob themes suggest\`

[Bead Pages](../README.md) / [bob-cli-dm](README.md) / bob-cli-dm.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2s.linker.w0.md) · **Assignee:** `bob-cli-dm.1` · **Size:** large
**Created:** 2026-10-28 08:45:53 EDT · **Closed:** 2026-10-28 17:37:53 EDT
**Plan:** [202610/task\_theme\_suggestions.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_suggestions.md)

## Description

suggest-core: Rust owns the rule. Parse `theme:` note defaults and `[theme:: X]` task fields, resolve the suggestion and inherited theme, implement the canonical field writer and the write rule as pure functions, add `plan.reading_theme`, ship read-only `bob themes suggest` and the `theme_default_unknown` hint, extend the shared vectors, write PT12 and the vault-format rows, and add the memory records.

## Notes

[2026-10-28T21:39:34Z · bob-cli-dm.1.1.land] Delegated child epic bob-cli-dm.1.1 closed after landing repairs. Phase suggest-core delivered: Rust suggestion rule, canonical task-field helpers, read-only bob themes suggest, theme_default_unknown hints, shared vectors suggest/task_field/write_rule, preservation coverage, PT13 (PT12 remains configured themes), and plan.reading_theme. Memory records were correctly omitted (memory_decision_record=no, memory_glossary_term=no). Landing repairs: scalar trim/off/blank/list classification, canonicalize_pomodoro_name reuse, Null reading_theme is ConfigError, shared field scanner, line-ending preservation, narrow unused-code allowances, cancel/complete preservation of authored (theme::  WRITE). sase tool run check 745957776dd0e3066ad0c0a8a5613093 exit 0: 6408 passed, 0 failed, 1 ignored. just docs-check passed. Scratch-vault human/JSON suggest for override/inherit/off/closed left vault bytes unchanged. epic-symbols bob-cli-dm.1: none. justfile has no symvision recipe. Accepted warm-list p95 file:explicit:babfd9c7f9ecf3f6fe7fddcf 41.400022→37.079298 ms (−4.320724); no rebenchmark. Follow-up triage complete: no PROPOSED FOLLOW-UP; no new task/+1/reopen. ledger_theme_pills and seed_plex_chore remain later outer phases. Outer epic bob-cli-dm left open.

[2026-10-28T21:39:40Z · bob-cli-dm.1.1.land] Delegated child epic bob-cli-dm.1.1 closed after landing repairs. Phase suggest-core delivered: Rust suggestion rule, canonical task-field helpers, read-only bob themes suggest, theme_default_unknown hints, shared vectors suggest/task_field/write_rule, preservation coverage, PT13 (PT12 remains configured themes), and plan.reading_theme. Memory records were correctly omitted (memory_decision_record=no, memory_glossary_term=no). Landing repairs: scalar trim/off/blank/list classification, canonicalize_pomodoro_name reuse, Null reading_theme is ConfigError, shared field scanner, line-ending preservation, narrow unused-code allowances, cancel/complete preservation of authored (theme::  WRITE). sase tool run check 745957776dd0e3066ad0c0a8a5613093 exit 0: 6408 passed, 0 failed, 1 ignored. just docs-check passed. Scratch-vault human/JSON suggest for override/inherit/off/closed left vault bytes unchanged. epic-symbols bob-cli-dm.1: none. justfile has no symvision recipe. Accepted warm-list p95 file:explicit:babfd9c7f9ecf3f6fe7fddcf 41.400022→37.079298 ms (−4.320724); no rebenchmark. Follow-up triage complete: no PROPOSED FOLLOW-UP; no new task/+1/reopen. ledger_theme_pills and seed_plex_chore remain later outer phases. Outer epic bob-cli-dm left open.

## Dependencies

- **Blocks:** [bob-cli-dm.2](bob-cli-dm.2.md) ◐ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dm.3](bob-cli-dm.3.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dm.5](bob-cli-dm.5.md) ◐ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.1.md) | [bob-cli-dm.1](bob-cli-dm.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.1.1.2--3][1] | Confirm parent phase and final epic decisions for assigned CLI work | 1 |
| read-by | [agent:bob-cli-dm.1.1.3][2] | need outer epic decisions and scope | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.1.1.2.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.1.1.3/README.md

<!-- sase:referenced-by:end -->
