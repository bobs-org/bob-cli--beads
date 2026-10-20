# Bead: bob-cli-a0.2.1.7.1 — Make mount assembly and serve safe and complete

[Bead Pages](../README.md) / [bob-cli-a0.2.1.7](bob-cli-a0.2.1.7.md) / bob-cli-a0.2.1.7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.2.1.land.md) · **Assignee:** `bob-cli-a0.2.1.7.1` · **Size:** medium
**Created:** 2026-10-19 21:02:59 EDT · **Closed:** 2026-10-19 21:13:54 EDT
**Plan:** [202610/docs\_toolchain\_landing\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_toolchain_landing_fixes.md)

## Description

mount-safety: fix front-matter stamping, destination symlink and gitignore validation, stale-deletion safety, cache freshness, serve build.json and live reload, and add the missing mounts acceptance tests.

## Notes

[2026-10-20T01:13:54Z · bob-cli-a0.2.1.7.1] mount-safety done: stamp delimiter fixed; destination symlink+resolved-parent+gitignore validation with shared bob_docs/ignore.py; validated-before-mutate sync (spoof/stale checks first, safe stale deletion); cache origin check with fetch/reset and offline-keep warning; staged build.json published by assemble with builder field (zensical/material) and serve live-mirror loop; README production example paths fixed. Verified: 150 docs tests pass, just docs-check exit 0, just docs-build-material exit 0, real lint ok, site build.json shows builder material with all tool versions, tracked tree shows only intended files, epic-symbols clean.

## Dependencies

- **Blocks:** [bob-cli-a0.2.1.7.2](bob-cli-a0.2.1.7.2.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.2.1.7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.7.1/README.md) | [bob-cli-a0.2.1.7.1](bob-cli-a0.2.1.7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2c50df5`](https://github.com/bobs-org/bob-cli/commit/2c50df5594a392e36b999be0968a0d14cce70d10) | feat(docs): make mount assembly and serve safe and complete | [bob-cli-a0.2.1.7.1](bob-cli-a0.2.1.7.1.md) | 2026-10-19 21:14:58 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.2.1.7.1][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.2.1.7.1/README.md

<!-- sase:referenced-by:end -->
