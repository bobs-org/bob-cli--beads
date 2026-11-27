# Bead: bob-cli-qj.5.1.4 — bob prose extract planner and hidden CLI

[Bead Pages](../README.md) / [bob-cli-qj.5.1](bob-cli-qj.5.1.md) / bob-cli-qj.5.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-qj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.md) · **Assignee:** `bob-cli-qj.5.1.4` · **Size:** medium
**Created:** 2026-11-27 07:18:28 EST · **Closed:** 2026-11-27 11:17:28 EST
**Plan:** [202611/prose\_section\_extract\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_section_extract_inline.md)

## Description

extract: the extract planner, the ProseConversion v1 JSON types, the fingerprint, and a hidden bob prose extract that writes through vault_rewrite.

## Notes

[2026-11-27T16:16:59Z · bob-cli-qj.5.1.4] PROPOSED FOLLOW-UP: Add Prose Section glossary strand (decisions:memory_prose_section was no) — descriptor glossary:prose-section with keyword Prose Section, body covering authored heading subtree extract/inline, eligibility derived at cursor, derived prose extracted_from/extracted_heading, non-goals, pointer to docs/prose.md; then run sase memory init, just docs-gen, just docs-check.

[2026-11-27T16:17:06Z · bob-cli-qj.5.1.4] PROPOSED FOLLOW-UP: just lint gate is red on clean base (clippy_gate errors in section_model.rs let-else, relocate.rs items-after-test-module, plus 160+ pre-existing errors noted on bob-cli-qj.5.1.1); extract phase introduces no new gate errors — convert/extract.rs and prose/cli.rs pass the gate.

[2026-11-27T16:17:28Z · bob-cli-qj.5.1.4] Implemented hidden bob prose extract with ProseConversion v1, fingerprint W2, planner X1-X7 via vault_rewrite. Verified preview/write JSON shape and exit codes, every refusal code, stub-section next inline, name-taken/bad-name/plan-changed races, link relocation both directions, prose host numbering off, .bob/.trash exclusion, offline writes, human diffs. Tests: cargo test lib native::prose 54 passed, cargo test cli prose 48 passed, docs-gen regenerated docs/reference/cli/prose.md. Pre-existing clippy_gate red on clean base recorded as follow-up; no new gate errors from this phase.

## Dependencies

- **Depends on:** [bob-cli-qj.5.1.1](bob-cli-qj.5.1.1.md) ✓ · ⧖ 2026-11-27
- **Depends on:** [bob-cli-qj.5.1.2](bob-cli-qj.5.1.2.md) ✓ · ⧖ 2026-11-27
- **Depends on:** [bob-cli-qj.5.1.3](bob-cli-qj.5.1.3.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-qj.5.1.5](bob-cli-qj.5.1.5.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.5.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.5.1.4/README.md) | [bob-cli-qj.5.1.4](bob-cli-qj.5.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`a558ce1`](https://github.com/bobs-org/bob-cli/commit/a558ce11176fcb9d03e8a11be917f8d671810b32) | feat(prose): plan and write prose-section extraction | [bob-cli-qj.5.1.4](bob-cli-qj.5.1.4.md) | 2026-11-27 11:18:45 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.5.1.4][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-qj.5.1.land][2] | Need the child scope and notes | 1 |
| read-by | [agent:bob-cli-r7.land][3] | Check phase notes for known hidden prose extract catalog/completion test failures | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.5.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.1.land.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-r7.land/README.md

<!-- sase:referenced-by:end -->
