# Bead: bob-cli-ce.9 — Argument mode, typed runs, Vim routing, and binding the colon key

[Bead Pages](../README.md) / [bob-cli-ce](README.md) / bob-cli-ce.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5c.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5c.linker.w0.md) · **Assignee:** `bob-cli-ce.9` · **Size:** medium
**Created:** 2026-10-26 10:35:53 EDT · **Closed:** 2026-10-26 13:53:52 EDT
**Plan:** [202610/bob\_colon\_command\_mode.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_colon_command_mode.md)

## Description

args-vim: add argument mode backed by `bob __complete`, a quote-aware tokenizer for typed bob argv with excluded-command refusal, and Vim routing (`::`, Vim-shaped input, fallback row, handleEx). It also adds the vimrc lint, then binds `:` in the vault vimrc.

## Notes

[2026-10-26T17:53:42Z · bob-cli-ce.9] PROPOSED FOLLOW-UP: Resolve the pre-existing BOB_TEST_FIXTURE_PDF docs lint finding — npm run docs:check fails in the clean bob-cli checkout at c048955 in src/native/highlights_ref/source_store.rs:194; bob-cli-ce.6 and bob-cli-ce.8 already record it, and no task bead exists to cite.

[2026-10-26T17:53:52Z · bob-cli-ce.9] Implemented argument mode with bob __complete, quote-aware typed argv and exclusion refusal, Vim routing, vimrc lint, and the colon binding. Verified the command-mode tests (30/30), build:check, explicit plugin deployment, and vault sync (local and remote SHA 92c3a71 match). docs:check still reports the clean-base BOB_TEST_FIXTURE_PDF finding, recorded as a proposed follow-up; epic-symbols is clear.

## Dependencies

- **Depends on:** [bob-cli-ce.1](bob-cli-ce.1.md) ✓ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-ce.11](bob-cli-ce.11.md) ✓ · ⧖ 2026-10-26
- **Depends on:** [bob-cli-ce.4](bob-cli-ce.4.md) ✓ · ⧖ 2026-10-26
- **Depends on:** [bob-cli-ce.8](bob-cli-ce.8.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ce.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.9/README.md) | [bob-cli-ce.9](bob-cli-ce.9.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6f8f1c5`](https://github.com/bobs-org/bob-plugins/commit/6f8f1c5c93edec5c2d82d41b3bc6d49760aff302) | feat(command-mode): add argument and Vim routing | [bob-cli-ce.9](bob-cli-ce.9.md) | 2026-10-26 14:06:09 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ce.9][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ce.9/README.md

<!-- sase:referenced-by:end -->
