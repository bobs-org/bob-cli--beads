# Bead: bob-cli-ct.1 — Render-time link records in the code catalog

[Bead Pages](../README.md) / [bob-cli-ct](README.md) / bob-cli-ct.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14k.md) · **Assignee:** `bob-cli-ct.1` · **Size:** medium
**Created:** 2026-10-26 15:37:26 EDT · **Closed:** 2026-10-26 16:02:04 EDT
**Plan:** [202610/ref\_link\_copy.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_link_copy.md)

## Description

links-catalog: extend the render-time catalog filter to record every URI link (exact target, text, autolink flag, lead-in context, section) with an invisible inline PDF anchor for its page, store them as an additive `links` array in code.json, and apply the bare_urls reader decision.

## Notes

[2026-10-26T20:01:56Z · bob-cli-ct.1] PROPOSED FOLLOW-UP: just docs-check published-URLs gate still red on two bob-command-mode links (tracked by bob-cli-cs); unrelated to links-catalog, lint/build/drift pass

[2026-10-26T20:02:04Z · bob-cli-ct.1] links-catalog done: render-time URI link records with BobLinkAnchor pages in code.json links array, bare_urls reader flags, links: summary line, docs updated; verified link render test (16 links, copy=click via annotations, pages via pdftotext), ref_library/code/attach/diagrams/snapshot/highlights-create suites green, clippy/fmt clean; docs-check URLs red pre-existing (bob-cli-cs)

## Dependencies

- **Blocks:** [bob-cli-ct.2](bob-cli-ct.2.md) ◐ · ⧖ 2026-10-26
- **Blocks:** [bob-cli-ct.3](bob-cli-ct.3.md) ◐ · ⧖ 2026-10-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ct.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ct.1/README.md) | [bob-cli-ct.1](bob-cli-ct.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`96793fd`](https://github.com/bobs-org/bob-cli/commit/96793fdac1309f1fc8c0cada42211222eef6d8b7) | feat(highlights-ref): record URI link catalog with anchor pages in code.json | [bob-cli-ct.1](bob-cli-ct.1.md) | 2026-10-26 16:03:47 EDT |
