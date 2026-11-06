# Bead: bob-cli-hg.12.1.4 — Durable send state and recovery engine

[Bead Pages](../README.md) / [bob-cli-hg.12.1](bob-cli-hg.12.1.md) / bob-cli-hg.12.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-hg.12](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-hg.12.md) · **Assignee:** `bob-cli-hg.12.1.4` · **Size:** medium
**Created:** 2026-11-06 07:12:29 EST · **Closed:** 2026-11-06 13:35:24 EST
**Plan:** [202611/gmail\_compose.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/gmail_compose.md)

## Description

send-recovery: implement durable state transitions, serialization, draft-id-only dispatch, and recovery classification with fault tests; keep the engine internal as in section 4.4.

## Notes

[2026-11-06T18:35:24Z · bob-cli-hg.12.1.4] send-recovery engine implemented and verified: durable gmail_send frontmatter state (state.rs), draft-id-only drafts send adapter with exact allowlist (gog.rs), internal recovery/dispatch engine with injected-transport fault tests (send.rs, 16 tests: crash/restart, timeout, lost-response ack, unique/old/ambiguous/no-evidence SENT, lookup failure, intent/ack persist failures, malformed state, race sends once, writer/scope refusals, stale digest, RFC preference, body-free journals). Fake gog extended with drafts send + in:sent/thread support. Gates: cargo fmt --check clean, cargo clippy workspace gate exit 0, cargo test --lib native::gmail 226 pass, gmail_draft 5 pass, gmail_shell/search_peek/pull_attach 46 pass.

## Dependencies

- **Depends on:** [bob-cli-hg.12.1.3](bob-cli-hg.12.1.3.md) ✓ · ⧖ 2026-11-06
- **Blocks:** [bob-cli-hg.12.1.5](bob-cli-hg.12.1.5.md) ◐ · ⧖ 2026-11-06

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-hg.12.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-hg.12.1.4/README.md) | [bob-cli-hg.12.1.4](bob-cli-hg.12.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`8935148`](https://github.com/bobs-org/bob-cli/commit/8935148f6933c96f6e709bdb161d69bcc411573c) | feat(gmail): add durable send-recovery engine for compose drafts | [bob-cli-hg.12.1.4](bob-cli-hg.12.1.4.md) | 2026-11-06 13:37:00 EST |
