# Bead: bob-cli-qj.5.1.7 — Bob Prose extract and inline gesture in Obsidian

[Bead Pages](../README.md) / [bob-cli-qj.5.1](bob-cli-qj.5.1.md) / bob-cli-qj.5.1.7

**Status:** ✓ closed · **Resolution:** (unrecorded) · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-qj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.md) · **Assignee:** `bob-cli-qj.5.1.7` · **Size:** medium
**Created:** 2026-11-27 07:18:28 EST
**Plan:** [202611/prose\_section\_extract\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_section_extract_inline.md)

## Description

keymap: bob-articles gains extract, inline, and toggle commands with a preview modal driven only by bob's JSON, bound per the keymap decision, with Command Mode rows, docs, tests, marker, and deploy.

## Notes

[2026-11-27T19:42:04Z · bob-cli-qj.5.1.7--2] PROPOSED FOLLOW-UP: Add glossary:prose-section after Bryan approves the declined memory change — this phase explicitly did not authorize memory edits.

[2026-11-27T19:42:12Z · bob-cli-qj.5.1.7--2] PROPOSED FOLLOW-UP: Fix the snooze-add-resnooze daily postimage mismatch. It reproduces on clean HEAD c2f73154 and is already tracked by bob-cli-r7.3; this phase records the baseline failure without changing unrelated snooze behavior.

[2026-11-27T19:43:26Z · bob-cli-qj.5.1.7--2] Verification: Bob Prose feature commit 07c4eeb4dc249e506efef49d3c88fa6c04c91720 is contained by origin/master. bob plugins sync succeeded from the linked checkout. The prose-extract-preview probe is current on athena, apollo, and mac (artifact file:explicit:89b09f66b65a5fb2c728053f). Build and validation passed; npm test has the clean-base snooze mismatch tracked by bob-cli-r7.3. epic-symbols found no remaining symbols.

## Dependencies

- **Depends on:** [bob-cli-qj.5.1.5](bob-cli-qj.5.1.5.md) ✓ · ⧖ 2026-11-27
- **Depends on:** [bob-cli-qj.5.1.6](bob-cli-qj.5.1.6.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.5.1.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.1.7.md) | [bob-cli-qj.5.1.7](bob-cli-qj.5.1.7.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c2f7315`](https://github.com/bobs-org/bob-plugins/commit/c2f73154be826107b397ed7eeaa4348468dc8a02) | feat(prose): add section extraction and inline gestures | [bob-cli-qj.5.1.7](bob-cli-qj.5.1.7.md) | 2026-11-27 14:12:12 EST |
| bob-plugins | [`bob-plugins@07c4eeb`](https://github.com/bobs-org/bob-plugins/commit/07c4eeb4dc249e506efef49d3c88fa6c04c91720) | feat(bob-articles): ship prose section conversion gestures | [bob-cli-qj.5.1.7](bob-cli-qj.5.1.7.md) | 2026-11-27 14:32:28 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.5.1.7--1][1] | Need the phase scope, design file, notes, and epic symbols | 1 |
| read-by | [agent:research.6o.cld][2] | Check whether the Bob Prose gesture phase edits the prose card host files | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.1.7.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6o.cld/README.md

<!-- sase:referenced-by:end -->
