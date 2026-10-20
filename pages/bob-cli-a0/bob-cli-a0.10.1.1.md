# Bead: bob-cli-a0.10.1.1 — Support source-owned mounted documentation hubs

[Bead Pages](../README.md) / [bob-cli-a0.10.1](bob-cli-a0.10.1.md) / bob-cli-a0.10.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.10](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.10.md) · **Assignee:** `bob-cli-a0.10.1.1` · **Size:** medium
**Created:** 2026-10-19 23:16:01 EDT · **Closed:** 2026-10-19 23:33:55 EDT
**Plan:** [202610/plugin\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/plugin_reference.md)

## Description

mount-hubs: add compatible support for a mounted repository's index.md while preserving authored landing pages, collision guards, provenance, and navigation.

## Notes

[2026-10-20T03:33:55Z · bob-cli-a0.10.1.1] Source-owned index.md hubs copy and stamp like other pages when the destination is gitignored and untracked; authored landings still work and are never replaced. Nested docs/ plus docs/develop/ hubs get provenance and one nav entry each. Repeat assembly, hub refresh, stale-page cleanup, and collision/ignore/symlink/tracked failures leave outputs untouched. Copied-hub lint covers source stamps and gitignore. just docs-check passed (219 unit tests) with mounts.yml and plugin-index gitignore exceptions unchanged. No leftover --epic-symbol entries.

## Dependencies

- **Blocks:** [bob-cli-a0.10.1.5](bob-cli-a0.10.1.5.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.10.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.1/README.md) | [bob-cli-a0.10.1.1](bob-cli-a0.10.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f367829`](https://github.com/bobs-org/bob-cli/commit/f3678291e724cc5f967145620732e0d72ec63374) | feat(docs): support source-owned mounted documentation hubs | [bob-cli-a0.10.1.1](bob-cli-a0.10.1.1.md) | 2026-10-19 23:35:35 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.10.1.1][1] | Need full phase description, notes, DECISIONS, and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.10.1.1/README.md

<!-- sase:referenced-by:end -->
