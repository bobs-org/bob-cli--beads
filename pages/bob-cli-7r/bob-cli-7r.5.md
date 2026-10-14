# Bead: bob-cli-7r.5 — Bob Mac Capture owner-aware pickers and the calm owner hint

[Bead Pages](../README.md) / [bob-cli-7r](README.md) / bob-cli-7r.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4g.linker.w1.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4g.linker.w1.w0.md) · **Assignee:** `bob-cli-7r.5` · **Size:** medium
**Created:** 2026-10-14 16:21:12 EDT · **Closed:** 2026-10-14 18:22:44 EDT
**Plan:** [202610/capture\_relate\_existing\_tasks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/capture_relate_existing_tasks.md)

## Description

mac_pickers: give the `&`/`*` picker headers the owner's name and direction, fix the nil new-task header, and add the "This note" group. Add an owner mode to the `+`/`@route+` picker with copy and disabled rows. Add a calm `dependency_target` hint in place of the red preview error. Fixtures, tests, and the README picker docs.

## Notes

[2026-10-14T22:22:32Z · bob-cli-7r.5] PROPOSED FOLLOW-UP: skipped decisions memory strand for existing-owner relationship rules — epic DECISIONS set decision_record=no, so the land agent should file a memory task for a new decisions web strand covering owner-aware &/* headers, + owner-mode parent picker, and the calm dependency_target hint.

[2026-10-14T22:22:44Z · bob-cli-7r.5] mac_pickers landed in bob-mac-capture: owner-aware &/* headers (owner.text, direction glyphs, This note first), +/@route+ owner-mode parent picker with dimmed disabled rows, and calm dependency_target hint (no dry-run, secondary status). Fixtures/fake-bob routes, README, and Ask Kelly panel repair included. just portable-check on athena: 1182 tests, 0 failures (Linux CaptureCore/RefsCore). Mac SSH to kellys-macbook-pro timed out; macOS BobMacCapture targets unverified. Epic DECISIONS decision_record=no: skipped decisions strand recorded as PROPOSED FOLLOW-UP. sase bead epic-symbols: no leftover --epic-symbol entries.

## Dependencies

- **Depends on:** [bob-cli-7r.4](bob-cli-7r.4.md) ✓ · ⧖ 2026-10-14
- **Blocks:** [bob-cli-7r.6](bob-cli-7r.6.md) ✓ · ⧖ 2026-10-14

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-7r.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7r.5/README.md) | [bob-cli-7r.5](bob-cli-7r.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@e41dee2`](https://github.com/bobs-org/bob-mac-capture/commit/e41dee2dc25b6048449edacaaf92250d15aca98e) | feat(capture): add owner-aware pickers and a calm dependency hint | [bob-cli-7r.5](bob-cli-7r.5.md) | 2026-10-14 18:23:46 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-7r.5][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-7r.5/README.md

<!-- sase:referenced-by:end -->
