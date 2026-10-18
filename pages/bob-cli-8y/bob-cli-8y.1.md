# Bead: bob-cli-8y.1 — Mermaid \`diagrams\` op in the web-clip adapter

[Bead Pages](../README.md) / [bob-cli-8y](README.md) / bob-cli-8y.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4r.linker.w0.md) · **Assignee:** `bob-cli-8y.1` · **Size:** medium
**Created:** 2026-10-17 19:29:16 EDT · **Closed:** 2026-10-17 20:33:57 EDT
**Plan:** [202610/ref\_create\_mermaid\_figures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_mermaid_figures.md)

## Description

adapter: vendor a pinned Mermaid 12.x bundle and a static DejaVu Sans TTF, add a `diagrams` op that renders batches offline in one Chrome page to fitted vector PDFs with per-item error isolation, report the version from ping, and extend the self-test.

## Notes

[2026-10-18T00:33:49Z · bob-cli-8y.1--4] PROPOSED FOLLOW-UP: Decide whether to add the Mermaid rendering and failure-policy decision record — the epic selected decision_record: no, so decisions:ref-create-renders-mermaid-in-the-adapter was intentionally skipped; the land agent should triage this proposal.

[2026-10-18T00:33:57Z · bob-cli-8y.1--4] Verified the adapter self-test and full just check passed; a protocol-1 flowchart LR request through the materialized adapter returned Mermaid 12.2.0 and a vector PDF whose Start, Render, Mermaid PDF, and Finish labels were extracted by pdftotext. Recorded the skipped decision-record follow-up and confirmed no epic symbols remain.

## Dependencies

- **Blocks:** [bob-cli-8y.3](bob-cli-8y.3.md) ✓ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-8y.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-8y.1.md) | [bob-cli-8y.1](bob-cli-8y.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`54670b4`](https://github.com/bobs-org/bob-cli/commit/54670b4535e3328f5ec1e54c574ff4e7ac8925de) | feat(web-clip): add offline Mermaid diagram rendering | [bob-cli-8y.1](bob-cli-8y.1.md) | 2026-10-17 20:34:41 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-8y.1--4][1] | Confirm the assigned phase is closed with the verification note | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-8y.1.md

<!-- sase:referenced-by:end -->
