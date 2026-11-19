# Bead: bob-cli-ni.2 — Inline chips in Live Preview and Reading view

[Bead Pages](../README.md) / [bob-cli-ni](README.md) / bob-cli-ni.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5g.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5g.linker.w0.md) · **Assignee:** `bob-cli-ni.2` · **Size:** large
**Created:** 2026-11-19 10:05:33 EST · **Closed:** 2026-11-19 12:07:06 EST
**Plan:** [202611/copy\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/copy_chips.md)

## Description

inline: render copy chips as quiet pills in Live Preview and Reading view, copy on click with in-place feedback, add the cursor-line copy command, and publish api.copyChips v1.

## Notes

[2026-11-19T17:06:53Z · bob-cli-ni.2] Inline phase implemented and verified. Plugin bob-copy-chips 0.1.0->0.2.0 (main.js 9e4e6b9ccc29c22bf155c7097d743d8f3da9122ea220c76b031b05bc00723021, manifest b85c86fb1249e4c2674c254f30b1949bb0c7aaf1c7863430e34cdcd9c5da91b2, styles e6c7b51ce0655bee9550416823ef3a8a45fcd1e4cfafab5ffb8e821767e4e94f). Fragments 030-feedback, 040-chip-dom, 050-live-preview, 060-reading, 065-cursor, 070-commands wired via 010-load, 090-plugin api.copyChips v1, styles, docs, tests. Focused: 38 pass (grammar, roundtrip, cursor-api, feedback-dom, live-preview, reading, e2e self-test). Full npm test: 7427/7432 pass; 2 load-sensitive budgets (event-link-times, frees-marks) fail under parallel load but pass in isolation (19ms, 471ms). Perf: 8/8 pass incl 35ms copy-chips budget. Validate 12/12, docs inventory current, docs:check 447 passed. Real-app E2E PASS on athena (isolated scratch vault, xvfb, owned Obsidian): plugin loads, api v1, LP open, LP click clipboard ssh apollo, Reading open, Reading click a|b, table exact a|b, every vector agrees, empty/dataview plain, cursor rule, source unchanged; staged hashes matched. Deployment: dry-run then sync --repo PWD --no-pull -p bob-copy-chips on apollo, 3 copied, vault 0.2.0 synced enabled, hashes match. Post-sync smoke needs Obsidian/xvfb (absent on apollo); isolated e2e on athena is the verification. Bryan: reload Obsidian.

[2026-11-19T17:07:06Z · bob-cli-ni.2] Implemented inline copy chips (bob-copy-chips 0.2.0, api.copyChips v1) with Live Preview, Reading, cursor command, feedback, docs, tests, real-app E2E PASS on athena, and vault sync on apollo. Bryan: reload Obsidian.

## Dependencies

- **Depends on:** [bob-cli-ni.1](bob-cli-ni.1.md) ✓ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-ni.3](bob-cli-ni.3.md) ◐ · ⧖ 2026-11-19
- **Blocks:** [bob-cli-ni.4](bob-cli-ni.4.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ni.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ni.2.md) | [bob-cli-ni.2](bob-cli-ni.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@76fa3f9`](https://github.com/bobs-org/bob-plugins/commit/76fa3f92a7db0131fdb99dbd8d899e54f330e160) | feat(bob-copy-chips): inline copy chips in Live Preview and Reading view | [bob-cli-ni.2](bob-cli-ni.2.md) | 2026-11-19 12:11:47 EST |
