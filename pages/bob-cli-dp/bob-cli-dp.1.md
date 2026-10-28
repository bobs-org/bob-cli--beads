# Bead: bob-cli-dp.1 — Provision the isolated plans sidecar for external SASE validation

[Bead Pages](../README.md) / [bob-cli-dp](README.md) / bob-cli-dp.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-df.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-df.land.md) · **Assignee:** `bob-cli-dp.1` · **Size:** large
**Created:** 2026-10-28 11:23:29 EDT · **Closed:** 2026-10-28 14:10:37 EDT
**Plan:** [202610/backlog\_batch\_b5.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b5.md)

## Description

external-plans-sidecar: resolve bob-cli-dg in sase by fixing external-checkout plan-links validation (invalid-root for sase/repos/plans). Provision the correct isolated sidecars via sase repo open or validate against an explicitly resolved read context; never silence validation or read another workspace. Verify with sase validate in a clean external checkout and the governed sase tool run check. Use sase validate or sase plan links validate, not the shorthand sase validate plan-links.

## Notes

[2026-10-28T18:10:29Z · bob-cli-dp.1] Implemented plan:202610/external_sidecar_validation.md in the sase repo.

Part A: `sase repo open` of a registered project now clones that project's own plans sidecar into `<external>/sase/repos/plans` and writes a checkout-local `.sase/sdd-store.json` after the clone succeeds. Matching existing clones are left unsynchronized. Provisioning failures warn on stderr and still print the opened path.

Part B: `sase.sdd._link_files._resolve_project_sdd_root` resolves a nested repo-open clone (`sase/repos/external/…` or `sase/repos/linked/…`) from its own materialized store record via a checkout-local primary resolver. Unprovisioned nested clones keep `invalid-root` with a `sase repo open` remedy.

Tests (sase tool run test):
- d59a72e9cf978868ca4eca94f2f3f1fe — tests/main/test_repo_open_external_plans_sidecar.py + tests/sdd_store/test_nested_repo_open_sdd_root.py succeeded
- 1692e75ba42d4843680e5a818c1aeb8c — repo open help assertion succeeded

Real-checkout acceptance from bob-cli_10 with `<external>/.venv/bin/sase`:
- Baseline: `sase plan links validate` reported invalid-root for `<external>/sase/repos/plans` plus the new remedy.
- `sase repo open sase -r "Provision plans sidecar for nested validation"` cloned `git@github.com:sase-org/sase--plans.git` at HEAD `33556e1b7` and wrote the checkout-local sidecar record.
- `.venv/bin/sase validate`: every stage ok (plan links validate included).
- `.venv/bin/sase plan links validate`: 5589 files, 12 warnings, exit 0 from the checkout root and from `src/`.
- `git status --porcelain` showed only the intended sase source/docs/test edits.

Governed check:
- install-venv 72adc48dcd44af08e40f07eeeb4f9178 succeeded (cached venv).
- check 3dcb9a523539b3e82791f3827cff0072: fmt/ruff/mypy/docs/SASE validation passed; committed-plans UNKNOWN because this bob-cli agent exports `SASE_SDD_PLANS_DIR` to the host bob-cli plans store (909 files). Unsetting that env, `python -m sase.scripts.validate_committed_plans` from the nested checkout passed 5589 sase plans, 0 errors.
- check f0968a143d1d4da7462612bb0baf40c8 with `SASE_SDD_PLANS_DIR` pointed at the nested plans: committed-plans 8.1s pass, docs pass, scoped tests 3861 passed / 87 failed. Failures are the published `sase-core-rs==0.42.7` wheel missing 31 bindings (`bead_close` arity, `footprint_wire_schema_version`, `artifact_link_quarantine_record_validate`). Core-floor probe skipped the same gap. Related beads: bob-cli-dp.3, bob-cli-df.4.1.

PROPOSED FOLLOW-UP: tier-3 SASE-managed externals — `gh:owner/repo` opens still skip plans-sidecar provisioning because they have no registered primary record.

PROPOSED FOLLOW-UP: nested store-resolution vs owner-anchor — default `resolve_sdd_store` still inherits the host marker for nested clones; only link validation uses the checkout-local record. Bead/plan writes inside an external checkout remain host-scoped by design.

PROPOSED FOLLOW-UP: agent `SASE_SDD_PLANS_DIR` leaks into nested-checkout `just validate-committed-plans` — a bob-cli agent running `sase tool run check` inside an external sase checkout validates host plans unless that env is unset or retargeted.

PROPOSED FOLLOW-UP: external sase checkout venv ships stale `sase-core-rs==0.42.7` when `../sase-core` is absent — scoped check failures on bead_close/footprint/artifact-link bindings reproduce from that wheel. See bob-cli-dp.3 and bob-cli-df.4.1.

[2026-10-28T18:10:37Z · bob-cli-dp.1] Verified nested plans-sidecar provisioning: focused tests d59a72e9cf978868ca4eca94f2f3f1fe, real-checkout `.venv/bin/sase validate` and `sase plan links validate` against sase-org/sase--plans (5589 files), checkout porcelain limited to intended source edits. Remaining sase check NEW/UNKNOWN items are the host `SASE_SDD_PLANS_DIR` leak and stale sase-core-rs 0.42.7 bindings; recorded as PROPOSED FOLLOW-UP on this phase.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-dp.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-dp.1.md) | [bob-cli-dp.1](bob-cli-dp.1.md) | 0 |
