# Bead: bob-cli-nu.5 — The bob-run sequence card

[Bead Pages](../README.md) / [bob-cli-nu](README.md) / bob-cli-nu.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.5` · **Size:** medium
**Created:** 2026-11-20 05:59:33 EST · **Closed:** 2026-11-20 11:42:14 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

## Description

fence: render bob-run fences as titled sequence cards. Each card has numbered monospace steps, a Run button, per-step live marks, unavailable and copy-only variants, and an armed state.

## Notes

[2026-11-20T16:41:29Z · bob-cli-nu.5] PROPOSED FOLLOW-UP: obsidian-command-chips-e2e "copy span and bob-copy card" case still only diagnoses the Live Preview copy-card press (livePreviewHit: notice-message) — the cause is the persistent Command Mode failure toasts from earlier phases covering the card's right-hand button; clearing .notice-container notices when elementFromPoint misses (as the new fencePhase clickFence does) would let that case assert the Live Preview copy.

[2026-11-20T16:41:36Z · bob-cli-nu.5] PROPOSED FOLLOW-UP: docs word budgets keep shrinking — bob-plugins docs/develop/plugin-apis.md is now 7,991/8,000 develop words (wc) after nu.5 added the mount options, and docs/bob-chips.md is ~4,190/6,000 reference words; keymap (nu.6) and author (nu.7) docs will need the planned page split already raised on bob-cli-nu.

[2026-11-20T16:42:14Z · bob-cli-nu.5] bob-run sequence card shipped in bob-plugins (bob-chips 0.12.0; committed by this turn's final declaration). New fragment plugins/bob-chips/src/085-command-fence.js registers the bob-run code-block processor (Live Preview + Reading/embeds/hover): header glyph, label or "Run · N steps", meta "N steps · <strongest effect>" (+ "· asks first"), numbered monospace steps, fixed-width Run/Output/Copy button; body clicks only select. Mounts via commandChipMount (new paint/gestureHost options) so Run, Shift+Click (openText), latch, source policy, stale check, and ⌘↵ share commandChipActivate. Live marks from the run store: ✓+duration, spinner current, ○ upcoming, ◐ attention, ■/? stopped/unknown, ✗ with first error line + per-step Output link, – skipped; header "2 of 3" / "stopped at k · <outcome>" / "finished · needs attention"; armed card = accent border + header rule via the chipAt block identity. Variants: unavailable (⊘ + "Can't run: reason (step k)", step k ✗), copy-only (copy glyph, Copy copies body byte-exact), print (title over plain listing). Store now times steps (durationMs per row; single run settles step 1). Verified: new scripts/test-command-chips-fence.cjs 14/14 (added to test:unit); all chip/copy/contract/e2e-selftest/build suites 239/239; npm test only fails the two known ledger 25 ms perf flakes (bob-cli-km, bob-cli-io; they flip pass/fail in isolation with no bob-chips involvement); npm run validate 12/12; npm run docs:gen + BOB_CLI_DIR=bob-cli docs:check pass. Chromium preview (light/dark/narrow/reduced-motion/print) 0 failures incl. fence button-width, attribute, and print checks; PNGs attached as artifacts. Real-Obsidian stub-bob e2e on athena (xvfb, scratch vault) 29/29 incl. 7 new card cases: body click never runs; Run runs 3 steps in order with live marks [done,current,upcoming] and button→Output opening the pager; Reading failure leaves ✓ ✗ – with "error: e2e failure at ffail-2" + Output link, step 3 never runs; ref/ card copies; exact invocation counts. Deployed with bob plugins sync -p bob-chips (no force); bob plugins list shows bob-chips 0.12.0 synced+enabled on apollo. Docs: docs/bob-chips.md "The bob-run card" section; plugin-apis mount options. epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-nu.4](bob-cli-nu.4.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.7](bob-cli-nu.7.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.5/README.md) | [bob-cli-nu.5](bob-cli-nu.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@59f3783`](https://github.com/bobs-org/bob-plugins/commit/59f3783d047a35484647b46c04940592a30d32d8) | feat(bob-chips): render bob-run fences as sequence cards | [bob-cli-nu.5](bob-cli-nu.5.md) | 2026-11-20 11:43:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.4.1.land][1] | Check whether the fence phase adds contracts to plugin-apis.md (word budget follow-up) | 1 |
| read-by | [agent:bob-cli-nu.5][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.land/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.5/README.md

<!-- sase:referenced-by:end -->
