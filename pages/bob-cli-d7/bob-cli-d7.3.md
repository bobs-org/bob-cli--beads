# Bead: bob-cli-d7.3 — Make the completion PTY and zpty tests load-tolerant

[Bead Pages](../README.md) / [bob-cli-d7](README.md) / bob-cli-d7.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14v](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14v.md) · **Assignee:** `bob-cli-d7.3` · **Size:** medium
**Created:** 2026-10-27 14:54:31 EDT
**Plan:** [202610/backlog\_batch\_a1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_a1.md)

## Description

completion-load-flakes: reproduce the bash and zsh completion driver failures under load, pin test-only deadlines and replace fixed sleeps with bounded readiness waits, prove repeated loaded runs pass, and close bob-cli-8q.

## Notes

[2026-10-27T19:18:34Z · bob-cli-d7.3] The shared test-only completion deadline also covers tests/cli/aliases.rs::complete_values, so bob-cli-b9 is covered for the next epic to re-check; bob-cli-b9 remains open. Historical bob-cli-8q baseline: 1/1 loaded failure, 0/1 isolated rerun; local pre-fix PTY attempts skipped due the invalid zpty -t usage. Post-fix: 5 consecutive loaded completion-module runs passed (116 each, 0/580 failures). The phase worker will close only bob-cli-d7.3 as instructed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-d7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d7.3.md) | [bob-cli-d7.3](bob-cli-d7.3.md) | 0 |
