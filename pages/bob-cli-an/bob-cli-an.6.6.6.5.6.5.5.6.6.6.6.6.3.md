# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3 — Diagnose the capture ref-jobs kick timing flake

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3` · **Size:** large
**Created:** 2026-10-26 10:47:09 EDT · **Closed:** 2026-10-26 11:34:32 EDT
**Plan:** [202610/backlog\_batch13\_vault\_integrity\_and\_perf\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch13_vault_integrity_and_perf_1.md)

## Description

capture-kick-flake: resolve bob-cli-5o by capturing the failure mode under full-suite load and fixing the demonstrated cause without blindly widening the timeout.

## Notes

[2026-10-26T14:58:11Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3] Planning evidence at 92706cb4: no prior phase notes or implementation to resume. Source shows queued_files concatenates pending and running paths, while spool::move_job installs running before removing pending, so one job can be counted twice; this is a concrete candidate, not a reproduced historical panic. kick already redirects stdio and calls setsid. Authored and validated a medium tale requiring full-load diagnostics, controlled queue-overlap reproduction, a narrow evidence-backed fix, retained under-10-second timing guard, and just check. No implementation changes or test executions yet; target bob-cli-5o remains for the parent lander. Plan proposal handoff follows.

[2026-10-26T15:34:05Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3--2] Verification update (2026-10-26):

Baseline SHA: 92706cb456ecb16286430ff7e859b698d920b261. Before the test-only change, the focused `capture_with_kick_returns_before_the_clip_finishes` test passed (1 passed, 0 failed; test harness 0.03s), and `cargo test --test cli -- --test-threads=64` passed (2,207 passed, 0 failed; 18.75s). The originally reported historical panic was not reproduced, so no historical failing assertion was recovered. The baseline monitor ran the focused and full-suite cargo commands sequentially; no concurrent build overlap was scheduled or observed. Baseline monitor `y96gap9fg4xx`, ToolRun `9da7bfe6ef7856ddaff3f0ec86192a6c` (exit 0; 159.864s total).

Controlled reproduction confirmed the candidate observation race: `move_job` installs the claimed job in `running/` before removing its `pending/` copy. The new `queued_job_ids_deduplicate_a_claim_overlap_and_keep_extra_jobs` fixture puts one identity in both locations: the former physical-path count sees 2, while identity counting sees exactly 1; adding a different identity keeps both. This demonstrates the counting defect under the valid transition, separate from the unrecovered historical panic.

Implementation is confined to `tests/cli/capture/ref.rs`: count distinct job filename stems and assert the set is exactly the ID returned in capture JSON. The real kick, queued placement assertion, 20-second fake clip, and existing under-10-second return guard remain. No production or CLI/JSON behavior changed.

Final verification monitor `np31h05s992f`, ToolRun `bdeb67b84979bec4c6f69d6d3c164f41` (exit 0; 300.910s total): controlled overlap regression 1/1 passed; ref-jobs tests 22/22 passed (7.89s); full CLI suite at 64 threads 2,208/2,208 passed (19.63s), including the capture reference integration tests; `just check` exited 0. The test retains the under-10-second assertion; the successful capture test does not print a separate child-process elapsed value. The monitor reported no remaining slow adapter workers, and a post-monitor process scan found no capture/slow-clip workers. `git diff --check` passed.

The monitor scripts captured full per-command logs under their printed temporary CARGO_TARGET_DIRs, but those temporary directories were no longer present after the monitors completed. I reviewed the retained monitor outputs, status lines, test summaries, and tails; no failure or panic appears in the retained evidence.

[2026-10-26T15:34:32Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3--2] Controlled pending/running identity overlap reproduced and fixed in the capture test by asserting the exact queued ID; real kick, 20-second clip, and under-10-second guard retained. Historical panic not recovered. Final checks passed: overlap 1/1, ref-jobs 22/22, 64-thread CLI suite 2,208/2,208, and just check; no leftover workers. Evidence: phase note #2 and monitors y96gap9fg4xx / np31h05s992f.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6a470eb`](https://github.com/bobs-org/bob-cli/commit/6a470ebe96ee31547264db373434042dc545e02e) | test(capture): deduplicate claimed ref jobs in kick test | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3.md) | 2026-10-26 11:35:14 EDT |
