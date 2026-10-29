# Bead: bob-cli-dm.6.1.2 — Stable selection, explanation, and link-once intent

[Bead Pages](../README.md) / [bob-cli-dm.6.1](bob-cli-dm.6.1.md) / bob-cli-dm.6.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-dm.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.6.md) · **Assignee:** `bob-cli-dm.6.1.2` · **Size:** medium
**Created:** 2026-10-28 20:08:12 EDT · **Closed:** 2026-10-28 20:58:17 EDT
**Plan:** [202610/task\_theme\_link\_picker.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_theme_link_picker.md)

## Description

picker-intent: preserve selection by key across asynchronous refreshes, render suggestion reasons and the live field-change footer, add explicit Alt+Enter link once, and carry themeIntent through the v1 picker API with interaction tests.

## Notes

[2026-10-29T00:58:17Z · bob-cli-dm.6.1.2] Implemented picker-intent in block-id-prompt: stable key-based selection across refreshes with settled initial key, suggestion reason badges with place-dot and theme-pill hues plus accessible labels, live taskThemeOf+planThemeChange footer preview shown only for effective edits, explicit Alt+Enter link-once, and themeIntent {deliberate, linkOnce, shown} through the v1 API with strict malformed-intent dropping. Verified: npm run build, npm test (4106 passed), npm run validate (8/8), BOB_CLI_DIR docs:check (448 passed), docs inventory clean, no epic-symbols, synced block-id-prompt to the vault and confirmed the new code deployed.

## Dependencies

- **Depends on:** [bob-cli-dm.6.1.1](bob-cli-dm.6.1.1.md) ✓ · ⧖ 2026-10-28
- **Blocks:** [bob-cli-dm.6.1.3](bob-cli-dm.6.1.3.md) ✓ · ⧖ 2026-10-28

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-dm.6.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.6.1.2/README.md) | [bob-cli-dm.6.1.2](bob-cli-dm.6.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@ea583df`](https://github.com/bobs-org/bob-plugins/commit/ea583df02f832d4ea149ed9ad77fc1945ebf4c68) | feat(block-id-prompt): add stable selection, suggestion reasons, and link-once intent | [bob-cli-dm.6.1.2](bob-cli-dm.6.1.2.md) | 2026-10-28 20:59:35 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-dm.6.1.2][1] | Need the phase scope and design file | 2 |
| read-by | [agent:bob-cli-dm.6.1.land--3][2] | Need child phase 2 notes and close state before dm.6.1 closeout | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-dm.6.1.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-dm.6.1.land.md

<!-- sase:referenced-by:end -->
