# Bead: bob-cli-nu.4.1.3 — Shared command-chip face and Live Preview rendering

[Bead Pages](../README.md) / [bob-cli-nu.4.1](bob-cli-nu.4.1.md) / bob-cli-nu.4.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-nu.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nu.4.md) · **Assignee:** `bob-cli-nu.4.1.3` · **Size:** medium
**Created:** 2026-11-20 07:37:01 EST · **Closed:** 2026-11-20 09:10:43 EST
**Plan:** [202611/command\_chips\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips_inline.md)

## Description

live: add the production inline DOM face and state styling, extend the existing viewport scan to both chip kinds, wire gestures and subscriptions, preserve copy behavior, and verify mixed-chip performance and rebuild continuity.

## Notes

[2026-11-20T14:10:13Z · bob-cli-nu.4.1.3] CONTRACT FOR READING/FENCE/KEYMAP (bob-chips 0.9.0): new fragments 041-command-chip-dom.js (commandChipBuildInline(doc, {label,text}, {interactive}) -> .bob-run-chip button[type=button] or role=button tabindex=0 span with .bob-run-chip-glyph(+bob-copy-chip-glyph so copy-only clicks reuse copy feedback)/-action(Run|Copy)/-face/-tip(role=tooltip, aria-describedby), aria-labelledby=action+face; commandChipPaint(host, paintModel, {plugin, chip}) repaints in place: is-<face> classes, icon replaced only on face change, step spans is-done/is-current, has-progress + --bob-run-progress gradient, aria-busy; commandChipFaceModel/PolicyText/HintText/StateLine/TipRows; commandChipAnnounceTransition dedupes per runtime by key+seq+face), 042-command-chip-mount.js (commandChipMount(plugin, host, chip, {context, gestures}) subscribes store key + catalog changes and re-keys on verdict change; context() returns fresh activation ctx WITHOUT plugin/element; commandChipUnmount never touches the run; commandChipMountRetarget; commandChipAttachGestures: primary click/tap <4px, Shift opens, Enter/Space/Shift+Enter, swallows native click after key/mouse (detail>0 or <1s after key), bare synthetic click activates once, Alt passed through as inert), 051-live-command-widget.js (run WidgetType: source path from the view editorInfoField, range {from,to,raw} absolute, chip in chipAt coords, updateDOM keeps DOM when only position moved). 050 now calls chipLiveChipsForLine (one chipScanLine pass, both kinds); copyChipLiveChipsForLine keeps its old copy-only shape. Keymap hook: set plugin.commandChipRunHotkey (live binding glyphs) to advertise "Click or <key> to run". Reading phase should build with {interactive:true} and mount with origin/readSource/snapshot/sourceVerified context; Reading still renders run spans as plain code.

[2026-11-20T14:10:20Z · bob-cli-nu.4.1.3] PROPOSED FOLLOW-UP: baseline check failures, not caused by this phase — `npm run docs:check` passes lint, generated drift, and strict build and fails only the published-URL step on docs/develop/plugins/architecture.md:74 -> /develop/validation/ (a bob-cli docs page, not in this diff; same failure the runtime phase reproduced on a clean HEAD worktree; tracked by bob-cli-nv). Full `npm test` (7698 tests) fails only the load-sensitive 25 ms perf asserts in test-ledger-tools-event-link-times.cjs and test-ledger-tools-frees-marks.cjs (40/40 green in isolation; tracked by bob-cli-km and bob-cli-io).

[2026-11-20T14:10:27Z · bob-cli-nu.4.1.3] PROPOSED FOLLOW-UP: docs word budget — docs/develop/plugin-apis.md is now 7,908 words (wc) against the 8,000-word develop/ warning cap after this phase added the Face bullet; the reading and evidence phases will push it over, so the land agent should move the command-chip contracts to their own develop page or trim (see the runtime phase note).

[2026-11-20T14:10:43Z · bob-cli-nu.4.1.3] Live phase landed in the bob-plugins working tree (Bob Chips 0.8.0 -> 0.9.0, deployed with bob plugins sync; bob plugins list shows bob-chips 0.9.0 synced). Added the shared .bob-run-chip builder/painter (041), the mount/gesture controller (042), and the Live Preview run widget (051). 050 now runs one chipScanLine pass and emits both kinds, with no second scanner or decoration pass. The manifest description names both kinds. docs/bob-chips.md gained 'Command chips in Live Preview' (it says Reading still shows plain code), and docs/develop/plugin-apis.md gained the internal Face contract. Verified: new scripts/test-command-chips-live-preview.cjs passes 16/16, covering every face, text safety and ARIA, in-place repaint without glyph recreation, both kinds on one line, inert contexts, gestures (drag, right button, leave, Alt, touch cancel, Enter/Space/Shift+Enter, native-click dedup), the double-click latch, copy-only byte-exact copy, a stale span refreshing with no run, rebuild/updateDOM continuity mid-run, per-note/span arming, announcements, and CSS rules. The perf test extension (2,000-line mixed note, 200-line viewport, real build+toDOM path) measured about 4-5 ms CPU against the 35 ms budget; identical text resolves once per catalog token and again only on a new token. All chip suites pass (148/148). npm run build and validate pass. Full npm test: 7692/7698; the only failures are the known load-sensitive ledger perf asserts (40/40 in isolation; bob-cli-km, bob-cli-io). docs:gen is done. docs:check passes lint, drift, and the strict build and fails only the baseline published-URL step (bob-cli-nv). I also rendered the faces from the production builder and styles.css in headless Chromium (light and dark) and inspected them. No epic symbols.

## Dependencies

- **Depends on:** [bob-cli-nu.4.1.2](bob-cli-nu.4.1.2.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.4.1.4](bob-cli-nu.4.1.4.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.3/README.md) | [bob-cli-nu.4.1.3](bob-cli-nu.4.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@fa28ece`](https://github.com/bobs-org/bob-plugins/commit/fa28ece28aeca2d492ac9f67ac7d3c95d58a7697) | feat(bob-chips): render and run command chips in Live Preview | [bob-cli-nu.4.1.3](bob-cli-nu.4.1.3.md) | 2026-11-20 09:11:40 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.4.1.3][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-nu.4.1.4][2] | Check prior phase notes and handoff | 1 |
| read-by | [agent:bob-cli-nu.4.1.5][3] | Check live phase notes for evidence-phase handoff | 1 |
| read-by | [agent:bob-cli-nu.4.1.land][4] | Need the child scope and notes | 1 |
| read-by | [agent:bob-cli-nu.6][5] | Check the inline phase's recorded contract for the keymap phase | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.land/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.6/README.md

<!-- sase:referenced-by:end -->
