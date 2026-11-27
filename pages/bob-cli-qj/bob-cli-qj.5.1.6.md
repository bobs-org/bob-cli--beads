# Bead: bob-cli-qj.5.1.6 — Contract docs, host probe, and vault-clone dogfood

[Bead Pages](../README.md) / [bob-cli-qj.5.1](bob-cli-qj.5.1.md) / bob-cli-qj.5.1.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-qj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.md) · **Assignee:** `bob-cli-qj.5.1.6` · **Size:** small
**Created:** 2026-11-27 07:18:28 EST · **Closed:** 2026-11-27 13:42:26 EST
**Plan:** [202611/prose\_section\_extract\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_section_extract_inline.md)

## Description

contract-docs: document the conversion contract in docs/prose.md and the reference pages, add the prose-extract-preview host probe, round-trip real sections on a throwaway vault clone, and apply the accepted memory decision.

## Notes

[2026-11-27T18:20:07Z · bob-cli-qj.5.1.6] PROPOSED FOLLOW-UP: add glossary:prose-section memory strand (decision memory_prose_section=no in plan:202611/prose_section_extract_inline.md)

[2026-11-27T18:26:47Z · bob-cli-qj.5.1.6] PROPOSED FOLLOW-UP: check-scripts install_ui live PTY test test_real_cargo_install_transcript_uses_correct_phases_and_hides_chatter fails identically on clean base (StopIteration seeking "compiling dependencies 87/235"); unrelated to contract-docs, needs triage

[2026-11-27T18:42:04Z · bob-cli-qj.5.1.6] PROPOSED FOLLOW-UP: just lint fails on clean base too (clippy 1.95 filter_map_bool_then at prose/convert/inline.rs:760 and useless_format at :1357, both from phase inline eff5d986; no .rs file touched by contract-docs)

[2026-11-27T18:42:26Z · bob-cli-qj.5.1.6] Contract docs done and verified: docs/prose.md gains Prose-sections (terms/selection/eligibility/X1-X7/I1-I9/relocation/L1-L3/provenance+W1-W5/toggle) and ProseConversion v1 JSON sections; vault-format, json-outputs, contracts.yml updated; just docs-gen clean and just docs-check passes (budgets met, README snapshot hash updated). prose-extract-preview probe added to bob-host-currency (usage, body, detail, known-probe list) and passes locally (exit 0). Dogfood on throwaway shared clone /tmp/dogfood-vault: extract+inline -o -w byte-identical on job_2026 Why-I-left-Google, dev Future-Work (bullet-only, 1 link), sase_blog_contents 5-Conclusion (numbered prose); live read-only previews match and Tasks refuses structural-section; live vault untouched; transcript stored as file:explicit:15f129d593801a369e9a1e2d. memory_prose_section=no honored (no memory edit; follow-up recorded). Two pre-existing clean-base failures recorded as follow-ups, not blockers: install_ui live PTY transcript test and clippy 1.95 lints in inline.rs from phase eff5d986.

## Dependencies

- **Depends on:** [bob-cli-qj.5.1.5](bob-cli-qj.5.1.5.md) ✓ · ⧖ 2026-11-27
- **Blocks:** [bob-cli-qj.5.1.7](bob-cli-qj.5.1.7.md) ◐ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.5.1.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.5.1.6/README.md) | [bob-cli-qj.5.1.6](bob-cli-qj.5.1.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d856be4`](https://github.com/bobs-org/bob-cli/commit/d856be45f37d9ca3b62cad77c426fd6247406e8b) | docs(prose): document extract and inline sections with JSON contract | [bob-cli-qj.5.1.6](bob-cli-qj.5.1.6.md) | 2026-11-27 13:44:02 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.5.1.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.5.1.6/README.md

<!-- sase:referenced-by:end -->
