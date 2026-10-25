# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.4 — Tolerate a closed child stdin in the gkeep login test helper

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.4` · **Size:** small
**Created:** 2026-10-25 11:34:35 EDT · **Closed:** 2026-10-25 11:48:23 EDT
**Plan:** [202610/backlog\_batch11\_ref\_repair\_taskcard\_popout\_gkeep\_again.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch11_ref_repair_taskcard_popout_gkeep_again.md)

## Description

gkeep-stdin-epipe: resolve bob-cli-2m by making tests/gkeep_auth.rs run_login (and any sibling stdin-writing gkeep helper) tolerate BrokenPipe while keeping the exit-code, hint, and no-call assertions.

## Notes

[2026-10-25T15:48:23Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.4] run_login (tests/gkeep_auth.rs) plus sibling stdin writers run_fake (tests/gkeep_adapter.rs) and run_pull_pty (tests/gkeep_pull.rs) now tolerate ErrorKind::BrokenPipe on the stdin write while failing on any other error; exit-code, hint, and no-call assertions unchanged. Verified: deterministic pipe probe proves closed-stdin write == BrokenPipe; login_missing_email_is_a_setup_error 50/50 sequential + 8/8 concurrent; gkeep_auth 11/11, gkeep_adapter 6/6; just check exit=0 (3423 passed, 0 failed across 18 targets). Target task bob-cli-2m left open for the lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`c8573d7`](https://github.com/bobs-org/bob-cli/commit/c8573d78f945760f13e80db5015362242511b4e7) | fix(gkeep): tolerate stdin EPIPE in test child-process helpers | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.6.4.md) | 2026-10-25 11:49:22 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.4][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.4/README.md

<!-- sase:referenced-by:end -->
