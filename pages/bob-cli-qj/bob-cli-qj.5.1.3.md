# Bead: bob-cli-qj.5.1.3 — Relocate links around a moved section

[Bead Pages](../README.md) / [bob-cli-qj.5.1](bob-cli-qj.5.1.md) / bob-cli-qj.5.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-qj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.md) · **Assignee:** `bob-cli-qj.5.1.3` · **Size:** medium
**Created:** 2026-11-27 07:18:28 EST · **Closed:** 2026-11-27 09:29:51 EST
**Plan:** [202611/prose\_section\_extract\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_section_extract_inline.md)

## Description

link-relocation: a relocation map and vault-wide rewriter that repairs links in every direction for extract and its inverse, preserving aliases, embeds, and link form.

## Notes

[2026-11-27T14:29:18Z · bob-cli-qj.5.1.3] PROPOSED FOLLOW-UP: Add glossary:prose-section — document the derived prose-section concept after the epic authorizes the memory note change.

[2026-11-27T14:29:51Z · bob-cli-qj.5.1.3] Implemented relocation maps and vault-wide extract/inline link rewriting with protected-region filtering and preservation of aliases, embeds, path style, fragments, and line endings. Verified cargo check, cargo fmt --check, 3 relocation tests, 34 prose tests (1 ignored corpus test), and 22 ref-rename link tests. Recorded the required glossary follow-up.

## Dependencies

- **Depends on:** [bob-cli-qj.5.1.2](bob-cli-qj.5.1.2.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-qj.5.1.4](bob-cli-qj.5.1.4.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.5.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.5.1.3/README.md) | [bob-cli-qj.5.1.3](bob-cli-qj.5.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9f461d5`](https://github.com/bobs-org/bob-cli/commit/9f461d52c51251f26e778c7eba6550cebc81a8df) | feat(prose): relocate links around extracted sections | [bob-cli-qj.5.1.3](bob-cli-qj.5.1.3.md) | 2026-11-27 09:31:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.5.1.3][1] | Need the phase scope, notes, and design file before implementation | 2 |
| read-by | [agent:bob-cli-qj.5.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.5.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.1.land.md

<!-- sase:referenced-by:end -->
