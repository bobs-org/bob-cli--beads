# Bead: bob-cli-5k.2 — Stop lib tests from racing on process environment

[Bead Pages](../README.md) / [bob-cli-5k](README.md) / bob-cli-5k.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0y2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y2.md) · **Assignee:** `bob-cli-5k.2` · **Size:** medium
**Created:** 2026-10-07 14:38:40 EDT · **Closed:** 2026-10-07 15:26:17 EDT
**Plan:** [202610/close\_top\_ten\_impact\_beads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/close_top_ten_impact_beads.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | [bead:bob-cli-5l][1] | proposed by bob-cli-5k.2 note #1 during env-isolation stress runs |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-5l/README.md

<!-- sase:links:end -->

## Description

env-isolation: replace every module-private env-mutating test helper with one shared isolation mechanism that never lets a test see another test's BOB_DAY_FILE or BOB_NOW, enforce it with clippy, stress-test it, and close bob-cli-2e, bob-cli-40 (superseded) and bob-cli-5c.

## Notes

[2026-10-07T19:25:36Z · bob-cli-5k.2] PROPOSED FOLLOW-UP: fetch fake-curl exec intermittently hits ETXTBSY under full-suite load — seen 2x in 26 parallel full lib runs on athena (Text file busy on a just-written unique-path fake-curl.sh), 0x in 20 base runs and 0x in 20 isolated fetch-loop runs; write-chmod-exec sequence is unchanged from base and script paths are unique per test, so this looks like a filesystem-under-load artifact rather than the env race; lander should watch for it in just check and consider a bounded ETXTBSY retry in write_fake_curl setup or a sandbox-fs investigation if it recurs

[2026-10-07T19:26:17Z · bob-cli-5k.2] env-isolation done on athena, tree master 6244ddd plus uncommitted phase diff (42 files + clippy.toml). Shared thread-local facility in src/native/env.rs (TestEnvGuard/with_var/snapshot_overrides/inherit_overrides/pin_tz_utc0); all production env reads via bob_env::var/var_os; every module-private with_env/ENV_LOCK/DAY_FILE_LOCK/CURL_TEST_LOCK deleted or facility-backed; clippy.toml disallowed-methods for set_var/remove_var (firing verified with a probe). Verified: rg set_var/remove_var only in facility; cargo fmt clean; cargo check zero warnings; cargo clippy --all-targets exit 0; full cargo test --lib 1874/1874 repeatedly (3/3 final, 9/10 + 8/8@64t with the only failures being the ETXTBSY load flake recorded as follow-up); victims+related 20/20; base fails the env race 8/20 for contrast. Closed 2e done, 40 superseded, 5c done. Known non-phase failures skipped by name per plan s2 (4j kinds, 4u pandoc). One ETXTBSY follow-up noted on this bead.

## Dependencies

- **Blocks:** [bob-cli-5k.3](bob-cli-5k.3.md) ✓ · ⧖ 2026-10-07

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5k.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.2/README.md) | [bob-cli-5k.2](bob-cli-5k.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c9b17c9`](https://github.com/bobs-org/bob-cli/commit/c9b17c96fb66af96e110b1d111f52380e1c8b601) | test(env): add crate-wide thread-local test-env facility | [bob-cli-5k.2](bob-cli-5k.2.md) | 2026-10-07 15:27:55 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5k.2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5k.2/README.md

<!-- sase:referenced-by:end -->
