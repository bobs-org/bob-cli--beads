# Bead: bob-cli-ex.2.1.2 — Enable the colon seal and verify the public capture protocol

[Bead Pages](../README.md) / [bob-cli-ex.2.1](bob-cli-ex.2.1.md) / bob-cli-ex.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ex.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ex.2.md) · **Assignee:** `bob-cli-ex.2.1.2` · **Size:** medium
**Created:** 2026-10-31 13:56:45 EDT · **Closed:** 2026-10-31 16:01:01 EDT
**Plan:** [202610/project\_note\_offer\_form.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_offer_form.md)

## Description

offer_language: enable @route:id@ in execution, editor parsing, completion, and sealed separator rewrites. Add CLI coverage of selections, destinations, atomic failures, and mixed-draft offers, and update CLI help and its generated reference pages.

## Notes

[2026-10-31T20:01:01Z · bob-cli-ex.2.1.2] Enabled @route:id@ offer form: execution grammar, editor spans/modes, completion intent, sealed :/^ rewrite toggles, updated CLI help + regenerated reference goldens. Verified: cargo fmt clean, full workspace tests green (4206 lib + 2572 cli), just docs-check passed, CLI tests cover selections/destinations/atomic failures/mixed drafts and invariant-1 byte equality, epic-symbols clean.

## Dependencies

- **Depends on:** [bob-cli-ex.2.1.1](bob-cli-ex.2.1.1.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ex.2.1.3](bob-cli-ex.2.1.3.md) ◐ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ex.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.2.1.2/README.md) | [bob-cli-ex.2.1.2](bob-cli-ex.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e9b9cd1`](https://github.com/bobs-org/bob-cli/commit/e9b9cd1dcf7c4696563060978856b726631fa6b0) | feat(capture): enable @route:id@ project-note offer form end to end | [bob-cli-ex.2.1.2](bob-cli-ex.2.1.2.md) | 2026-10-31 16:18:40 EDT |
