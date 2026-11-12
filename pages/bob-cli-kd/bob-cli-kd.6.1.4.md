# Bead: bob-cli-kd.6.1.4 — Bank row and day-heading rendering in both Obsidian views

[Bead Pages](../README.md) / [bob-cli-kd.6.1](bob-cli-kd.6.1.md) / bob-cli-kd.6.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-kd.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kd.6.md) · **Assignee:** `bob-cli-kd.6.1.4` · **Size:** medium
**Created:** 2026-11-11 14:27:33 EST · **Closed:** 2026-11-12 06:51:40 EST
**Plan:** [202611/bank\_obsidian.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_obsidian.md)

## Description

bank-ui-marks: add Live Preview and Reading view bank decorations, mark gating, bank-property hiding, and dollar-sign math protection. Follow the bank-ui-marks section.

## Notes

[2026-11-12T11:51:23Z · bob-cli-kd.6.1.4] PROPOSED FOLLOW-UP: docs-check strict Zensical still fails on missing page bob-vim-yank-flash.md#verification in develop/plugins/validation.md; reproduced after this phase and unrelated to bank marks. Lint word budget is green. Distinct from bob-cli-kk (other broken anchors).

[2026-11-12T11:51:40Z · bob-cli-kd.6.1.4] Bank marks shipped in bob-plugins: tokenizer+presentation (241o), Live Preview widgets at Prec.highest (241p), Reading wrap+math unwrap (241q). Verified: 11/11 test-ledger-tools-bank-marks.cjs; related bank unit tests 36/36; build:check; docs:gen inventory includes toggle-bank-marks; docs lint green after compressing the bank section; bob plugins sync deployed ledger-tools to the vault (main.js +1431, styles.css +62) after restamping a stale dirty deploy from closed bob-cli-kq.3. Source mode unchanged, math protection stays on when marks are off, hub bank property hide is bank.md-only. Native Obsidian UI walkthrough is left to bob-cli-kd.6.1.5.

## Dependencies

- **Depends on:** [bob-cli-kd.6.1.3](bob-cli-kd.6.1.3.md) ✓ · ⧖ 2026-11-11
- **Blocks:** [bob-cli-kd.6.1.5](bob-cli-kd.6.1.5.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kd.6.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.4/README.md) | [bob-cli-kd.6.1.4](bob-cli-kd.6.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@4e4a580`](https://github.com/bobs-org/bob-plugins/commit/4e4a58019dc7e6fea2608ff37d6fa7a9dc9e2db9) | feat(ledger-tools): decorate bank month rows in Live Preview and Reading view | [bob-cli-kd.6.1.4](bob-cli-kd.6.1.4.md) | 2026-11-12 06:53:25 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-kd.6.1.4][1] | Need remaining notes, design, and DECISIONS | 6 |
| read-by | [agent:bob-cli-kd.6.1.5][2] | Need sibling phase close notes and evidence refs | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kd.6.1.5/README.md

<!-- sase:referenced-by:end -->
