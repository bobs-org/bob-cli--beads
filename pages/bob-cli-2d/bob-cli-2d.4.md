# Bead: bob-cli-2d.4 — login and doctor subcommands

[Bead Pages](../README.md) / [bob-cli-2d](README.md) / bob-cli-2d.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.2t](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2t.md) · **Assignee:** `bob-cli-2d.4` · **Size:** medium
**Created:** 2026-09-28 13:31:29 EDT · **Closed:** 2026-09-28 14:35:20 EDT
**Plan:** [202609/bob\_gkeep\_inbox\_drain.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/bob_gkeep_inbox_drain.md)

## Description

auth: implement `bob gkeep login` (hidden cookie prompt or stdin, exchange, store via `token_store_command`, read-back and reachability check) and `bob gkeep doctor` (a styled checklist plus JSON), with integration tests.

## Notes

[2026-09-28T18:35:02Z · bob-cli-2d.4] PROPOSED FOLLOW-UP: Fix pre-existing clippy deny failure in tests/cli.rs:31818 (overly_complex_bool_expr with `|| true`); reproduces on clean tree, see also bob-cli-v

[2026-09-28T18:35:10Z · bob-cli-2d.4] PROPOSED FOLLOW-UP: tests/gkeep_adapter.rs fake_adapter_serves_ping_and_records_the_call flakes with ETXTBSY under parallel load; consider retry-on-EBUSY in the test spawn like AdapterClient already does

[2026-09-28T18:35:20Z · bob-cli-2d.4] Implemented bob gkeep login (TTY hidden prompt/stdin cookie, preflight store check, exchange, stdin store, read-back equality, snapshot reachability, 0600 recovery file) and doctor (7-check human/JSON checklist with skip reasons, exit 0 unless fail). Added tests/gkeep_auth.rs (11 tests) plus unit tests; narrowed the skeleton stub test to list/pull. Verified: cargo fmt --check clean, full cargo test green (1123 lib + 515 cli + all gkeep suites incl. 11 new). cargo clippy has one pre-existing deny failure in tests/cli.rs:31818 reproduced on the clean tree (noted as follow-up).

## Dependencies

- **Depends on:** [bob-cli-2d.2](bob-cli-2d.2.md) ✓ · ⧖ 2026-09-28
- **Blocks:** [bob-cli-2d.7](bob-cli-2d.7.md) ✓ · ⧖ 2026-09-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-2d.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-2d.4/README.md) | [bob-cli-2d.4](bob-cli-2d.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`150b954`](https://github.com/bobs-org/bob-cli/commit/150b954251ddad1662945d98ba2e77ac4c993251) | feat(gkeep): add login and doctor subcommands with integration tests | [bob-cli-2d.4](bob-cli-2d.4.md) | 2026-09-28 14:36:45 EDT |
