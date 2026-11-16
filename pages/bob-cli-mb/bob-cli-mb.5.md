# Bead: bob-cli-mb.5 — bob-plugins: line-less bob-open-notes opens record a \`\<C-o\>\` jump

[Bead Pages](../README.md) / [bob-cli-mb](README.md) / bob-cli-mb.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cs](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cs.md) · **Assignee:** `bob-cli-mb.5` · **Size:** small
**Created:** 2026-11-16 10:14:22 EST · **Closed:** 2026-11-16 10:41:48 EST
**Plan:** [202611/note\_goto\_followups.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/note_goto_followups.md)

## Description

plugin-open-notes-jump: in bob-navigation-hotkeys, record a Vim jump from the prior caret to the landed note when `obsidian://bob-open-notes` opens a Markdown note without a line, with tests, docs, and a deployed sync.

## Notes

[2026-11-16T15:41:48Z · bob-cli-mb.5] plugin-open-notes-jump done: line-less Markdown bob-open-notes opens now record a Vim jump via finishVimLinkJump (commit c68ff50 in bob-plugins). Verified: 34/34 pass in test-navigation-open-notes-uri.cjs (6 new jump tests), 77/77 across open-notes/goto-task/jump-history suites, npm run docs:check passes, deployed via bob plugins sync -p bob-navigation-hotkeys. Full npm test shows only pre-existing perf/e2e flakes that also fail on the clean base tree (baseline 8 vs 6 with this change, same unrelated tests). No epic-symbol entries remain.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-mb.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mb.5/README.md) | [bob-cli-mb.5](bob-cli-mb.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mb.5][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-mb.5/README.md

<!-- sase:referenced-by:end -->
