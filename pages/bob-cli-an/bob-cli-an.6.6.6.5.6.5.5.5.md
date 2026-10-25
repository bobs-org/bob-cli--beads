# Bead: bob-cli-an.6.6.6.5.6.5.5.5 — Write lib-test executable stubs without an ETXTBSY race

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5](bob-cli-an.6.6.6.5.6.5.5.md) / bob-cli-an.6.6.6.5.6.5.5.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.5` · **Size:** small
**Created:** 2026-10-25 07:49:27 EDT · **Closed:** 2026-10-25 08:07:51 EDT
**Plan:** [202610/backlog\_batch8\_listen\_manifest\_mac\_ci\_flakes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch8_listen_manifest_mac_ci_flakes.md)

## Description

lib-stub-etxtbsy: resolve bob-cli-5l by routing every lib-test executable stub through one fork-safe scratch-then-copy writer.

## Notes

[2026-10-25T12:07:51Z · bob-cli-an.6.6.6.5.6.5.5.5] lib-stub-etxtbsy done: new shared crate::native::test_stub::write_executable_stub (scratch-payload + cp onto fresh inode, bob-cli-o pattern) with ported fork-stress regression test; all 8 lib-test stub writers routed through it (fetch write_fake_curl, listen/kick/profile/adapter write_executable|write_script, task_move commit-msg hook, plus dedup of already-safe diagrams/create writers); gkeep/pull.rs verified to have no executable stub writers. Verified: new stress test passes; affected modules pass (43+63+35 tests); 6 consecutive cargo test --lib -- --test-threads=64 runs all 3412 passed 0 failed; just check exit 0 with no new warnings. Target task bob-cli-5l left open for the lander per epic rules.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.5/README.md) | [bob-cli-an.6.6.6.5.6.5.5.5](bob-cli-an.6.6.6.5.6.5.5.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f4f6a9c`](https://github.com/bobs-org/bob-cli/commit/f4f6a9caa3968a1dc2751baa4cfb2faca804f670) | test(native): route lib-test executable stubs through fork-safe shared writer | [bob-cli-an.6.6.6.5.6.5.5.5](bob-cli-an.6.6.6.5.6.5.5.5.md) | 2026-10-25 08:09:00 EDT |
