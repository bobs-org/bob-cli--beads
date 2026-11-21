# Bead: bob-cli-om.9 — Mac Pull-In reason link band

[Bead Pages](../README.md) / [bob-cli-om](README.md) / bob-cli-om.9

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5o.linker.w0.md) · **Assignee:** `bob-cli-om.9` · **Size:** medium
**Created:** 2026-11-21 10:32:18 EST · **Closed:** 2026-11-21 13:13:35 EST
**Plan:** [202611/prose\_wikilink\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md)

## Description

mac-pull-in: wire the Pull-In cancel reason field (S16) in bob-mac-capture to capture-complete --links-only. Render a LINK band in the recall band's slot with the same key contract, fail open on an older bob, and watch macOS CI to green.

## Notes

[2026-11-21T18:13:17Z · bob-cli-om.9] PROPOSED FOLLOW-UP: docs-check lint still reports 2 word-budget errors on the clean base (plugin-apis, bob-navigation-hotkeys, vault-format); unrelated to this phase

[2026-11-21T18:13:24Z · bob-cli-om.9] PROPOSED FOLLOW-UP: push the bob-mac-capture change and watch the exact-SHA macOS run to green; agent had no commit/push authorization so CI never ran

[2026-11-21T18:13:35Z · bob-cli-om.9] mac-pull-in done: Pull-In reason LINK band via capture-complete --links-only + --source-note, same key contract, fail-open on old bob. Verified: athena swift build+test 2656 pass (18 PullInLinkState + 5 links-only client new); mac swift build + typecheck-tests PASS; docs-check matches clean-base (2 pre-existing budget errors). Push + macOS CI watch left for user (no push authorization).

## Dependencies

- **Depends on:** [bob-cli-om.8](bob-cli-om.8.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-om.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.9/README.md) | [bob-cli-om.9](bob-cli-om.9.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-om.9][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.9/README.md

<!-- sase:referenced-by:end -->
