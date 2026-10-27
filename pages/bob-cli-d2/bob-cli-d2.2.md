# Bead: bob-cli-d2.2 — bob ref attach-source adopts orphan saved-source stores

[Bead Pages](../README.md) / [bob-cli-d2](README.md) / bob-cli-d2.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.14o](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.14o.md) · **Assignee:** `bob-cli-d2.2` · **Size:** medium
**Created:** 2026-10-27 07:42:24 EDT · **Closed:** 2026-10-27 08:31:38 EDT
**Plan:** [202610/research\_ref\_saved\_markdown.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/research_ref_saved_markdown.md)

## Description

adopt: let `bob ref attach-source` point a reference at its own unreferenced render-time store after verifying it against the PDF, leave its code.json untouched, make --search optional, and name the repair in the doctor orphan warning.

## Notes

[2026-10-27T12:31:38Z · bob-cli-d2.2--2] Implemented verified adoption of a reference's unique orphan render-time source store, preserving code.json; made --search optional for adoption-only runs; added ambiguity and mismatch handling, doctor repair guidance, help/completion updates, docs, and regression coverage. Verified just check passed, just docs-check passed (447 passed, 1 skipped for absent font-generation dependencies), and epic-symbols reported no leftovers.

## Dependencies

- **Blocks:** [bob-cli-d2.3](bob-cli-d2.3.md) ✓ · ⧖ 2026-10-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-d2.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d2.2.md) | [bob-cli-d2.2](bob-cli-d2.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`d38bef5`](https://github.com/bobs-org/bob-cli/commit/d38bef590c065b2bfef67745b0e83ce350707498) | feat(ref): adopt orphan saved source stores | [bob-cli-d2.2](bob-cli-d2.2.md) | 2026-10-27 08:32:19 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-d2.2--2][1] | Need the phase scope, design file, and earlier work notes before completion | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d2.2.md

<!-- sase:referenced-by:end -->
