# Bead: bob-cli-ex.3 — Mac manila-chip highlighting and @ seal migration

[Bead Pages](../README.md) / [bob-cli-ex](README.md) / bob-cli-ex.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bp.f0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bp.f0.md) · **Assignee:** `bob-cli-ex.3` · **Size:** medium
**Created:** 2026-10-31 12:01:12 EDT · **Closed:** 2026-10-31 14:14:55 EDT
**Plan:** [202610/project\_note\_seals.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/project_note_seals.md)

## Description

mac_seal: Bob Mac Capture decodes the `project_note` span modifier and the new span kinds. It paints the manila chip: a brown wash, brown name and seal, and a green separator and seal for the offer form. It moves picker teaching copy, fake-bob fixtures, and separator-toggle tests from `+` to `@`, and updates the Mac docs.

## Notes

[2026-10-31T18:14:33Z · bob-cli-ex.3] PROPOSED FOLLOW-UP: compile and eyeball the manila chip on the Mac — the Mac was offline, so Sources/BobMacCapture and Tests/BobMacCaptureTests (palette, paintHighlighting wash, CapturePickerView caption, new highlight/toggle/type-through tests) were never compiled and the 0.16/0.26 wash alphas were not tuned by eye; run bundle.sh + just typecheck-tests on a scratch rsync copy once it is online and let macOS CI run the tests

[2026-10-31T18:14:39Z · bob-cli-ex.3] PROPOSED FOLLOW-UP: fake-bob sealed-toggle (@r^id@: and @r:id@^) and offer-form parse replies are hand-authored from the plan contract — mac_offer_card (bob-cli-ex.4) must re-check them against real bob once offer_form (bob-cli-ex.2) lands

[2026-10-31T18:14:55Z · bob-cli-ex.3] mac_seal done in bob-mac-capture: CaptureSpan decodes project_note; new categories projectNoteName/Seal/OfferSeal with per-span brown manila wash (0.16, 0.26 under Increase Contrast) restored after picker marker clears; Project note caption brown; @ teaching lines and ':' detail strip; fake-bob parse/rewrite replies migrated (real-bob spans for ^ form, hand-authored offer/sealed-toggle replies); block-id fixtures regenerated from real bob (byte-identical); docs (capture-panel, task-pickers, protocol) updated. Verified on athena: swift format lint (no new warnings class), swift build --build-tests, swift test 1823 passed (CaptureCore); just docs-check passed via bob-cli; just check-scripts passed. NOT verified: macOS-only targets (BobMacCapture, BobMacCaptureTests) — Mac offline, never compiled; wash alpha not tuned by eye.

## Dependencies

- **Depends on:** [bob-cli-ex.1](bob-cli-ex.1.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ex.4](bob-cli-ex.4.md) ◐ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ex.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.3/README.md) | [bob-cli-ex.3](bob-cli-ex.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ex.3][1] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ex.3/README.md

<!-- sase:referenced-by:end -->
