# Bead: bob-cli-mf.8 — Bank setup card arrangement parity

[Bead Pages](../README.md) / [bob-cli-mf](README.md) / bob-cli-mf.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.51.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.51.linker.w0.md) · **Assignee:** `bob-cli-mf.8` · **Size:** medium
**Created:** 2026-11-16 15:38:38 EST · **Closed:** 2026-11-16 23:16:07 EST
**Plan:** [202611/schema\_editor\_arrange\_and\_emoji.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/schema_editor_arrange_and_emoji.md)

## Description

bank-arrange: bring arrangement editing to bank categories, groups, and rules (always loud) without per-move confirm stages. Paint bob's dry-run order and hotkey shifts, check bob's order against the local one, and add region painting, Ctrl+Z semantics, and saves that survive closing the card.

## Notes

[2026-11-17T04:15:42Z · bob-cli-mf.8] PROPOSED FOLLOW-UP: Real-bob bank arrange e2e and screenshots — scripts/obsidian-bank-ui-e2e.cjs category 3-slot + group one-commit, loud rule-move one-commit, Undo restore, and light/dark screenshots of pending/hint/saving/saved. Blocked on apollo: xvfb-run and Obsidian binary are absent (DISPLAY=localhost:10.0 only).

[2026-11-17T04:16:07Z · bob-cli-mf.8] Bank setup card local arrangement shipped in bob-ledger-tools 1.126.0: groups/group:<name>/rules scopes, no per-move confirm, quiet_once Enter, G→H badges, order check skips hidden, edge clamp, region paint, Ctrl+Z, close-during-save. Verified: node --test bank-setup + arrange 41/41; npm run docs:check passed; bob plugins sync -p bob-ledger-tools --no-pull deployed; epic-symbols none. Full npm test 7118 pass / 17 fail are env/perf/unrelated (Chromium, perf budgets, navigation, block-marks dates, reduced-motion). Real-bob e2e/screenshots recorded as PROPOSED FOLLOW-UP (no xvfb-run/Obsidian on apollo).

## Dependencies

- **Depends on:** [bob-cli-mf.7](bob-cli-mf.7.md) ✓ · ⧖ 2026-11-16
- **Blocks:** [bob-cli-mf.9](bob-cli-mf.9.md) ✓ · ⧖ 2026-11-16

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-mf.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.8/README.md) | [bob-cli-mf.8](bob-cli-mf.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@3c69a57`](https://github.com/bobs-org/bob-plugins/commit/3c69a570b1f2566b0a940c61ef644336ca7678b0) | feat(ledger-tools): arrange bank categories, groups, and rules locally | [bob-cli-mf.8](bob-cli-mf.8.md) | 2026-11-16 23:17:41 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-mf.8][1] | Need notes and remaining work from earlier agents | 7 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-mf.8/README.md

<!-- sase:referenced-by:end -->
