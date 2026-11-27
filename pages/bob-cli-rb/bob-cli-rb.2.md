# Bead: bob-cli-rb.2 — bob-cli task\_type candidates carry an optional lead

[Bead Pages](../README.md) / [bob-cli-rb](README.md) / bob-cli-rb.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hh.md) · **Assignee:** `bob-cli-rb.2` · **Size:** medium
**Created:** 2026-11-27 15:03:21 EST · **Closed:** 2026-11-27 17:17:05 EST
**Plan:** [202611/capture\_type\_leads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_type_leads.md)

## Description

lead_complete: compute the optional `lead` object on editor `task_type` candidates behind Bob's eligibility gates and one parser probe, keep shell completion and every write path lead-free, render it in human output, and document the contract.

## Notes

[2026-11-27T22:17:05Z · bob-cli-rb.2] lead_complete done: editor task_type candidates carry optional lead {text, insert_at, insertion, cursor_after} behind eligibility gates + D0/D1 parser probe (mode Task, no Directive span, task_type span, no new diagnostics, body check) with route-aware policies; shell/write paths lead-free; human rows show · types "Fix"; docs in capture.md + json-outputs.md. Verified: just check EXIT=0, just docs-check EXIT=0, 11 new CLI tests in complete_task_types.rs green. Also fixed two blocking rb.1 defects found red on this tree: loader probe compared the trailing probe body to <text> instead of <text> x (no lead could ever load), and 4 loader unit tests used backslash-continuations that stripped YAML nesting (plus NULL key parses as YAML null, renamed to SKIP).

## Dependencies

- **Depends on:** [bob-cli-rb.1](bob-cli-rb.1.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-rb.3](bob-cli-rb.3.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rb.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rb.2/README.md) | [bob-cli-rb.2](bob-cli-rb.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`bd6a5fe`](https://github.com/bobs-org/bob-cli/commit/bd6a5fe5d6a9976a5f638d371b092a29e1f5faec) | feat(capture): task\_type lead completion with eligibility gates and parser probe | [bob-cli-rb.2](bob-cli-rb.2.md) | 2026-11-27 17:18:25 EST |
| bob-plugins | `bob-plugins@bd6a5fe` | feat(capture): task\_type lead completion with eligibility gates and parser probe | [bob-cli-rb.2](bob-cli-rb.2.md) | 2026-11-27 17:18:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-rb.2][1] | Need phase notes and remaining work | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-rb.2/README.md

<!-- sase:referenced-by:end -->
