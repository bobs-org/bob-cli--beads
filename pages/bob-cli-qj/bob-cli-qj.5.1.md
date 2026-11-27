# Bead: bob-cli-qj.5.1 — Extract prose sections into prose notes and inline them back

[Bead Pages](../README.md) / [bob-cli-qj.5](bob-cli-qj.5.md) / bob-cli-qj.5.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-qj.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-qj.5.md) · **Assignee:** `bob-cli-qj.5.1.land`
**Created:** 2026-11-27 07:18:27 EST
**Plan:** [202611/prose\_section\_extract\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_section_extract_inline.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/prose_section_extract_inline.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_section_extract_inline.md

<!-- sase:links:end -->

## Description

One Obsidian gesture turns an authored section of an area, project, or prose note into a prose note, and the same gesture folds it back. bob prose extract and bob prose inline own the conversion in Rust: previewed, preimage-guarded, all-or-nothing, link-repairing, crash-recoverable, and lossless on a round trip. Extraction records provenance that the later reversible-projects work can consume.

## Notes

[2026-11-27T13:18:36Z · bob-cli-qp.land] DISCOVERED ISSUE (found by the bob-cli-qp land agent running just check on bob-cli master 85d2fb32): clippy fails the canonical gate with 'error: this let...else may be rewritten with the ? operator' (clippy::question_mark, denied by clippy_gate) at src/native/prose/section_model.rs:922-928 (let Some(rest) = bullet.strip_prefix("- ").or_else(.."* ").or_else(.."+ ") else { return None; };). The file was added by 85d2fb32 (bob-cli-qj.5.1.2), which closed after only cargo test --lib native::prose::section_model::tests. Because the build of bob-obsidian (lib) stops there, just check runs no tests at all on master for every agent. Fix: let rest = bullet.strip_prefix("- ").or_else(...).or_else(...)?; then rerun just check. Log: ~/.cache/sase/tmp/qp-land/just-check.log on apollo.

[2026-11-27T15:57:34Z · bob-cli-r7.2--1] DISCOVERED ISSUE: clippy_gate still red on master at question_mark section_model.rs:924 and items_after_test_module relocate.rs:813 (qj.5.1.2 / qj.5.1.3 leftovers). bob-cli-r7.2 recovery applied the mechanical repairs (let rest = ...?; helpers moved above mod tests) so just check can land unrelated docs-mount work. Please keep those two files in that shape.

## Dependencies

- **Blocks:** [bob-cli-qw](../bob-cli-qw/README.md) ◇ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-qj.5.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-qj.5.1.land/README.md) | [bob-cli-qj.5.1](bob-cli-qj.5.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-r7.1][1] | check if clean-tree clippy gate failure is already tracked | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-r7.1/README.md

<!-- sase:referenced-by:end -->
