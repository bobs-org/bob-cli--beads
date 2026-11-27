# Bead: bob-cli-q5.8.1.4 — Present and act on the snoozed-task wake HUD

[Bead Pages](../README.md) / [bob-cli-q5.8.1](bob-cli-q5.8.1.md) / bob-cli-q5.8.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-q5.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.md) · **Assignee:** `bob-cli-q5.8.1.4` · **Size:** medium
**Created:** 2026-11-26 12:54:20 EST · **Closed:** 2026-11-26 19:16:27 EST
**Plan:** [202611/mac\_snooze\_wake\_notice.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/mac_snooze_wake_notice.md)

## Description

notice-hud: extract shared non-activating glass-panel infrastructure without changing existing Refs toasts, implement the accessible wake HUD and truthful Open/+15m actions, and wire the coordinator into AppDelegate.

## Notes

[2026-11-27T00:16:27Z · bob-cli-q5.8.1.4--7] Verified snoozed-task wake HUD fix at cc14132518e917f86b6f1f4fd4e0f65cd25bb562: Mac scratch format lint, bundle build, and test typecheck passed; exact-SHA macOS CI m34fem1rk35x passed all required checks on snapshot 3b69231a4288b22549275c1fc9d68719939d073e. epic-symbols reported no entries.

## Dependencies

- **Depends on:** [bob-cli-q5.8.1.3](bob-cli-q5.8.1.3.md) ✓ · ⧖ 2026-11-26
- **Blocks:** [bob-cli-q5.8.1.5](bob-cli-q5.8.1.5.md) ✓ · ⧖ 2026-11-26

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-q5.8.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.4.md) | [bob-cli-q5.8.1.4](bob-cli-q5.8.1.4.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@033b6f9`](https://github.com/bobs-org/bob-mac-capture/commit/033b6f9cf6ed87fa0a0c1c4acf7c3f2dd445f8c8) | feat(snooze): add interactive wake HUD | [bob-cli-q5.8.1.4](bob-cli-q5.8.1.4.md) | 2026-11-26 16:45:19 EST |
| bob-mac-capture | [`bob-mac-capture@ec0f899`](https://github.com/bobs-org/bob-mac-capture/commit/ec0f8997994c23fba7548512e34507f4c2aff62e) | fix(snooze): preserve the initial wake notice probe | [bob-cli-q5.8.1.4](bob-cli-q5.8.1.4.md) | 2026-11-26 17:20:21 EST |
| bob-mac-capture | [`bob-mac-capture@cc14132`](https://github.com/bobs-org/bob-mac-capture/commit/cc14132518e917f86b6f1f4fd4e0f65cd25bb562) | fix(snooze): fetch after wake notice hold settles | [bob-cli-q5.8.1.4](bob-cli-q5.8.1.4.md) | 2026-11-26 18:33:44 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-q5.8.1.4--1][1] | Need phase scope, prior notes, and current bead state before fixing its failed verification | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-q5.8.1.4.md

<!-- sase:referenced-by:end -->
