# Bead: bob-cli-nh.4.1.4 — Period field findings and public documentation

[Bead Pages](../README.md) / [bob-cli-nh.4.1](bob-cli-nh.4.1.md) / bob-cli-nh.4.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.md) · **Assignee:** `bob-cli-nh.4.1.4` · **Size:** medium
**Created:** 2026-11-19 13:01:12 EST · **Closed:** 2026-11-19 17:17:36 EST
**Plan:** [202611/intention\_link\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/intention_link_repair.md)

## Description

findings: add dangling_period_link, intentions_shape, intentions_over_soft_cap, and legacy_period_text to the shared report-only collector for canonical daily and period notes. Test human/JSON/nightly behavior, document the contract, and regenerate CLI documentation.

## Notes

[2026-11-19T21:01:41Z · bob-cli-nh.4.1.4] PROPOSED FOLLOW-UP: Bring the existing Mac Capture reference pages under the docs budget — `just docs-check` reports docs/reference/mac-capture/capture-previews.md at 6,171 words and docs/reference/mac-capture/keyboard.md at 6,027 words (6,000 cap); both paths are unchanged from the initially clean base tree.

[2026-11-19T22:17:09Z · bob-cli-nh.4.1.4--4] PROPOSED FOLLOW-UP: Fix the pre-existing full-verification failures confirmed on clean base. `just check` fails on both this worktree and clean-base HEAD 749efc28358f0c9b8eb0314cf3d81615a66bb3b9 (monitors 4ac505v9c4ys and wct4cayr68tm) with the same six library failures: three capture completion expectations, missing `periods update` catalog and completion decisions, and the ordered-intention-operations expectation in `native::periods::update`; the same CLI capture completion case fails with identical output. The period findings tests pass (4/4), and `cargo test --test cli periods` passes (49/49).

[2026-11-19T22:17:36Z · bob-cli-nh.4.1.4--4] Implemented the report-only period findings collector for dangling links, intentions shape, over-cap intentions, and legacy period text; added human, JSON, and nightly coverage, updated the period contract and CLI help, and regenerated reference docs with `just docs-gen` successfully. Focused verification passed: `cargo test --lib native::periods::problems` (4/4) and `cargo test --test cli periods` (49/49). Full verification: `just check` fails with the same six library and one CLI failures on this worktree and clean-base HEAD 749efc28358f0c9b8eb0314cf3d81615a66bb3b9; recorded as a proposed follow-up. `just docs-check` fails only on the two pre-existing over-budget Mac Capture pages, already recorded as a proposed follow-up. `sase bead epic-symbols bob-cli-nh.4.1.4` reported no entries. Closed this phase only.

## Dependencies

- **Depends on:** [bob-cli-nh.4.1.1](bob-cli-nh.4.1.1.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.1.4.md) | [bob-cli-nh.4.1.4](bob-cli-nh.4.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`992fd33`](https://github.com/bobs-org/bob-cli/commit/992fd33d72dcb0d0b80382666a73da94559322c1) | feat(periods): report legacy and malformed intention findings | [bob-cli-nh.4.1.4](bob-cli-nh.4.1.4.md) | 2026-11-19 17:19:17 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nh.4.1.4--4][1] | Review the follow-up proposal and completion evidence before closing this phase | 4 |
| read-by | [agent:bob-cli-nh.4.1.land][2] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.1.4.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.1.land.md

<!-- sase:referenced-by:end -->
