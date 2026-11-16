# Bead: bob-cli-lt.8 — Accounts, Rules, and Checks in the Setup card

[Bead Pages](../README.md) / [bob-cli-lt](README.md) / bob-cli-lt.8

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1co](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1co.md) · **Assignee:** `bob-cli-lt.8` · **Size:** medium
**Created:** 2026-11-15 13:16:09 EST · **Closed:** 2026-11-15 22:38:51 EST
**Plan:** [202611/bank\_setup\_render\_and\_edit.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_setup_render_and_edit.md)

## Description

setup-card-more: add the Accounts, Rules, and Checks sections and their gestures to the Setup card.

## Notes

[2026-11-16T03:38:26Z · bob-cli-lt.8] PROPOSED FOLLOW-UP: Trim the mounted bob-ledger-tools reference back under its 6,000-word budget — docs:check reports 6302 words after this phase (6281 on clean cb885ca per bob-cli-lt.7 note #2, plus ~21 for the required Accounts/Rules/Checks card docs); see the bob-cli-lt.6 docs proposal cited there. The overage is pre-existing, so it does not block this phase.

[2026-11-16T03:38:51Z · bob-cli-lt.8] Accounts, Rules, and Checks sections live in the Bank Setup card with staged bob previews: account rows with status plus + Add (derived alias editable at birth), relabel, remove, and stale-after change/unset; numbered rule rows with + New, edit, Alt+J/K reorder, and remove; Checks findings selectable with Enter/Ctrl+E YAML jumps and the valid-state line. Verified: npm run build, build:check, validate, docs:inventory:check, all bank unit tests (181 pass incl. command-mode surface), and setup-card tests (36 pass, 5 new); bob plugins sync deployed main.js+styles.css; epic-symbols clean. docs:check overage (6302 vs 6000; 6281 pre-existing on clean tree) recorded as a proposed follow-up.

## Dependencies

- **Depends on:** [bob-cli-lt.5](bob-cli-lt.5.md) ✓ · ⧖ 2026-11-15
- **Depends on:** [bob-cli-lt.7](bob-cli-lt.7.md) ✓ · ⧖ 2026-11-15

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-lt.8](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lt.8/README.md) | [bob-cli-lt.8](bob-cli-lt.8.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@99e3410`](https://github.com/bobs-org/bob-plugins/commit/99e34103666e00b5edda98629eb40dc6ce9a7339) | feat(bank): add Accounts, Rules, and Checks to the Bank Setup card | [bob-cli-lt.8](bob-cli-lt.8.md) | 2026-11-15 22:41:08 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-lt.8][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lt.8/README.md

<!-- sase:referenced-by:end -->
