# Bead: bob-cli-7v.3 — Adapter render:false capture, compose op, and the collection layout

[Bead Pages](../README.md) / [bob-cli-7v](README.md) / bob-cli-7v.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.10k](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.10k.md) · **Assignee:** `bob-cli-7v.3` · **Size:** medium
**Created:** 2026-10-15 12:30:28 EDT · **Closed:** 2026-10-15 12:58:00 EDT
**Plan:** [202610/ref\_create\_multi\_url\_collections.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_multi_url_collections.md)

## Description

adapter: let capture skip printing, add a compose op that typesets ordered article.json parts into one PDF (opening page, linked contents, a fresh page and bookmark per part, namespaced ids and assets), plus the Rust client types; single-capture requests stay byte-identical.

## Notes

[2026-10-15T16:58:00Z · bob-cli-7v.3] Verified render:false capture (article.json written, pdf_bytes null, out_pdf omitted), compose op plus render_collection, and Rust CaptureRequest/ComposeRequest serialization (single-capture JSON byte-identical). Two-article fixture HTML: ids/fragments prefixed pN-, contents links to #part-N, opening page has no h1-h6, one h1 per part, unique pN-img-001 assets, relative hrefs resolved per part URL. Printed fixture (mutool): 3 pages, outline two top-level part titles with nested Introduction headings, no blank pages, counters 1/3 2/3 3/3 continuous; collection-title left footer with :first suppression (no per-part named pages). TMPDIR=/tmp just check-web-clip-adapter ok; just check ok. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-7v.5](bob-cli-7v.5.md) ◐ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7v.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7v.3/README.md) | [bob-cli-7v.3](bob-cli-7v.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e104962`](https://github.com/bobs-org/bob-cli/commit/e10496251059137f53dece8f98543e24d5fae283) | feat(web-clip): add render:false capture and collection compose | [bob-cli-7v.3](bob-cli-7v.3.md) | 2026-10-15 12:58:59 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7v.3][1] | Need notes, remaining work, and design file path | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7v.3/README.md

<!-- sase:referenced-by:end -->
