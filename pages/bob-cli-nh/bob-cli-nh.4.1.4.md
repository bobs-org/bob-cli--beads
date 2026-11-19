# Bead: bob-cli-nh.4.1.4 — Period field findings and public documentation

[Bead Pages](../README.md) / [bob-cli-nh.4.1](bob-cli-nh.4.1.md) / bob-cli-nh.4.1.4

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-nh.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.md) · **Assignee:** `bob-cli-nh.4.1.4` · **Size:** medium
**Created:** 2026-11-19 13:01:12 EST
**Plan:** [202611/intention\_link\_repair.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/intention_link_repair.md)

## Description

findings: add dangling_period_link, intentions_shape, intentions_over_soft_cap, and legacy_period_text to the shared report-only collector for canonical daily and period notes. Test human/JSON/nightly behavior, document the contract, and regenerate CLI documentation.

## Notes

[2026-11-19T21:01:41Z · bob-cli-nh.4.1.4] PROPOSED FOLLOW-UP: Bring the existing Mac Capture reference pages under the docs budget — `just docs-check` reports docs/reference/mac-capture/capture-previews.md at 6,171 words and docs/reference/mac-capture/keyboard.md at 6,027 words (6,000 cap); both paths are unchanged from the initially clean base tree.

[2026-11-19T22:17:09Z · bob-cli-nh.4.1.4--4] PROPOSED FOLLOW-UP: Fix the pre-existing full-verification failures confirmed on clean base. `just check` fails on both this worktree and clean-base HEAD 749efc28358f0c9b8eb0314cf3d81615a66bb3b9 (monitors 4ac505v9c4ys and wct4cayr68tm) with the same six library failures: three capture completion expectations, missing `periods update` catalog and completion decisions, and the ordered-intention-operations expectation in `native::periods::update`; the same CLI capture completion case fails with identical output. The period findings tests pass (4/4), and `cargo test --test cli periods` passes (49/49).

## Dependencies

- **Depends on:** [bob-cli-nh.4.1.1](bob-cli-nh.4.1.1.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-nh.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-nh.4.1.4.md) | [bob-cli-nh.4.1.4](bob-cli-nh.4.1.4.md) | 0 |
