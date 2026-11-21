# Bead: bob-cli-om.1 — Fix bob's wikilink field range and ranking, publish shared vectors

[Bead Pages](../README.md) / [bob-cli-om](README.md) / bob-cli-om.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5o.linker.w0.md) · **Assignee:** `bob-cli-om.1` · **Size:** medium
**Created:** 2026-11-21 10:32:17 EST · **Closed:** 2026-11-21 11:21:45 EST
**Plan:** [202611/prose\_wikilink\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md)

## Description

cli-link-fixes: in bob-cli, end unclosed link fields at the caret, keep authored #subpath and |alias text when the target is replaced, break ranking ties by depth then inbound links, publish tests/fixtures/wikilink_complete/vectors.json, and write the new decisions strand.

## Notes

[2026-11-21T16:21:19Z · bob-cli-om.1--1] PROPOSED FOLLOW-UP: just docs-check still fails identically on clean base HEAD 020ad4e6: docs/reference/vault-format.md is 6016/6000 (tracked by bob-cli-oc), and docs/develop/plugins/plugin-apis.md is 8165/8000 (tracked by bob-cli-ob). Neither docs file is changed by this phase; the reproduced fatal lint failure is vault-format.

[2026-11-21T16:21:45Z · bob-cli-om.1--1] Verified wikilink field ranges, authored suffix preservation, depth/inbound ranking, and shared vectors; focused Rust vectors and capture_links tests passed, and just all passed. docs-check fails on clean base HEAD 020ad4e6 with the same tracked word-budget lint findings; recorded them in the phase follow-up note (bob-cli-oc, bob-cli-ob). epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-om.2](bob-cli-om.2.md) ✓ · ⧖ 2026-11-21
- **Blocks:** [bob-cli-om.8](bob-cli-om.8.md) ◐ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-om.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-om.1.md) | [bob-cli-om.1](bob-cli-om.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`746f4d5`](https://github.com/bobs-org/bob-cli/commit/746f4d5a4aa5ada921ca8bce5d454a473ab4d0ed) | fix(capture): preserve wikilink fields and rank candidates | [bob-cli-om.1](bob-cli-om.1.md) | 2026-11-21 11:23:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-om.1--1][1] | Need the phase scope, design file, and prior notes before finishing verification | 4 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-om.1.md

<!-- sase:referenced-by:end -->
