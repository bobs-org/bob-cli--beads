# Bead: bob-cli-om.10 — Prose-field role lint and end-to-end walkthrough

[Bead Pages](../README.md) / [bob-cli-om](README.md) / bob-cli-om.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5o.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5o.linker.w0.md) · **Assignee:** `bob-cli-om.10` · **Size:** small
**Created:** 2026-11-21 10:32:18 EST · **Closed:** 2026-11-21 16:23:56 EST
**Plan:** [202611/prose\_wikilink\_completion.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prose_wikilink_completion.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:1dc5b865bd4aaf4f57c09e94 | attached via sase artifact create --bead |
| related | file:explicit:f0b28b634d1ed5fd428c6b94 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

prose-lint: mark every text control in bob-plugins with a role (prose, literal, mixed, or none) and add a contract test that pins the S1-S15 allowlist and its wiring. Then run one isolated real-Obsidian walkthrough across representative surfaces.

## Notes

[2026-11-21T20:02:05Z · bob-cli-om.10] PROPOSED FOLLOW-UP: docs-check still reports pre-existing word-budget overruns tracked by bob-cli-ob (plugin-apis and bob-navigation-hotkeys) and bob-cli-il (bob-ledger-tools). The live Obsidian walkthrough is also pending: this runner has no executable at /snap/obsidian/current/app/obsidian and no OBSIDIAN_BIN; the isolated script self-test passes, but it cannot produce the required real-app screenshots here.

[2026-11-21T21:23:20Z · bob-cli-om.10] PROPOSED FOLLOW-UP: shared real-Obsidian harness leaves the Settings window active — scripts/obsidian-record-card-e2e.cjs trustCommunityPlugins clicks "Trust author", which opens Obsidian 1.15 Settings as a separate window that becomes window.activeWindow; under Xvfb nothing refocuses the vault window, so every Modal mounts in the Settings document (modal "open" but invisible, keys go to the editor). obsidian-prose-field-e2e.cjs now closes it via its CDP target and dispatches a main-window focus; fold that into trustCommunityPlugins so other runners that open modals stop flaking.

[2026-11-21T21:23:30Z · bob-cli-om.10] PROPOSED FOLLOW-UP: Task Card contentEl Escape branches beyond prose (theme stage 352-picker-task-card-theme-stage.js:967, relation stages 426/428) sit behind Modal.onEscapeKey in real Obsidian exactly as the prose/recall back-out did (fixed here via BulletPropertyPickerModal.onEscapeKey + pickerProseEscapeBackOut); verify their Esc layering under trusted keys and route them through onEscapeKey if they also close the whole card.

[2026-11-21T21:23:39Z · bob-cli-om.10] PROPOSED FOLLOW-UP: load-sensitive 25 ms budgets in the parallel unit list — "perf — one build over a 200-link ledger stays under 25 ms" (scripts/test-ledger-tools-event-link-times.cjs) and "200-link / 2000-task build stays within the 25 ms budget" (scripts/test-ledger-tools-frees-marks.cjs) failed at 218-540 ms during npm test with apollo load avg ~125 and passed twice in isolation on the same tree; move them to the serial test:perf list or loosen under load. Docs-check still fails only on the pre-existing budget overruns tracked by bob-cli-ob and bob-cli-il.

[2026-11-21T21:23:56Z · bob-cli-om.10] Role lint + S1-S15 contract test landed earlier (c2e28cad). This run did the real-Obsidian walkthrough on athena (Obsidian 1.15.1, Xvfb, trusted CDP keys, scratch Git vault, bob 0.5.0 sha256 9dd6ca7c): rewrote scripts/obsidian-prose-field-e2e.cjs to drive the real hosts S1 Unlink Work summary, S10 Task Card review reason+summary, S11 scheduled inline reason, S14 Intention reflection, S15 Record Card text and link (field mode). Each: [[ filter, # drill, Enter accept + held Enter, one Ctrl+Z, re-accept, Esc with band open, submit, written note text checked. Final run GO 53/53 checks, 0 console exceptions, 31 screenshots; report + 14 screenshots registered as artifacts (report attached to this bead). The walkthrough found and this run fixed 3 real nav defects: (1) field mode with a value starting [[ wrapped the whole value again ([[sase#ov -> [[sase#[[sase]]); 189-prose-field-model now hands bracketed values to the inline model; (2) trusted Escape closed S1-S5/S12/S13 prompts instead of the band because Obsidian Scope is first-registered-wins and Modal binds Escape first; 189b now front-inserts an escape-only catch-all that returns undefined when not consumed; (3) same for the Task Card (S7-S11): BulletPropertyPickerModal.onEscapeKey backs out via pickerProseEscapeBackOut first. New unit tests replicate Obsidian 1.15 Scope.handleKey and fail without the fixes. nav bumped to 2.101.0, docs:gen run, architecture.md + validation.md updated. npm test: 8388/8395 unit + 13/13 perf; the 2 failures are ledger-tools 25 ms timing budgets under load avg ~125 that pass in isolation (follow-up noted). validate 12/12. docs:check fails only on pre-existing budget overruns (bob-cli-ob, bob-cli-il). bob plugins sync deployed nav 2.101.0 (main.js 51933af2, the walkthrough build) after the clean-tree runbook; ledger-tools untouched by this run.

## Dependencies

- **Depends on:** [bob-cli-om.4](bob-cli-om.4.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-om.5](bob-cli-om.5.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-om.6](bob-cli-om.6.md) ✓ · ⧖ 2026-11-21
- **Depends on:** [bob-cli-om.7](bob-cli-om.7.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-om.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.10/README.md) | [bob-cli-om.10](bob-cli-om.10.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c2e28ca`](https://github.com/bobs-org/bob-plugins/commit/c2e28cad167df64c11f373c8c98be5d3fb79ef74) | feat(bob-plugins): lint prose field roles and add walkthrough | [bob-cli-om.10](bob-cli-om.10.md) | 2026-11-21 15:03:32 EST |
| bob-plugins | [`bob-plugins@fc806cf`](https://github.com/bobs-org/bob-plugins/commit/fc806cfeb6d92a28ee46c802a25df16cda485804) | fix(nav): back the LINK band out before Obsidian's Escape close and walk real prose hosts | [bob-cli-om.10](bob-cli-om.10.md) | 2026-11-21 16:24:56 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-om.10][1] | Need the phase scope, prior notes, and linked design file before checking what already landed | 2 |
| read-by | [agent:bob-cli-om.7][2] | see sibling phase status and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.10/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-om.7/README.md

<!-- sase:referenced-by:end -->
