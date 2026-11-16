# Bead: bob-cli-m0.6 — Commands, focused-split underline, docs, acceptance, rollout

[Bead Pages](../README.md) / [bob-cli-m0](README.md) / bob-cli-m0.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.e9](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.e9.md) · **Assignee:** `bob-cli-m0.6` · **Size:** medium
**Created:** 2026-11-15 20:01:48 EST · **Closed:** 2026-11-16 09:08:28 EST
**Plan:** [202611/obsidian\_ctrl\_w\_window\_prefix.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/obsidian_ctrl_w_window_prefix.md)

## Description

finish: add palette commands and the focused-split underline, document the window keys, run the full real-Obsidian acceptance, and sync.

## Notes

[2026-11-16T14:07:10Z · bob-cli-m0.6] ACCEPTANCE (finish): real Obsidian 1.15.1 on athena (snap rev 73, xvfb). spike 14/15 (sole fail keyboard-unbound-capture is pre-existing, see follow-up), prefix 17/17, NEW visual group 28/28. Reports: /tmp/bob-wp-finish-PbU5rn/report-{spike,prefix,visual}.json, shots in sibling shots-*/ (24 visual PNGs reviewed: ring/card/receipt/underline x light/dark x 1-3 splits all calm and correct; 1-split ghost slots, 3-split minimap, palette receipt all per spec). Landed: 688 palette commands + underline (body gate + mod-active fallback, layout-change/active-leaf-change, unload cleanup), 10 unit tests, docs/window-keys.md + nav + bullet + manifest sentence (nav 2.83.1), vimrc comment line; hotkeys.json untouched per linux_ctrl_w=keep. Local gates: build:check, inventory:check, validate-manifests, 83/83 window+build+e2e-selftest all green.

[2026-11-16T14:07:30Z · bob-cli-m0.6] PROPOSED FOLLOW-UP: spike/keyboard-unbound-capture probe is stale after the prefix landing (m0.5). It asserts a bare window capture listener sees Ctrl+W first with no defaultPrevented, but the shipped prefix intentionally consumes Ctrl+W at window capture on arm (preventDefault + stopImmediatePropagation), so the probe records events=[] and fails. Reproduced identically on clean HEAD c725370 (14/15, same single fail), so pre-existing and unrelated to finish. Fix in a follow-up: update the spike probe to the armed-consume reality (or retire finding 4a), keeping prefix-group coverage as the authority.

[2026-11-16T14:07:44Z · bob-cli-m0.6] PROPOSED FOLLOW-UP: docs-check documentation unit test test_every_capture_token_has_a_literal_query_at_its_heading fails on this base (//<query> at #double-slash-picker), reproduced with an untouched bob-cli checkout and independent of the window-keys docs (no capture tokens added; lint budget passes at 6006->under after trims). Needs a docs owner to fix the token anchor or the test.

[2026-11-16T14:08:03Z · bob-cli-m0.6] PROPOSED FOLLOW-UP (blocks final vault deploy): bob plugins sync refuses -F-less overwrite: vault nav bundle is a stale pre-commit mix (2.83.0, missing 4288af6 tier logic + finish) stamped from abandoned ws13 uncommitted build; ws13/ws14 agents not running (only ws0, ws10). Verified zero novel work in vault bundle: all 27 vault-only main.js lines are stale variants of committed symbols (settleReviewWalkLock etc. all present in committed src). Safe resume for land agent or Bryan: review the diff, then run: bob plugins sync --repo /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/linked/bob-plugins --no-pull -p bob-navigation-hotkeys -F. Ledger-tools refusal (ws14) is unrelated to this phase; do not force it.

[2026-11-16T14:08:28Z · bob-cli-m0.6] Finish verified: 6 palette commands + focused-split underline shipped (nav 2.83.1) with 10 new unit tests; window/build/e2e-selftest 83/83 green; docs gates pass (budget + inventory + lint); real-Obsidian 1.15.1 acceptance prefix 17/17 and new visual group 28/28 with 24 reviewed screenshots, no polish issues; spike 14/15 where the single fail is a pre-existing stale probe confirmed identical on clean HEAD. Vault deploy blocked by abandoned ws13 stale bundle (zero-loss evidenced, exact -F resume in bead notes for land agent); ledger-tools refusal unrelated; docs token-coverage failure pre-existing. linux_ctrl_w=keep honored (hotkeys.json untouched); window_prefix_record=no honored (no memory edits).

## Dependencies

- **Depends on:** [bob-cli-m0.5](bob-cli-m0.5.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-m0.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.6/README.md) | [bob-cli-m0.6](bob-cli-m0.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@0e16e30`](https://github.com/bobs-org/bob-plugins/commit/0e16e304142f94c70c78357f7bdfe4ded19d0db5) | feat(navigation): add Ctrl+W palette commands, focused-split underline, window-keys docs, and visual acceptance | [bob-cli-m0.6](bob-cli-m0.6.md) | 2026-11-16 09:12:12 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-m0.5][1] | Need to know whether the finish phase is already editing shared plugin files | 1 |
| read-by | [agent:bob-cli-m0.6][2] | Need the phase scope and design file | 2 |
| read-by | [agent:research.4y.cld][3] | Find the visual acceptance screenshots and findings for the shipped Ctrl+W hint to design Ctrl+W N tab hints | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.5/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-m0.6/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.4y.cld/README.md

<!-- sase:referenced-by:end -->
