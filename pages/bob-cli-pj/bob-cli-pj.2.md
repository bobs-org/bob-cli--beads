# Bead: bob-cli-pj.2 — Invalidate only the plans an edit affects

[Bead Pages](../README.md) / [bob-cli-pj](README.md) / bob-cli-pj.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1fa.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1fa.1.md) · **Assignee:** `bob-cli-pj.2` · **Size:** large
**Created:** 2026-11-22 18:00:45 EST · **Closed:** 2026-11-22 21:59:35 EST
**Plan:** [202611/tick\_contention\_noise.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/tick_contention_noise.md)

## Description

refs-incremental-coherence: classify scan snapshot mismatches by owner, re-plan only affected PDFs then re-run finalization in a bounded refresh at all three stale sites, keep global and fail-closed paths, and extend the interleave tests.

## Notes

[2026-11-23T02:11:41Z · bob-cli-pj.2.1.land] LAND BLOCKER from bob-cli-pj.2.1: child phases are closed, but landing source review found nonconverged no-work returns in the lock refresh branch and incorrect replacement dependency/ownership evidence. The child epic stays open. A validated medium repair tale will finish these issues, add the required interleave coverage, run just check and docs-check, then close bob-cli-pj.2.1 and this phase normally in its coding turn. Outer epic bob-cli-pj remains with its waiting land agent. Docs baseline failures have been triaged to on.15.1 plus jz/h9, and plugin API headroom to ob; see child landing notes for all evidence.

[2026-11-23T03:00:38Z · bob-cli-pj.2.1.land] LAND VERIFICATION (phase close): refs-incremental-coherence satisfies three-site convergence (prepare_from_inputs via settle, prepare_full_scan_with_retry via settle, lock_validate via settle), dependency-aware classification (vault-link/lineage/parent/incomplete union, per-PDF owners, candidate vectors, index rest fingerprint), shared budget (initial + 4 subsets + 1 rebuild, combined prep+lock test 6 lines inputs_changed, prep 6 success, lock 6 inputs_changed), safety (dest scan_failed locked receipt preserved, prelock failures without receipt, no retry after intake move, collision validation, ref_dir global rule, pinned date, hooks once). Verification: cargo fmt clean; scan_plan 31 passed; interleave 11 focused passed; sase tool run check exit 0 run 9d1be27cee08c4bf935c9c3a581e780c; docs-check baseline-only failures (6082/6036/6107/8963). Drift: origin/master +2 docs-only commits ef640fde/bf005290, no scan impact. Epic-symbols empty. Outer epic bob-cli-pj left to waiting land agent.

## Dependencies

- **Depends on:** [bob-cli-pj.1](bob-cli-pj.1.md) ✓ · ⧖ 2026-11-22

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-pj.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-pj.2.md) | [bob-cli-pj.2](bob-cli-pj.2.md) | 0 |
