# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.4 — Make Mermaid PDF tests pass when pdftotext is absent

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.4` · **Size:** small
**Created:** 2026-10-25 10:04:07 EDT · **Closed:** 2026-10-25 10:23:17 EDT
**Plan:** [202610/backlog\_batch10\_port\_help\_doctor\_mermaid\_startpending.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch10_port_help_doctor_mermaid_startpending.md)

## Description

mermaid-pdf-pdftotext: resolve bob-cli-9i by handling the missing pdftotext path in the diagram PDF tests so clean trees pass without the binary.

## Notes

[2026-10-25T14:23:17Z · bob-cli-an.6.6.6.5.6.5.5.6.6.4] Removed the raw-bytes pdf_haystack fallback in create.rs, note_snapshot/profile.rs, and tests/cli/highlights/diagrams.rs (pdftotext now required for text assertions); added the missing pdftotext gate to skip_real_diagram_render. Verified: base profile test FAILS with pdftotext hidden (reproduces bob-cli-9i); fixed tree passes focused lib diagrams_ 10/10 both with and without pdftotext (skips with reason when absent), CLI diagrams 12/12 skip-pass without it, one CLI mermaid test passes end-to-end with it; fmt and configured clippy gate clean. Target bob-cli-9i left open for the lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.4/README.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3eebe47`](https://github.com/bobs-org/bob-cli/commit/3eebe47f459207d61d05801347a90dde41b0a909) | fix(highlights): require pdftotext for diagram PDF assertions | [bob-cli-an.6.6.6.5.6.5.5.6.6.4](bob-cli-an.6.6.6.5.6.5.5.6.6.4.md) | 2026-10-25 10:24:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.4][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.land.md

<!-- sase:referenced-by:end -->
