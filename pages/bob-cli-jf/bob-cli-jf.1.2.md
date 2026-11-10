# Bead: bob-cli-jf.1.2 — SASE refuses Git mutations outside a linked checkout's own worktree

[Bead Pages](../README.md) / [bob-cli-jf.1](bob-cli-jf.1.md) / bob-cli-jf.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-jf](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-jf.md) · **Assignee:** `bob-cli-jf.1.2` · **Size:** medium
**Created:** 2026-11-10 06:47:59 EST · **Closed:** 2026-11-10 07:36:59 EST
**Plan:** [202611/bob\_mac\_capture\_history\_restore.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_mac_capture_history_restore.md)

## Description

guard: in the sase repo, make linked and sidecar materialization verify that a reused path is a Git worktree rooted at itself before any origin rewrite, fetch, merge, or exclude write, and make the push path refuse a checkout whose toplevel or origin is not the one SASE expects, with regression tests.

## Notes

[2026-11-10T12:08:16Z · bob-cli-jf.1.2] PROPOSED FOLLOW-UP: External repo reuse can accept its enclosing host checkout — src/sase/main/repo_open_external.py::_is_valid_git_repo uses rev-parse --is-inside-work-tree without a ceiling or root comparison. A local git-init host with an empty sase/repos/external/gh/example/child returns true for that child while show-toplevel is the host. This phase guards publication and linked/sidecar materialization; migrate the external-open validator to the new shared worktree-root probe as a separate follow-up.

[2026-11-10T12:17:32Z · bob-cli-jf.1.2] Implementation is complete in the opened sase repository: bounded realpath worktree probe; empty invalid directories are cloned fresh, nonempty paths are preserved with an actionable error; linked/sidecar origin rewrites, refresh, excludes and SDD setup are guarded; nested clones do not inherit host identity markers; bare sidecars now verify an explicit Git directory; shared Git pushes and bare submit validate expected origin and every push URL, accepting equivalent transports and refusing retries on identity errors. All 99 focused real-repository/reuse/heal/cutover/provider tests pass. Required check ToolRun 1ff97e7d77df29ca1443b8d36fbfb1d8 has passed all lint/validation stages and is running its automatically expanded full test lane. The final small bare-sidecar change additionally passes targeted Ruff/mypy and is included in the running test selection. Remaining work is verification results and phase close/final declaration, which fits one follow-up coder if the check hands off. No epic-symbol entries remain. Test environment uses the published 0.44.2 core wheel via SASE_CORE_WHEEL because the pinned 0.43.2 wheel lacks required bindings; no Rust source or memory changes.

[2026-11-10T12:36:23Z · bob-cli-jf.1.2] PROPOSED FOLLOW-UP: Full-suite agent-state tests fail intermittently — ToolRun 1ff97e7d77df29ca1443b8d36fbfb1d8 failed test_normal_dismiss_reconciles_unloaded_agent_session_members_after_root_delete (two dismissed timestamps remained visible) and test_production_paths_keep_parity_with_marker_only_population (49 missing production rows). Both pass when rerun with unchanged production code and also pass on clean base bd97664e07f78922f4f9803cb5688ba0b425f6fd in an isolated worktree using the same core 0.44.2 wheel. Investigate suite-order or shared-state sensitivity; no owner was identified by ToolRun triage.

[2026-11-10T12:36:28Z · bob-cli-jf.1.2] PROPOSED FOLLOW-UP: Publication-output test fails for long checkout paths — tests/test_commit_workflow_publication_outcomes.py::test_publication_without_target_warns_but_keeps_primary_successful failed identically at line 308 on both this guard tree and clean base bd97664e07f78922f4f9803cb5688ba0b425f6fd using the same test environment; Rich wraps the repository path, so the whitespace-normalized captured output does not contain the original contiguous path. Recorded by check ToolRun 1ff97e7d77df29ca1443b8d36fbfb1d8; no existing owner was identified by triage. This unrelated baseline assertion does not block the guard phase.

[2026-11-10T12:36:59Z · bob-cli-jf.1.2] Implemented checkout-root and expected-origin guards in the opened sase repo. Real local Git regressions verify nested non-checkouts cannot alter host origin, refs, or excludes; empty targets clone cleanly; nonempty targets are preserved; valid reuse, origin healing, sidecar cutover, worktree gitfiles and equivalent URL transports remain supported; wrong-origin/pushurl publication and retry are refused. Final focused verification: 117 passed in 9.46s; Ruff, format and diff checks pass. Required check ToolRun 1ff97e7d77df29ca1443b8d36fbfb1d8 passed whole-repo lint/validation and ran the full suite (16510 passed, 8 failed, 8 skipped): fixed all five affected mock failures and reran their modules successfully; two intermittent agent-state failures pass on rerun and clean base, and the publication-output failure reproduces on clean base bd97664e07. Those verification issues and the external-open validator discovery are recorded as PROPOSED FOLLOW-UP notes. No epic-symbol entries remain. No ancestor bead closed; no memory or Rust source changes.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-jf.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-jf.1.2/README.md) | [bob-cli-jf.1.2](bob-cli-jf.1.2.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-jf.1.2][1] | Confirm completion criteria and record final verification evidence | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-jf.1.2/README.md

<!-- sase:referenced-by:end -->
