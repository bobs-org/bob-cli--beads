# Bead: bob-cli-kd.4 — Weekly QFX import that writes only what you missed

[Bead Pages](../README.md) / [bob-cli-kd](README.md) / bob-cli-kd.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1be](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1be.md) · **Assignee:** `bob-cli-kd.4` · **Size:** large
**Created:** 2026-11-11 11:24:16 EST
**Plan:** [202611/bank\_daily\_acknowledgment.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_daily_acknowledgment.md)

## Description

bank-import: parse Wells Fargo QFX (OFX 1.x SGML and 2.x XML) plus one CSV profile; resolve accounts without numbers; journal hashed identities per host; match typed rows; name rows from rules, learned payees, and restaurant records; write unchecked rows in one guarded, committed transaction with an exact dry run; add the weekly PRE chore.

## Notes

[2026-11-12T02:52:37Z · bob-cli-kd.4.1.land] Closeout blocker from child kd.4.1: source, planner, importer, transaction, and docs repairs are implemented, but approved landing plan also requires the narrow live vault .gitignore allowlist and .gitattributes union rule. No supported SASE inventory entry brokers the live Bob vault repository, so the policy edit and check-ignore/check-attr verification cannot be performed without bypassing repo access rules. Child note records the fresh test/docs results and exact blocker. Leave kd.4.1 and this phase open until that vault setup is verified; do not close the phase.

[2026-11-12T03:07:34Z · bob-cli-kd.4.1.land--1] REQUIRED GATE RESULT: monitored `just check` (ToolRun 5a7d51346f33f6981050349b553e722d; monitor afdtjmdcq2b4) failed, exit 101, started 2026-11-12T02:53:05.505430-05:00, finished 2026-11-12T03:00:06.858520Z, elapsed 6m 5s. Two failures are outside the bank-import diff: `bob-obsidian --lib` 6693 passed / 1 failed / 3 ignored in 30.01s, `native::subprocess_runner::tests::run_bounds_pipe_drain_when_detached_grandchild_holds_output` at `src/native/subprocess_runner.rs:462` (missing `output truncated` marker); `bob-obsidian --test cli` 3603 passed / 1 failed in 84.34s, `capture::complete_themes::configured_shell_describes_never_used_and_unconfigured_create` at `tests/cli/capture/complete_themes.rs:308` (expected `your type · never used`, got empty stdout). Neither failed file is modified in this landing. The theme completion test deadline omission was already recorded in child triage, so the gate failure is unrelated to this implementation. Keep phase and child open while the required live Bob vault `.gitignore` allowlist and `.gitattributes` union rule remain unverified; supported SASE inventory has no brokerable vault reference, and `~/bob` must not be accessed directly.

## Dependencies

- **Depends on:** [bob-cli-kd.3](bob-cli-kd.3.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-kd.5](bob-cli-kd.5.md) ◐ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.md) | [bob-cli-kd.4](bob-cli-kd.4.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.4.1.1][1] | Need parent phase DECISIONS that remain final | 1 |
| read-by | [agent:bob-cli-kd.4.1.4][2] | Need parent epic DECISIONS for docs-ritual phase | 1 |
| read-by | [agent:bob-cli-kd.4.1.land--1][3] | Verify the just check diagnosis was appended and the phase remains open | 2 |
| read-by | [agent:research.49.cdx][4] | Separate implemented daily CLI from remaining import, proof, and UI acceptance work | 1 |
| read-by | [agent:research.49.cld][5] | research: user guide for first-time bank ack and e2e test of bob-cli-kd | 1 |
| read-by | [agent:research.49.gem][6] | Understand phase 4 import commands | 1 |
| read-by | [agent:research.49.grk][7] | Need import, balance, and Obsidian child-epic status so the first-run guide does not promise unshipped gestures | 1 |
| read-by | [agent:research.49.mus][8] | research kd epic phase scope for user guide | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.4.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.4.1.land.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cdx/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.cld/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.gem/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.grk/README.md
[8]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.49.mus/README.md

<!-- sase:referenced-by:end -->
