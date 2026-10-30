# Bead: bob-cli-eq.4 — Task Wikilink Picker card and identified-link insert

[Bead Pages](../README.md) / [bob-cli-eq](README.md) / bob-cli-eq.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.b5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.b5.md) · **Assignee:** `bob-cli-eq.4` · **Size:** medium
**Created:** 2026-10-30 16:10:20 EDT · **Closed:** 2026-10-30 18:15:11 EDT
**Plan:** [202610/obsidian\_task\_wikilinks.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/obsidian_task_wikilinks.md)

## Description

picker: wire the trigger to the new card, render it beautifully, and insert links for identified rows, with Escape, Backspace, the reopen command, and reference docs.

## Notes

[2026-10-30T22:14:44Z · bob-cli-eq.4] PROPOSED FOLLOW-UP: skipped decisions:obsidian-task-wikilinks-mirror-bob — decision_record = no

[2026-10-30T22:14:49Z · bob-cli-eq.4] PROPOSED FOLLOW-UP: bob-plugins npm test still fails two ledger-tools startup tests on clean HEAD (the startup storm is linear 1!==2; relationIndex registers after layout-ready) — already tracked by bob-cli-eh

[2026-10-30T22:14:55Z · bob-cli-eq.4] PROPOSED FOLLOW-UP: bob plugins sync --repo <checkout> --no-pull refused to overwrite block-id-prompt and bob-navigation-hotkeys because bob-cli_15 has uncommitted deploys on apollo; did not pass -F

[2026-10-30T22:15:11Z · bob-cli-eq.4] Wired (( to TaskWikilinkPickerModal (bid-twl-* on the bid-tlp card), identified [[note#^id]] insert, Escape/Backspace, link-task-wikilink, and docs. Verified: npm run build; picker view+runtime 20/20; npm run validate; npm run docs:gen; BOB_CLI_DIR docs:check passed. npm test 4486 pass / 3 fail: two ledger-tools startup tests reproduce on clean HEAD (bob-cli-eh); keystroke-rank 12.1ms flake of the index budget passed in isolation. bob plugins sync --no-pull refused bob-cli_15 uncommitted deploys (no -F). decision_record=no follow-up noted. epic-symbols: none.

## Dependencies

- **Depends on:** [bob-cli-eq.2](bob-cli-eq.2.md) ✓ · ⧖ 2026-10-30
- **Depends on:** [bob-cli-eq.3](bob-cli-eq.3.md) ✓ · ⧖ 2026-10-30
- **Blocks:** [bob-cli-eq.5](bob-cli-eq.5.md) ✓ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-eq.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.4/README.md) | [bob-cli-eq.4](bob-cli-eq.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@145ea37`](https://github.com/bobs-org/bob-plugins/commit/145ea37d4abec37d017affc4dc6c490667c389f8) | feat(block-id-prompt): Task Wikilink Picker card and identified (( insert | [bob-cli-eq.4](bob-cli-eq.4.md) | 2026-10-30 18:23:25 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-eq.4][1] | Need the phase scope and design file | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-eq.4/README.md

<!-- sase:referenced-by:end -->
