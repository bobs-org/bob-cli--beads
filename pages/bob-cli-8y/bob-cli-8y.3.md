# Bead: bob-cli-8y.3 — Render through the adapter on both routes

[Bead Pages](../README.md) / [bob-cli-8y](README.md) / bob-cli-8y.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4r.linker.w0.md) · **Assignee:** `bob-cli-8y.3` · **Size:** medium
**Created:** 2026-10-17 19:29:17 EDT · **Closed:** 2026-10-17 21:30:56 EDT
**Plan:** [202610/ref\_create\_mermaid\_figures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_mermaid_figures.md)

## Description

wire: add the adapter client call, orchestration that never fails the import, the results and fallback notes, the scale warnings, and the summary and warning output on the generic and snapshot routes, with stub-adapter tests and an athena smoke run.

## Notes

[2026-10-18T01:30:29Z · bob-cli-8y.3] PROPOSED FOLLOW-UP: skipped decisions-web record — epic decision_record=no, so do not edit decisions:ref-create-renders-mermaid-in-the-adapter; land agent may file a memory task if Bryan still wants that strand

[2026-10-18T01:30:56Z · bob-cli-8y.3] Wired diagrams through the adapter on both Markdown PDF routes. Stub-adapter CLI tests cover success, partial failure, crash/invalid JSON/timeout, missing adapter, kill switch, no-Mermaid skip, snapshot success/failure, and scale warnings (pandoc+xelatex). Athena smoke with the real adapter on a scratch vault rendered 1 of 2: pdftotext shows Start/Done labels, the broken fence keeps its italic note plus source, exit 0. decision_record=no: recorded PROPOSED FOLLOW-UP for the skipped decisions-web strand. epic-symbols: none leftover.

[2026-10-18T01:45:19Z · bob-cli-8y.3--1] Fixed ETXTBSY flake: diagrams_filter_runs_first_on_generic_route wrote fake-pandoc with fs::write then execd it under parallel cargo test (os error 26). Stub helpers in create.rs and diagrams.rs now write via scratch+cp, matching tests/cli/support.rs. Re-ran the test: ok. epic-symbols: none leftover. Bead already closed; leaving it closed.

## Dependencies

- **Depends on:** [bob-cli-8y.1](bob-cli-8y.1.md) ✓ · ⧖ 2026-10-17
- **Depends on:** [bob-cli-8y.2](bob-cli-8y.2.md) ✓ · ⧖ 2026-10-17
- **Blocks:** [bob-cli-8y.4](bob-cli-8y.4.md) ✓ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-8y.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-8y.3.md) | [bob-cli-8y.3](bob-cli-8y.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`58c9614`](https://github.com/bobs-org/bob-cli/commit/58c9614401350666609e9dbc67d5b95f8aa5b0d9) | feat(highlights-ref): render mermaid diagrams through the clip adapter | [bob-cli-8y.3](bob-cli-8y.3.md) | 2026-10-17 21:56:04 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8y.3--2][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-8y.3.md

<!-- sase:referenced-by:end -->
