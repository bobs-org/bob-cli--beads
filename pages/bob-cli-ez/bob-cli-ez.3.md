# Bead: bob-cli-ez.3 — bob gkeep status with bob-owned check gates

[Bead Pages](../README.md) / [bob-cli-ez](README.md) / bob-cli-ez.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.2y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2y.linker.w0.md) · **Assignee:** `bob-cli-ez.3` · **Size:** medium
**Created:** 2026-10-31 13:32:41 EDT · **Closed:** 2026-10-31 15:37:22 EDT
**Plan:** [202610/gkeep\_footer\_indicator.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gkeep_footer_indicator.md)

## Description

keep-status-command: add `bob gkeep status [-b] [-f] [-m] [-r]`, the never-prompting token read, freshness/floor/single-flight/busy/budget/backoff gates, gkeep.check_interval, the JSON and human output, the catalog row and gkeep invalidation tag, and docs.

## Notes

[2026-10-31T19:37:05Z · bob-cli-ez.3] PROPOSED FOLLOW-UP: decision_record skipped (auto decision no) — add a decisions-web record "Keep Count Is bob-Owned And Attention-Gated" (bob decides when to contact Google Keep and caches host-locally; clients run bob gkeep status [-r], never poll on a timer, never read the token) if Bryan wants it; bob-cli-ez.3 shipped the status command, gates, cache reads, and gkeep.check_interval it would govern.

[2026-10-31T19:37:22Z · bob-cli-ez.3] Added bob gkeep status [-b -f -m -r]: cache-only default (no token/adapter/network/ledger scan), -r with ordered gates (unconfigured, auth, busy, in_flight, 60s floor, backoff, off/fresh, 48/day budget; -m 0 forces), never-prompting 10s token read (stdin null, GPG_TTY removed, pinentry-mode error), 30s adapter deadline, gkeep.check_interval (default 30m, 5m-24h or off/false), human + schema_version 1 JSON output, lockless cache reads plus begin_check budget/floor writer, locked failure state, pull lock 2s WouldBlock retry, gkeep-status catalog row + gkeep invalidation tag on list/pull/doctor/status, completion decision for --max-age, docs (gkeep.md Status section, json-outputs, configuration) with just docs-gen and docs-check green. Verified: cargo fmt --check, just lint (exit 0), full cargo test --workspace (all pass incl. 26 new tests/gkeep_status.rs integration tests with fake adapter, gate/backoff/next_check_at unit tests, config/token tests, pull-lock retry test). No live Keep contact. Decision record skipped per auto decision; recorded as PROPOSED FOLLOW-UP.

## Dependencies

- **Depends on:** [bob-cli-ez.1](bob-cli-ez.1.md) ✓ · ⧖ 2026-10-31
- **Depends on:** [bob-cli-ez.2](bob-cli-ez.2.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ez.5](bob-cli-ez.5.md) ✓ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ez.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ez.3/README.md) | [bob-cli-ez.3](bob-cli-ez.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`efe2ebe`](https://github.com/bobs-org/bob-cli/commit/efe2ebe066d0df87736b8af2eeef52e152bf5e3e) | feat(gkeep): add bob gkeep status with bob-owned check gates | [bob-cli-ez.3](bob-cli-ez.3.md) | 2026-10-31 15:38:28 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ez.3][1] | notes check | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ez.3/README.md

<!-- sase:referenced-by:end -->
