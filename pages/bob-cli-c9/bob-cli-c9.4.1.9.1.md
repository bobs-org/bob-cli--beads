# Bead: bob-cli-c9.4.1.9.1 — Fix overwrite selection, refusals, and refusal coverage

[Bead Pages](../README.md) / [bob-cli-c9.4.1.9](bob-cli-c9.4.1.9.md) / bob-cli-c9.4.1.9.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-c9.4.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-c9.4.1.land.md) · **Assignee:** `bob-cli-c9.4.1.9.1` · **Size:** medium
**Created:** 2026-10-26 03:39:12 EDT · **Closed:** 2026-10-26 04:29:40 EDT
**Plan:** [202610/overwrite\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/overwrite_landing_fixes.md)

## Description

selection: honor -N on URL and collection overwrite, refuse disabled ingest, archived reopen, and unstampable statuses before render, match the annotated refusal text, add the reread overwrite hint, surface verify_failed, and cover every refusal code with CLI tests.

## Notes

[2026-10-26T08:29:40Z · bob-cli-c9.4.1.9.1] Implemented selected -N overwrite, refusal preflights and coverage, annotated refusal wording, unread reread hints, and human-visible verify_failed. Verified with focused local/web/collection CLI tests, the CommandError unit test, cargo fmt, and just docs-gen.

## Dependencies

- **Blocks:** [bob-cli-c9.4.1.9.2](bob-cli-c9.4.1.9.2.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-c9.4.1.9.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-c9.4.1.9.1/README.md) | [bob-cli-c9.4.1.9.1](bob-cli-c9.4.1.9.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3e9da7c`](https://github.com/bobs-org/bob-cli/commit/3e9da7cc63731672dbe04794a2520b72ca7feb94) | fix(highlights): honor overwrite selection and refusal contracts | [bob-cli-c9.4.1.9.1](bob-cli-c9.4.1.9.1.md) | 2026-10-26 04:30:31 EDT |
