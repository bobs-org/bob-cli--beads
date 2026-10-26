# Bead: bob-cli-cc.6 — Verified attach of existing references' sources

[Bead Pages](../README.md) / [bob-cli-cc](README.md) / bob-cli-cc.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5b.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5b.linker.w0.md) · **Assignee:** `bob-cli-cc.6` · **Size:** medium
**Created:** 2026-10-26 09:00:56 EDT · **Closed:** 2026-10-26 13:13:11 EDT
**Plan:** [202610/ref\_code\_block\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_code_block_copy.md)

## Description

attach: add bob ref attach-source, which finds same-stem Markdown candidates, verifies them against the library PDF text, and attaches only verified sources; then dry-run and run it on athena per the backfill decision.

## Notes

[2026-10-26T17:12:47Z · bob-cli-cc.6] attach-source backfill run on athena (backfill=run): dry-run 235 attached / 297 skipped; write pass committed 3 batches fdd325a2 (100 refs), 63ab5a58 (100 refs), 86f99f12 (35 refs) — all present under later vault-sync merges, tree clean. Candidate coverage 431/487 agent-report-eligible refs (~89%, research expected ~429/473); verify rate 235/349 compared (67%, gate is 60%). Skips by design: 100 no candidate (blogs/papers/sidecar-missing), 47 ambiguous (plan-vs-report stem collision in sase research sidecar), 35 title mismatch (renamed reports), 115 low match (edited sources). Spot-checked 10 refs via bob ref code JSON (8 available, 2 no_code paragraph-fallbacks, all route=attached); page labels verified against pdftotext for agent_image_generation_toolset (5/5 pages) and agent_history_in_agents_tab; raw block bytes byte-verbatim in source.md. Search roots: bob-cli, sase, actstat, tailnet research sidecars (canonical clones; cross-project sase repo open -p fails with no WORKSPACE_DIR, reads used local checkouts, no network fetch). Vault NOT pushed: batches are local commits for the normal vault-sync flow to distribute.

[2026-10-26T17:12:56Z · bob-cli-cc.6] PROPOSED FOLLOW-UP: code-cmd phase left two lib-test gaps that fail identically on the clean base tree: completion::kinds::every_value_arg_has_a_decision wants kinds decisions for ref code:number and ref code:page, and catalog::public_leaves_are_entries_or_excluded fails the same way. Small, in code-cmd scope.

[2026-10-26T17:13:00Z · bob-cli-cc.6] PROPOSED FOLLOW-UP: just docs-check fails identically on the clean base tree: bob-docs lint flags undocumented BOB_TEST_FIXTURE_PDF in source_store.rs. Needs a configuration.md entry or a reasoned exception. Unrelated to attach.

[2026-10-26T17:13:03Z · bob-cli-cc.6] PROPOSED FOLLOW-UP: 47 ambiguous stems (plan-vs-report collisions inside the sase research sidecar, e.g. sase/repos/plans/202608/X.md vs 202608/X/X.md) and 35 title-mismatched reports need human disambiguation or explicit file invocation (bob ref attach-source REF -s FILE) in a follow-up pass.

[2026-10-26T17:13:11Z · bob-cli-cc.6] bob ref attach-source shipped with tests+docs; dry-run then write pass on athena attached 235 refs in 3 revertable batch commits (fdd325a2, 63ab5a58, 86f99f12); 67% of compared candidates verify (gate 60%), all skip reasons by design; 10 refs spot-checked via bob ref code with page labels confirmed against pdftotext; fmt+clippy clean, 294 focused integration tests and full cli suite green (2227 passed); 2 lib-test gaps and the docs-check env lint fail identically on base and are recorded as follow-ups

## Dependencies

- **Depends on:** [bob-cli-cc.3](bob-cli-cc.3.md) ✓ · ⧖ 2026-10-26
- **Depends on:** [bob-cli-cc.4](bob-cli-cc.4.md) ✓ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-cc.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-cc.6/README.md) | [bob-cli-cc.6](bob-cli-cc.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`36ae0ef`](https://github.com/bobs-org/bob-cli/commit/36ae0ef0ae4fe4fd49b6916eb04431a2738f4eab) | feat(ref): add bob ref attach-source with text-verified sources | [bob-cli-cc.6](bob-cli-cc.6.md) | 2026-10-26 13:14:49 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land][1] | Check whether ref code/source_store test failures are already recorded | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
