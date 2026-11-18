# Bead: bob-cli-my.4 — Require corroboration before quarantining a foreign-note clobber

[Bead Pages](../README.md) / [bob-cli-my](README.md) / bob-cli-my.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-mr.land--2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-mr.land.md) · **Assignee:** `bob-cli-my.4` · **Size:** medium
**Created:** 2026-11-17 19:17:52 EST · **Closed:** 2026-11-17 21:59:08 EST
**Plan:** [202611/backlog\_triage\_t2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/backlog_triage_t2.md)

## Description

clobber-evidence: require evidence beyond a shared created timestamp before quarantine and close bob-cli-l0.

## Notes

[2026-11-18T02:59:08Z · bob-cli-my.4] Required created-time corroboration in vault clobber matching; created-only minute/second matches reject, while created plus one shared task ID, standalone ^prj, and three shared IDs remain covered. Verified with cargo test --lib native::vault_clobber (11 passed), the shared-created scratch-vault integration test (1 passed), cargo test --test cli clobber (5 passed), and sase tool run check (succeeded).

## Dependencies

- **Depends on:** [bob-cli-my.3](bob-cli-my.3.md) ✓ · ⧖ 2026-11-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-my.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-my.4/README.md) | [bob-cli-my.4](bob-cli-my.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2f14eef`](https://github.com/bobs-org/bob-cli/commit/2f14eef5dcbdcd46151ae9b87fb94ac4784496c9) | fix(vault-sync): corroborate created-time identity matches | [bob-cli-my.4](bob-cli-my.4.md) | 2026-11-17 22:00:47 EST |
