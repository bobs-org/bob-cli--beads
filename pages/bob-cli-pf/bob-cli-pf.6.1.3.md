# Bead: bob-cli-pf.6.1.3 — Enable fail-open ownership on album, record, and temporal cards

[Bead Pages](../README.md) / [bob-cli-pf.6.1](bob-cli-pf.6.1.md) / bob-cli-pf.6.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.6.md) · **Assignee:** `bob-cli-pf.6.1.3` · **Size:** medium
**Created:** 2026-11-23 20:38:15 EST · **Closed:** 2026-11-23 23:10:05 EST
**Plan:** [202611/frontmatter\_takeover.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/frontmatter_takeover.md)

## Description

adapter-takeover: wire successful card mounts to generation-bound whole-container ownership, preserving row hiding as fallback and promptly releasing on invalidation, failure, Source, navigation, or teardown. Include identity-only day cards.

## Notes

[2026-11-24T04:10:05Z · bob-cli-pf.6.1.3] Implemented generation-bound, source/cache/capability-gated frontmatter ownership for album, record, and day/week/quarter/year cards, with fail-open release across invalidation, Source, navigation, failed mounts, and teardown. Verified: focused ownership/adapter suite (156 passed), npm run build:check, npm run docs:inventory:check, git diff --check, bob plugins sync; epic-symbols reported none.

## Dependencies

- **Depends on:** [bob-cli-pf.6.1.2](bob-cli-pf.6.1.2.md) ✓ · ⧖ 2026-11-23
- **Blocks:** [bob-cli-pf.6.1.4](bob-cli-pf.6.1.4.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.6.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.3/README.md) | [bob-cli-pf.6.1.3](bob-cli-pf.6.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@57bcb47`](https://github.com/bobs-org/bob-plugins/commit/57bcb470a703dbb263a3a1847b8490be4675d5a2) | feat(property-cards): own frontmatter on mounted cards | [bob-cli-pf.6.1.3](bob-cli-pf.6.1.3.md) | 2026-11-23 23:11:47 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.6.1.3][1] | Review remaining phase notes before closing | 2 |
| read-by | [agent:bob-cli-pf.6.1.land][2] | Need the child scope and notes | 1 |
| read-by | [agent:fx][3] | Timeline of pf phase closures for pl gate research | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.land/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.fx/README.md

<!-- sase:referenced-by:end -->
