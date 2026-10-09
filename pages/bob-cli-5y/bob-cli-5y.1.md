# Bead: bob-cli-5y.1 — sase: file hooks export SASE\_FILE\_HOOK\_PROJECT

[Bead Pages](../README.md) / [bob-cli-5y](README.md) / bob-cli-5y.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0z0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0z0.md) · **Assignee:** `bob-cli-5y.1` · **Size:** small
**Created:** 2026-10-09 12:29:34 EDT · **Closed:** 2026-10-09 12:43:52 EDT
**Plan:** [202610/ref\_tasks\_live\_with\_parent.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_tasks_live_with_parent.md)

## Description

sase-hook-env: the sase file-hook runner exports the producing project's name to every hook command as an environment variable, with docs and dispatch tests.

## Notes

[2026-10-09T16:43:36Z · bob-cli-5y.1] PROPOSED FOLLOW-UP: Add decisions strand ref-tasks-live-with-their-parent recording that ref tasks live with their parent note (memory_ref_parent_decision = no, left for land agent)

[2026-10-09T16:43:40Z · bob-cli-5y.1] PROPOSED FOLLOW-UP: Update glossary reference-task, reference-note, and area-note strands for the v2 parent-residence model (memory_glossary_ref_terms = no, left for land agent)

[2026-10-09T16:43:44Z · bob-cli-5y.1] PROPOSED FOLLOW-UP: just check is red on the clean base tree too: _setup-required-plugins fails with stale sase_core_rs content-layout wire (expects schema >= 7, installed wheel provides 5) and no sase-core checkout is present to rebuild from

[2026-10-09T16:43:52Z · bob-cli-5y.1] sase file-hook runner exports SASE_FILE_HOOK_PROJECT (unset when missing/empty/unknown, inherited value removed, .get for old batches); run log gains project: line; docs in configuration.md + plugins.md; 26/26 tests/file_hook_engine pass, ruff + mypy clean; just check blocked by pre-existing stale sase_core_rs wire, identical on clean tree

## Dependencies

- **Blocks:** [bob-cli-5y.4](bob-cli-5y.4.md) ◐ · ⧖ 2026-10-09

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-5y.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.1/README.md) | [bob-cli-5y.1](bob-cli-5y.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-5y.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-5y.1/README.md

<!-- sase:referenced-by:end -->
