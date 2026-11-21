# Bead: bob-cli-om.6 — Intention Card fields

[Bead Pages](../README.md) / [bob-cli-om](README.md) / bob-cli-om.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5o.linker.w0.md) · **Assignee:** `bob-cli-om.6` · **Size:** medium
**Created:** 2026-11-21 10:32:18 EST · **Closed:** 2026-11-21 13:41:32 EST
**Plan:** [202611/prose\_wikilink\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md)

## Description

intention-card: attach proseField to the Intention Card's intention input, summary input, and reflection textarea (S14). The band must survive repaints and [ / ] travel, and it is the first rung of the card's back-out ladder.

## Notes

[2026-11-21T18:41:00Z · bob-cli-om.6] PROPOSED FOLLOW-UP: deploy Bob Ledger Tools 1.153.0 (S14 Intention Card LINK band) to the vault — bob plugins sync refused (no -F used): bob-ledger-tools is stamped from an uncommitted ws13 build (base 7b44b29, 2026-11-21T17:50:38Z) whose author is still running; a clean sync at upstream 2aa877ce was also refused. Run bob plugins sync once that build lands. nav, bob-mail, and block-id-prompt carry similar foreign stamps (ws19, ws10, ws13).

[2026-11-21T18:41:10Z · bob-cli-om.6] PROPOSED FOLLOW-UP: harden proseField rebind for element-replacing hosts in nav 189b — Chromium blurs the focused input when a repaint removes it, and the controller onBlur then closes an open band before rebind; rebind also never repaints the unresolved-link hint on the new host. S14 guards this in ledger-tools (capture-phase blur guard during paint plus setSourcePath after rebind), but S6, S10, and S15 rebind hosts need the same; a controller fix (defer the blur close and re-check activeElement against the rebound input, renderHint in rebind) would cover all of them.

[2026-11-21T18:41:17Z · bob-cli-om.6] Full npm test on the final tree: 8230/8237 pass. The only failures are two 25 ms wall-clock budgets (test-ledger-tools-frees-marks and event-link-times), at load average ~158; both files pass 40/40 when rerun alone on this same tree. These flakes are already tracked by task beads bob-cli-io and bob-cli-km. docs:check lint reports only the pre-existing word-budget errors on nav reference and vault-format, which om.3 already recorded and this phase did not touch.

[2026-11-21T18:41:32Z · bob-cli-om.6] S14 wired in bob-plugins ledger-tools 1.153.0. New fragment 297cd feature-detects nav proseField v1 and attaches it to the intention input, summary input, and reflection textarea. Options: links:true, recall:null, ownKeys:false, sourcePath getter () => modal.subjectPath, so it follows [ / ] travel. The band host is data-intention-band, directly under the field (297cc). Every paint rebinds the same handle to the rebuilt input and host. A capture-phase blur guard keeps Chromium's blur-on-removal from closing an open band mid-paint; a mutation check confirmed the guard is load-bearing. The handle is the first rung of intentionBackOut (Esc, Ctrl+[ via bobCardWireCloseKeys, onEscapeKey); q still types. intentionOnKeyDown offers stage keys to the handle after the pending-write swallow. Enter, Tab, and Ctrl/Cmd+Enter accept and never save; a held Enter is swallowed; reflection Shift+Enter is still a newline. The handle detaches on stage close and modal close. Fails open with no nav, an old nav, a throwing attach, or a null handle. Tests: new test-ledger-tools-intention-card-prose-field.cjs (11 tests, fake API plus the real nav controller), all intention, record, and prose-field tests green, validate 12/12, docs inventory current, docs/intention-card.md updated. Full npm test: only the known load flakes (bob-cli-io, bob-cli-km). Vault sync was refused by a foreign ws13 stamp; recorded as a follow-up, no -F used. Fragments stay at or under 1000 lines. link_text=path; no memory edits.

## Dependencies

- **Blocks:** [bob-cli-om.10](bob-cli-om.10.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-om.3](bob-cli-om.3.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-om.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.6/README.md) | [bob-cli-om.6](bob-cli-om.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@da0737b`](https://github.com/bobs-org/bob-plugins/commit/da0737b159bb9465fbb3836c8e7720f4510c1455) | feat(ledger-tools): complete \[\[ wikilinks in the Intention Card fields | [bob-cli-om.6](bob-cli-om.6.md) | 2026-11-21 14:23:32 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-om.6][1] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-om.7][2] | see sibling phase status and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.6/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.7/README.md

<!-- sase:referenced-by:end -->
