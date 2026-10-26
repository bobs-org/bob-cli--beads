# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3 — Diagnose the capture ref-jobs kick timing flake

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3` · **Size:** large
**Created:** 2026-10-26 10:47:09 EDT
**Plan:** [202610/backlog\_batch13\_vault\_integrity\_and\_perf\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch13_vault_integrity_and_perf_1.md)

## Description

capture-kick-flake: resolve bob-cli-5o by capturing the failure mode under full-suite load and fixing the demonstrated cause without blindly widening the timeout.

## Notes

[2026-10-26T14:58:11Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3] Planning evidence at 92706cb4: no prior phase notes or implementation to resume. Source shows queued_files concatenates pending and running paths, while spool::move_job installs running before removing pending, so one job can be counted twice; this is a concrete candidate, not a reproduced historical panic. kick already redirects stdio and calls setsid. Authored and validated a medium tale requiring full-load diagnostics, controlled queue-overlap reproduction, a narrow evidence-backed fix, retained under-10-second timing guard, and just check. No implementation changes or test executions yet; target bob-cli-5o remains for the parent lander. Plan proposal handoff follows.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.3.md) | 0 |
