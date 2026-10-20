# Bead: bob-cli-a0.11.1.1 — Extract capture, keyboard, and protocol reference and mount it

[Bead Pages](../README.md) / [bob-cli-a0.11.1](bob-cli-a0.11.1.md) / bob-cli-a0.11.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.11.md) · **Assignee:** `bob-cli-a0.11.1.1` · **Size:** medium
**Created:** 2026-10-20 03:05:22 EDT · **Closed:** 2026-10-20 03:26:04 EDT
**Plan:** [202610/mac\_capture\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_reference.md)

## Description

capture-reference: Create the Mac reference and developer hubs, extract the capture-side README content into bounded reference pages and an architecture page, consolidate capture protocol compatibility, and add both bob-cli mounts. Leave the README intact. Follow the capture-reference section and shared contracts below.

## Notes

[2026-10-20T07:25:49Z · bob-cli-a0.11.1.1] README-section-to-destination mapping (capture-reference): Requirements capability bullet -> protocol.md (requirements, required/optional, 22-row compatibility table); login-shell para -> protocol.md; platform/toolchain + exe paths stay in README for install.md (next phase). Runtime Contract panel/editor/inline-completion -> capture-panel.md; Active Task picker -> task-pickers.md. Task Link / Go To / Parent Task -> task-pickers.md. Dependency / Blocks / Complete behavior -> relationship-pickers.md; their preview rows -> capture-previews.md. Block ID + Name Pomodoro + named-start -> task-pickers.md. Live preview, sub-bullets/items, capture JSON, preview stack, close/start cards, pomodoro/task blocks, seed, Completing-with-!, Saving-links, successor card, =-override -> capture-previews.md. Submit/stash/cancel/Open-chip/focus/growth -> capture-panel.md. Keyboard tables, focus, stash/shelf keys, Control-\, editing+paste -> keyboard.md; draft model + 3 fenced examples -> capture-panel.md; Bob Refs shortcut rows kept verbatim in keyboard.md for refs.md (next phase) to expand. Idle agenda -> idle-agenda.md; Saved templates -> saved-templates.md; Wikilink Completion -> wikilink-completion.md (-R flow kept). Timeout/guards -> protocol.md; targets/lanes/palette/rules/guards -> develop/architecture.md. DEVIATION (repo test over plan text): hubs are bob-cli-authored landings (docs/reference|develop/mac-capture/index.md) per committed test_documented_mount_destinations_are_gitignored + gitignore allowances; Mac source ships no index.md. Interim links to Mac README anchors (#updating-..., #diagnostics-..., #privacy, #troubleshooting) retarget in later phases.

[2026-10-20T07:26:04Z · bob-cli-a0.11.1.1] capture-reference done and verified: 12 Mac pages (10 reference + architecture + empty media.yml + 2 nav.yml) extracted verbatim from README 065908f (fences checked), 2 bob-cli mounts green. just docs-check exit 0: strict zensical build, 418 pytest, search smoke 91 cases incl new Pomodoro-agenda case. Reference hubs are bob-cli-authored landings per committed mount test (deviation from plan text recorded on bead). README intact, no Swift changes.

## Dependencies

- **Blocks:** [bob-cli-a0.11.1.2](bob-cli-a0.11.1.2.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.11.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.11.1.1/README.md) | [bob-cli-a0.11.1.1](bob-cli-a0.11.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1f3b90e`](https://github.com/bobs-org/bob-cli/commit/1f3b90e5e90ab1891e42d52de8b6c4786e5ddbee) | docs(bob-cli): mount mac-capture reference pages and add hub landings | [bob-cli-a0.11.1.1](bob-cli-a0.11.1.1.md) | 2026-10-20 03:27:18 EDT |
