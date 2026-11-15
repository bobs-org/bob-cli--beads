# Bead: bob-cli-ls.2.1.2 — Shared charge attribution and subscription ledger

[Bead Pages](../README.md) / [bob-cli-ls.2.1](bob-cli-ls.2.1.md) / bob-cli-ls.2.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-ls.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.md) · **Assignee:** `bob-cli-ls.2.1.2` · **Size:** medium
**Created:** 2026-11-15 13:23:49 EST · **Closed:** 2026-11-15 15:12:59 EST
**Plan:** [202611/subscription\_core.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/subscription_core.md)

## Description

attribution_ledger: build the deduplicated journal-and-row universe, resolve explicit links and eligible pattern matches, derive coverage-aware subscription ledger facts, and test integer money and calendar boundaries.

## Notes

[2026-11-15T20:12:59Z · bob-cli-ls.2.1.2] Attribution and ledger core landed: journal+row universe with unique joins, explicit-link-over-match (billing/ aliases and .md), inference exclusions, refund netting, coverage-aware typed rows, and coverage-aware timeline. Verified cargo test --lib native::bank::subscriptions (38 passed), cargo fmt, git diff --check, cargo clippy --lib with the just lint gates, and no epic-symbol leftovers.

[2026-11-15T20:37:14Z · bob-cli-ls.2.1.2--1] PROPOSED FOLLOW-UP: complete_themes shell descriptions flake under just check — just check failed capture::complete_themes::configured_shell_describes_never_used_and_unconfigured_create at tests/cli/capture/complete_themes.rs:308 (missing "your type · never used"); isolated cargo test -p bob-obsidian --test cli of that node passed in 0.08s. Matches ready flake bead bob-cli-g8 (command() used bob_command() and the 150 ms production COMPLETE_DEADLINE_MS). Applied g8's one-line helper repair here so this phase's verification can finish: command() now starts from bob_completion_command().

## Dependencies

- **Depends on:** [bob-cli-ls.2.1.1](bob-cli-ls.2.1.1.md) ✓ · ⧖ 2026-11-15
- **Blocks:** [bob-cli-ls.2.1.3](bob-cli-ls.2.1.3.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.1.2.md) | [bob-cli-ls.2.1.2](bob-cli-ls.2.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`96b35f4`](https://github.com/bobs-org/bob-cli/commit/96b35f41c4d20cecc065e85e2fe5ac1d8d191c2c) | feat(bank): add subscription attribution and ledger | [bob-cli-ls.2.1.2](bob-cli-ls.2.1.2.md) | 2026-11-15 16:08:32 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ls.2.1.2--2][1] | Confirm phase completeness before close on host completion | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.1.2.md

<!-- sase:referenced-by:end -->
