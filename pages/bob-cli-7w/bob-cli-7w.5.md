# Bead: bob-cli-7w.5 — Bob Mac Capture template presentation

[Bead Pages](../README.md) / [bob-cli-7w](README.md) / bob-cli-7w.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.1j.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.1j.linker.w0.md) · **Assignee:** `bob-cli-7w.5` · **Size:** medium
**Created:** 2026-10-15 14:04:18 EDT · **Closed:** 2026-10-15 17:06:43 EDT
**Plan:** [202610/bulk\_capture\_templates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bulk_capture_templates.md)

## Description

mac: decode the additive template fields and present them in Bob Mac Capture: slot-colored placeholders and fields, a calm no-rows state, in-place diagnostic underlines, a template preview chip, and the header candidate row.

## Notes

[2026-10-15T20:56:52Z · bob-cli-7w.5--2] PROPOSED FOLLOW-UP: Add an optional Expand template editor action backed by bob capture -E — skipped by the final mac_expand_action=no decision.

[2026-10-15T20:56:57Z · bob-cli-7w.5--2] PROPOSED FOLLOW-UP: Add a decision record that explicit @template: expands to equivalent captures before parsing — skipped by the final memory_template_decision=no decision.

[2026-10-15T21:06:43Z · bob-cli-7w.5--4] Bob Mac Capture template presentation and real Bob fixtures are in the linked repo. cargo build --bin bob passed; Athena portable-check passed with 1,209 tests and exit 0; git diff --check passed. The Mac scratch bundle built, but typecheck-tests could not load arm64-apple-macosx26.0 standard library and mac SSH later timed out, so macOS targets remain unverified.

## Dependencies

- **Depends on:** [bob-cli-7w.2](bob-cli-7w.2.md) ✓ · ⧖ 2026-10-15
- **Depends on:** [bob-cli-7w.3](bob-cli-7w.3.md) ✓ · ⧖ 2026-10-15
- **Depends on:** [bob-cli-7w.4](bob-cli-7w.4.md) ✓ · ⧖ 2026-10-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-7w.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7w.5.md) | [bob-cli-7w.5](bob-cli-7w.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e959476`](https://github.com/bobs-org/bob-mac-capture/commit/e959476fba87df548c3734f0c94311cd419fa5a9) | feat(capture): present bulk templates in Mac Capture | [bob-cli-7w.5](bob-cli-7w.5.md) | 2026-10-15 17:07:35 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7w.5--4][1] | Need the phase scope, design file, and prior notes before final review | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-7w.5.md

<!-- sase:referenced-by:end -->
