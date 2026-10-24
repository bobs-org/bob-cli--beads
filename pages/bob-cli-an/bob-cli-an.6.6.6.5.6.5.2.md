# Bead: bob-cli-an.6.6.6.5.6.5.2 — Give Gist clips a real author and a readable content title

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5](bob-cli-an.6.6.6.5.6.5.md) / bob-cli-an.6.6.6.5.6.5.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.land--2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.2` · **Size:** medium
**Created:** 2026-10-24 12:31:54 EDT · **Closed:** 2026-10-24 12:49:25 EDT
**Plan:** [202610/backlog\_batch7\_url\_identity\_gist\_metadata\_close\_summary\_mac\_ci.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch7_url_identity_gist_metadata_close_summary_mac_ci.md)

## Description

gist-metadata: resolve bob-cli-86 with evidence-based Gist metadata extraction and offline adapter fixtures, preserving generic metadata and explicit overrides.

## Notes

[2026-10-24T16:49:15Z · bob-cli-an.6.6.6.5.6.5.2] PROPOSED FOLLOW-UP: Carry the known clean-base just check failures with their owners: native::completion::kinds::tests::every_value_arg_has_a_decision still lacks decisions for themes rename:old/new (bob-cli-bc.6), and the two highlights::continuations::continuation_scan_* failures remain owned by bob-cli-bd; ToolRun 9e9ae28d687b3e9d1f225fb95db35ec1 reproduced the same three test names recorded at batch-6 landing ae3a432b.

[2026-10-24T16:49:25Z · bob-cli-an.6.6.6.5.6.5.2] Verified the offline Gist capture selects karpathy as author and LLM Wiki as title, multi-file Gists without an H1 use the first readable filename, explicit overrides and non-Gist metadata remain intact, and Rust preserves title/author provenance. just check-web-clip-adapter and the focused Rust test passed. just check reproduced only the three baseline failures recorded at ae3a432b and noted above; epic-symbols reported no leftovers.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.2/README.md) | [bob-cli-an.6.6.6.5.6.5.2](bob-cli-an.6.6.6.5.6.5.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e3754c0`](https://github.com/bobs-org/bob-cli/commit/e3754c0ddbb8531265668fbfcedab227e6ae4884) | feat(web-clip): improve Gist author and title metadata | [bob-cli-an.6.6.6.5.6.5.2](bob-cli-an.6.6.6.5.6.5.2.md) | 2026-10-24 12:50:17 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.2][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.2/README.md

<!-- sase:referenced-by:end -->
