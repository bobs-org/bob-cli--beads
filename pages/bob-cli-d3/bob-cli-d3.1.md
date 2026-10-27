# Bead: bob-cli-d3.1 — Renderer emits the source view and code anchors

[Bead Pages](../README.md) / [bob-cli-d3](README.md) / bob-cli-d3.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ao](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ao.md) · **Assignee:** `bob-cli-d3.1` · **Size:** medium
**Created:** 2026-10-27 11:21:28 EDT · **Closed:** 2026-10-27 11:40:00 EDT
**Plan:** [202610/web\_ref\_saved\_sources.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/web_ref_saved_sources.md)

## Description

adapter-source-view: web-clip adapter keeps image origins, writes render/source.html and render/code-anchors.json, injects Chrome-destination anchors for every printed pre, and reports both paths; the Rust client decodes them.

## Notes

[2026-10-27T15:39:39Z · bob-cli-d3.1] PROPOSED FOLLOW-UP: Preserve Mermaid language markers through web article extraction — Defuddle v0.19.4 drops language-mermaid from extracted code blocks, so the web article catalog route may otherwise treat Mermaid as ordinary code.

[2026-10-27T15:40:00Z · bob-cli-d3.1] Verified just check-web-clip-adapter (passed) and cargo test --lib clip_adapter::tests --no-fail-fast (12 passed); capture and compose emit source/code-anchor paths, PDF code destinations are covered, and Rust decodes the additive fields. No epic symbols remain.

## Dependencies

- **Blocks:** [bob-cli-d3.2](bob-cli-d3.2.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-d3.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-d3.1/README.md) | [bob-cli-d3.1](bob-cli-d3.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f8dc405`](https://github.com/bobs-org/bob-cli/commit/f8dc405b9a318496dab8c8f3e0f7e91226ecff7b) | feat(web-clip): emit saved source views and code anchors | [bob-cli-d3.1](bob-cli-d3.1.md) | 2026-10-27 11:41:00 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-d3.1][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-d3.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-d3.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-d3.land/README.md

<!-- sase:referenced-by:end -->
