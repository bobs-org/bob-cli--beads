# Bead: bob-cli-a0.2.1.7.3 — Check fragments offline, widen mention scans, and finish templates

[Bead Pages](../README.md) / [bob-cli-a0.2.1.7](bob-cli-a0.2.1.7.md) / bob-cli-a0.2.1.7.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.2.1.land.md) · **Assignee:** `bob-cli-a0.2.1.7.3` · **Size:** medium
**Created:** 2026-10-19 21:02:59 EDT · **Closed:** 2026-10-19 21:24:06 EDT
**Plan:** [202610/docs\_toolchain\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_toolchain_landing_fixes.md)

## Description

links-authoring: enable offline lychee fragment checking, scan every text source for docs mentions, harden the URL resolver and live manifest, and give the authoring templates and guide Bob examples and Output fences.

## Notes

[2026-10-20T01:23:48Z · bob-cli-a0.2.1.7.3] EVIDENCE: just docs-check green. lint ok; 32 published pages; urls OK (365 mentions checked, 1 curated); offline lychee with --include-fragments --index-files index.html: 3595 total, 821 unique, 3374 OK, 0 errors, 221 excluded; search smoke 2 cases; 123 pytest. just docs-build-material green. Injected broken relative #this-anchor-does-not-exist and org-root /plan/#also-missing into a temp site copy: lychee 2 errors, both Cannot find fragment. Output fence syntax proven on a scratch page then removed: ```text { .no-copy title="Output" } renders <span class="filename">Output</span> and class="no-copy highlight" in both Zensical and Material 9.7. cargo run -q -- plan --help and bob plan -b <temp vault> verified -b/--bob-dir and -f/--format. epic-symbols: none. No SASE memory edits. No Rust source changes.

[2026-10-20T01:24:06Z · bob-cli-a0.2.1.7.3] Verified offline lychee fragment checking (3595 links, 0 errors; injected relative and org-root anchors fail), all-text mention scans (365 mentions resolve), URL resolver/live-manifest/ignore/refresh hardening, Output fence syntax on both builders, templates and writing-docs passing lint; just docs-check and just docs-build-material green; 123 pytest; epic-symbols none.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.2.1.7.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.7.3/README.md) | [bob-cli-a0.2.1.7.3](bob-cli-a0.2.1.7.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`5cbfea1`](https://github.com/bobs-org/bob-cli/commit/5cbfea1f38d605e840f8dad69551b9b9e71ac52d) | fix(docs): check fragments offline and finish authoring templates | [bob-cli-a0.2.1.7.3](bob-cli-a0.2.1.7.3.md) | 2026-10-19 21:25:17 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.2.1.7.3][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.7.3/README.md

<!-- sase:referenced-by:end -->
