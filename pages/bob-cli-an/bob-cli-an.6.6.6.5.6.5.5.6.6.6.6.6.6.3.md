# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3 — Declare bob-cli's named check tool for SASE prepared completion

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3` · **Size:** medium
**Created:** 2026-10-26 12:58:46 EDT · **Closed:** 2026-10-26 13:19:00 EDT
**Plan:** [202610/backlog\_batch14\_ledger\_integrity\_mac\_ci\_and\_cleanup.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch14_ledger_integrity_mac_ci_and_cleanup.md)

## Description

check-tool-catalog: resolve bob-cli-91 by declaring a run_silent named check tool for just check in sase/sase.yml, so sase tool run check and prepared completion work on this Rust project.

## Notes

[2026-10-26T17:18:38Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3] check-tool-catalog done: declared tools.check (argv [just, check], stages run_silent, args deny, inputs justfile/Cargo/clippy/rustfmt/toolchain, just/cargo/rustc toolchain fingerprints) in sase/sase.yml. Evidence: sase tool list shows check/short; sase tool run check executed the gate (run 29c43e463aa136ae4afa06a5a096e9e2, exit 101) failing ONLY on the 4 known cc-owned tests (catalog public_leaves, completion every_value_arg, help ref_help snapshot, source_store doctor) recorded in the batch-14 plan as pre-existing on the unchanged tree — YAML-only change, no Rust reads sase.yml. _resolve_stage_source([just,check])=run_silent (uncatalogued argv gives none), so prepare seals instead of refusing. No AGENTS/CLAUDE/docs check-runner guidance exists to update. Target bob-cli-91 left open for the lander.

[2026-10-26T17:19:00Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3] Declared tools.check in sase/sase.yml (argv just check, stages run_silent, args deny). Verified: sase tool list shows check; sase tool run check runs the gate and fails only on the 4 pre-existing cc-owned tests documented in the batch-14 plan (YAML-only change, no Rust reads sase.yml); prepare stage_source resolves to run_silent so the prepared-completion path accepts just check. epic-symbols clean. Target bob-cli-91 left open for the lander.

[2026-10-26T17:19:22Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3] BASE-TREE EVIDENCE: stashed sase/sase.yml and reran exactly the 4 failing tests on the clean tree — all 4 fail identically (3 lib + help::ref_help snapshot), exit 101. The just-check failure is pre-existing cc-owned breakage, outside this bead scope per the close policy. Stash popped; tree holds only the sase/sase.yml catalog change.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d7b87d4`](https://github.com/bobs-org/bob-cli/commit/d7b87d41ee563bdc3c0978339065b15ff8b01c5a) | feat(sase): declare named check tool for prepared completion | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3.md) | 2026-10-26 13:20:21 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3][1] | need note numbers to fix garbled note | 2 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
