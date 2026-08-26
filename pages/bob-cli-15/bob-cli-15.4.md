# Bead: bob-cli-15.4 — Rust and agent-workspace build artifacts

[Bead Pages](../README.md) / [bob-cli-15](README.md) / bob-cli-15.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0dy](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.0dy/README.md) · **Assignee:** `bob-cli-15.4` · **Size:** medium
**Created:** 2026-08-26 08:19:52 EDT · **Closed:** 2026-08-26 08:48:53 EDT
**Plan:** [202608/disk\_space\_reclamation.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/disk_space_reclamation.md)

## Description

buildart: prune the 125G sase-core target directory and the per-workspace Rust target copies under ~/.local/state/sase/workspaces, then redirect future builds to a single shared, size-capped location.

## Notes

[2026-08-26T12:48:41Z · bob-cli-15.4] PROPOSED FOLLOW-UP: ~31G of Rust target/ build output remains in currently-live workspaces that this phase deliberately left alone to avoid disrupting active agents: bob-cli primary checkout target (4.4G, 4 occupant agents), bob-cli_10-13 workspace targets (12G/5.7G/3.2G/2.1G), and 5 live sase_org workspace targets (sase_19/20/23/26/27, ~755M each). Once those agents finish, the same rm-of-orphaned-target approach used here should be repeated for them. Also still open from the buildart phase design: a periodic cargo-sweep-style job to auto-prune target/ dirs untouched for 30 days (may belong in the guardrails phase bob-cli-15.7 alongside its other scheduled cleanups), and an optional sccache evaluation for cross-checkout artifact reuse.

[2026-08-26T12:48:53Z · bob-cli-15.4] Verified sase-core/target (125G) already removed and ~/.cargo/config.toml already redirects target-dir to /mnt/poseidon/cargo-target (both done prior to this turn). This turn: identified 16 per-workspace sase-core/target copies plus zorg and actstat target dirs (18 total, ~30G) belonging to unclaimed/dead-PID workspaces with no running cargo/rustc process; proposed the exact rm list via /sase_gate, user approved, deleted all 18 (confirmed gone), df / went from 63% to 59% used (avail 327G -> 355G). Left target/ in currently-claimed/live workspaces (bob-cli primary + bob-cli_10-13, sase_19/20/23/26/27, ~31G) untouched to avoid disrupting active agents; recorded as PROPOSED FOLLOW-UP along with the still-open cargo-sweep cron job and sccache consideration.

## Dependencies

- **Blocks:** [bob-cli-15.7](bob-cli-15.7.md) ✓ · ⧖ 2026-08-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-15.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-15.4/README.md) | [bob-cli-15.4](bob-cli-15.4.md) | 0 |
