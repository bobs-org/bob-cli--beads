# Bead: bob-cli-a0.6.1.1 — Synthetic demo vault and executable first-day tutorial

[Bead Pages](../README.md) / [bob-cli-a0.6.1](bob-cli-a0.6.1.md) / bob-cli-a0.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.6.md) · **Assignee:** `bob-cli-a0.6.1.1` · **Size:** medium
**Created:** 2026-10-19 23:17:16 EDT · **Closed:** 2026-10-19 23:47:09 EDT
**Plan:** [202610/learn\_path.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/learn_path.md)

## Description

tutorial: build the date-independent demo vault and isolated Bash-fence runner, write the checkpointed first-day tutorial and its hub, and install the tutorial command, recipe, tests, and docs-check gate.

## Notes

[2026-10-20T03:47:01Z · bob-cli-a0.6.1.1--3] Verified: cargo build --locked --bin bob; just docs-tutorial; the full documentation tests included in just docs-check; and just docs-check. The second-date replay also passed with now=2026-10-21T09:02:00 (exit 0). Resolved tutorial executable: /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws18-261019_233858/debug/bob. No --epic-symbol entries for bob-cli-a0.6.1.1. reported no entries.

[2026-10-20T03:47:09Z · bob-cli-a0.6.1.1--3] Completed and verified the tutorial implementation: cargo build --locked --bin bob, just docs-tutorial, full documentation tests via just docs-check, and just docs-check passed; second-date replay passed using /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws18-261019_233858/debug/bob. No epic-symbol entries remained.

## Dependencies

- **Blocks:** [bob-cli-a0.6.1.2](bob-cli-a0.6.1.2.md) ○ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.6.1.1.md) | [bob-cli-a0.6.1.1](bob-cli-a0.6.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.6.1.1--3][1] | Check existing epic notes and scope before recording replay verification and closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.6.1.1.md

<!-- sase:referenced-by:end -->
