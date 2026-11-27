# Bead: bob-cli-qj.5 — Plan prose-section extract and inline

[Bead Pages](../README.md) / [bob-cli-qj](README.md) / bob-cli-qj.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.6i.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.6i.linker.w0.md) · **Assignee:** `bob-cli-qj.5` · **Size:** xlarge
**Created:** 2026-11-26 10:56:27 EST · **Closed:** 2026-11-27 07:16:37 EST
**Plan:** [202611/prose\_note\_type.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_note_type.md)

## Description

prose-sections: author and propose the epic for bob prose extract/inline and its Obsidian keymap, bound by the research requirements, with the research's open questions embedded as decisions.

## Notes

[2026-11-27T12:16:37Z · bob-cli-qj.5] Authored and proposed (Staged) the child epic plan 'Extract prose sections into prose notes and inline them back' (sase_plan_prose_section_extract_inline.md; validated 0 warnings). It carries every binding prose-sections requirement: Rust-owned bob prose extract/inline in src/native/prose/ under a new ProseConversion v1 contract (ArticlePlan untouched), vault_rewrite base with tested trash + durable crash-recovery journal, derived eligibility via the real classifier with named refusals, inverse shipped with extract (extract hidden until inline lands), provenance extracted_from/extracted_heading for Phase 3, testable losslessness L1-L3 with proptest, explicit section_numbers: false, heading promotion/demotion with depth-overflow refusals, all-direction link relocation, and a thin bob-articles keymap client. Open research questions embedded as decisions: keymap (new_chord|overload), stub_form (link|embed), intro_prose (refuse|overview), prose_catalog (toggle, with reversal catalog-skip fix), memory_prose_section (glossary:prose-section, default off). Cited decisions: prose-notes-are-owned-prose, drawers-keep-their-names, task-reqs-are-met-with-their-task, projects-block-from-prj-line, unblocked-tasks-are-offered, relation-label-rename-rewrites-history, notebook-routes-write-notes, reference-sources-are-preserved-write-once, q-and-ctrl-bracket-mirror-esc, mac-capture-is-a-thin-client, bob-cli-releases-ride-a-daily-train. 8 phases: txn-trash-recovery, section-model, link-relocation, extract, inline, contract-docs, keymap, prose-catalog. Epic symbols: none.

## Dependencies

- **Depends on:** [bob-cli-qj.4](bob-cli-qj.4.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.md) | [bob-cli-qj.5](bob-cli-qj.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-qj.5.1.land][1] | Need the parent phase scope to tell the tale what to verify before closing it | 1 |
| read-by | [agent:bob-cli-qj.5.1.land--1][1] | Check the parent epic bead status and closure requirements | 1 |
| read-by | [agent:research.6k.gem][2] | Inspect in-progress phase details and progress notes of qi and qj epics | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.1.land.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.gem/README.md

<!-- sase:referenced-by:end -->
