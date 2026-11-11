# Bead: bob-cli-k6.2 — Vector SVG rendering through the Chrome diagram renderer

[Bead Pages](../README.md) / [bob-cli-k6](README.md) / bob-cli-k6.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.d9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.d9.md) · **Assignee:** `bob-cli-k6.2` · **Size:** medium
**Created:** 2026-11-11 07:53:18 EST · **Closed:** 2026-11-11 09:43:49 EST
**Plan:** [202611/ref\_create\_svg\_images.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/ref_create_svg_images.md)

## Description

svg-vector-render: extend the Mermaid diagram pass and adapter protocol so local SVG embeds render to vector PDFs in the same browser launch, falling back to the guard, then optionally recapture the failed report.

## Notes

[2026-11-11T14:43:31Z · bob-cli-k6.2] PROPOSED FOLLOW-UP: just docs-check still fails on pre-existing 6000-word budget overruns in files this phase did not touch (docs/reference/json-outputs.md plus mounted mac-capture capture-panel/capture-previews/keyboard/protocol and plugins/bob-navigation-hotkeys.md); tracked by bob-cli-jz and bob-cli-h9

[2026-11-11T14:43:49Z · bob-cli-k6.2] Vector SVG rendering ships through the Chrome diagram pass: local generic-Markdown SVG embeds collect as sha1(svg\0target), render inline in the same adapter launch as Mermaid (protocol 1, kind omitted for mermaid), swap to vector PDFs, and fall back to the sibling/placeholder guard with renderer errors. cargo fmt --check, just lint, cargo test --workspace --no-fail-fast, and just check-web-clip-adapter passed. Recapture of keep_moving_link_marks after just install printed diagrams: rendered 2 of 2 Mermaid diagrams and svg: rendered 1 of 1 SVG images (exit 0). Empty image-guard reports now encode images as []. Snapshot SVG stays on the placeholder path. No leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-k6.1](bob-cli-k6.1.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-k6.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-k6.2/README.md) | [bob-cli-k6.2](bob-cli-k6.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`7eb8244`](https://github.com/bobs-org/bob-cli/commit/7eb82440731f94ffc65177b1ab94a2fa708bd447) | feat(highlights): render local SVG embeds as vector PDFs | [bob-cli-k6.2](bob-cli-k6.2.md) | 2026-11-11 09:45:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-k6.2][1] | Need full notes, history, and remaining work for this phase | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-k6.2/README.md

<!-- sase:referenced-by:end -->
