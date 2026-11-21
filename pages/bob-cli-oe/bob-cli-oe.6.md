# Bead: bob-cli-oe.6 — Mac Capture Pull-In card pin

[Bead Pages](../README.md) / [bob-cli-oe](README.md) / bob-cli-oe.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5m.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5m.linker.w0.md) · **Assignee:** `bob-cli-oe.6` · **Size:** medium
**Created:** 2026-11-20 17:03:15 EST · **Closed:** 2026-11-20 20:23:38 EST
**Plan:** [202611/successor\_jump\_pin.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/successor_jump_pin.md)

## Description

mac-jump-pin: add `jumpKey` to CapturePullInOutcomes. Ctrl+J is consumed by the card's router. Add the capsule with a glide animation, plus footer, button, context-menu, and VoiceOver copy. Gate `--jump-offer` on the capability, reopen after `offer_jump_stale`, and on success open the jump landing as a one-entry `bob-open-notes` URL in place of the open-notes intent.

## Notes

[2026-11-20T23:39:04Z · bob-cli-oe.6] PROPOSED FOLLOW-UP: bob-cli docs/reference/vault-format.md word budget is over cap (6016 > 6000) on clean master, failing bob-mac-capture just docs-check; trim ~20 words there

[2026-11-21T01:23:38Z · bob-cli-oe.6] Landed bf590f32: jump pin (jumpKey state, Ctrl+J router, --jump-offer gate, offer_jump_stale reopen, one-entry jump landing, capsule/footer/menu/VO copy, 20 tests, docs). Verified: 2632 portable tests green (athena), mac bundle+typecheck green, docs-check green except pre-existing vault-format budget, throwaway SHA CI 44844221318 success, master SHA bf590f32 CI 44847276397 success.

## Dependencies

- **Depends on:** [bob-cli-oe.1](bob-cli-oe.1.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-oe.7](bob-cli-oe.7.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oe.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-oe.6.md) | [bob-cli-oe.6](bob-cli-oe.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@bf590f3`](https://github.com/bobs-org/bob-mac-capture/commit/bf590f324b88126823d55db701ba73feda77520c) | feat(capture): add successor jump pin to Pull-In card | [bob-cli-oe.6](bob-cli-oe.6.md) | 2026-11-20 19:58:18 EST |
