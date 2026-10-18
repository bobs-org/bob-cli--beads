# Bead: bob-cli-8y.2 — Diagram collect and swap filters, wired behind an off-by-default hook

[Bead Pages](../README.md) / [bob-cli-8y](README.md) / bob-cli-8y.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4r.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4r.linker.w0.md) · **Assignee:** `bob-cli-8y.2` · **Size:** medium
**Created:** 2026-10-17 19:29:16 EDT · **Closed:** 2026-10-17 20:11:22 EDT
**Plan:** [202610/ref\_create\_mermaid\_figures.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_mermaid_figures.md)

## Description

ast: add the Rust diagrams module with the kill switch, the fence pre-scan, the pandoc collect pass, and the results writer, plus the collect and swap Lua filters, inserted first in both renderers through RenderFilters but unused in production yet.

## Notes

[2026-10-17T23:54:31Z · bob-cli-8y.2] PROPOSED FOLLOW-UP: skipped decisions-web record — epic decision_record=no; land agent may add decisions:ref-create-renders-mermaid-in-the-adapter after wire/finish land (Applies/Claim/Why/Cost/Reopens, metadata.status: accepted, citing the research report and landed commits).

[2026-10-18T00:11:22Z · bob-cli-8y.2--1] Verified diagrams collect/swap: kill switch, fence pre-scan, pandoc collect on both readers, results.json writer, collect/swap Lua filters first on both Markdown PDF routes via RenderFilters. Production callers pass diagrams: None. just check passed (exit 0) including diagrams unit tests and render_temp_pdf/render_note_pdf swap tests. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-8y.3](bob-cli-8y.3.md) ◐ · ⧖ 2026-10-17

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-8y.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-8y.2.md) | [bob-cli-8y.2](bob-cli-8y.2.md) | 0 |
