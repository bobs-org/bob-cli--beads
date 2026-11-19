# Bead: bob-cli-ni.6 — Vault adoption, GTD prompt chips, and memory

[Bead Pages](../README.md) / [bob-cli-ni](README.md) / bob-cli-ni.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5g.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5g.linker.w0.md) · **Assignee:** `bob-cli-ni.6` · **Size:** medium
**Created:** 2026-11-19 10:05:34 EST · **Closed:** 2026-11-19 14:08:40 EST
**Plan:** [202611/copy\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/copy_chips.md)

## Description

adopt: add the gy Vim mapping, turn the GTD agent prompts into chips, reconcile with bob-cli-nh's new Summarize yesterday row, apply accepted memory decisions, and record follow-ups.

## Notes

[2026-11-19T19:07:41Z · bob-cli-ni.6] Adopted copy chips in the vault: gy mapping after the zoom-image block in obsidian_vimrc.md; six open gtd_daily.md review rows now carry last-week/last-quarter/last-year labeled chips whose payloads match the old quoted prompts. Vault-sync committed both files as bc60835f3. bob-copy-chips 0.4.0 and navigation 2.89.0 (C row) are synced and enabled. bob task reconcile applied_files=[] and left the six chip lines unchanged. glossary:copy-chip added (aliases chip, copy card fence, bob-copy). memory_decision_record was reviewer-off, so no decisions:copy-chips-are-code-spans edit. bob-cli-nh.8 has not landed Summarize yesterday; its existing COPY CHIP note already matches the shipped ``copy[summary prompt]:`` syntax, so no correcting note. Reload Obsidian on each host; apollo and the Mac also need bob plugins sync (and chezmoi apply for the allowlist) before chips render.

[2026-11-19T19:08:00Z · bob-cli-ni.6] PROPOSED FOLLOW-UP: Research phase 3 copy-chip features — vault-wide "Copy a snippet…" picker, a masked copy* variant, rich-text card copy, and a per-note opt-out. Deferred from copy_chips.md; see research:202611/obsidian_copy_chips/obsidian_copy_chips.md.

[2026-11-19T19:08:07Z · bob-cli-ni.6] PROPOSED FOLLOW-UP: Plain-text task surfaces show raw chip source — pickers, the Task Card title, and the Mac agenda still display copy[label]: payloads. An api.copyChips face helper could feed them the label/face instead of the source span.

[2026-11-19T19:08:15Z · bob-cli-ni.6] PROPOSED FOLLOW-UP: .obsidian/plugins/bob-emoji/ is tracked in vault git and missing from ~/bob/.gitignore (bob-articles through bob-vim-yank-flash are ignored; bob-emoji is not). Found while planning this epic; bob plugins list still warns about 4 tracked files.

[2026-11-19T19:08:22Z · bob-cli-ni.6] PROPOSED FOLLOW-UP: docs/copy-card.md still lists reserved keys P A F N I and omits the C chip row — ni.4 commit 0a4a91f shipped the Copy card C row in bob-navigation-hotkeys but did not update the Keys table, reserved list, or the "authored payloads live on copy chips" cross-link.

[2026-11-19T19:08:40Z · bob-cli-ni.6] Verified: bob-copy-chips 0.4.0 synced+enabled, Copy card C row in navigation 2.89.0, gy unbound then mapped nnoremap gy :bob_yank_chip after zoom-image; six open gtd_daily.md prompts parse via copyChipScanLine with byte-identical payloads (2 last-week, 2 last-quarter, 2 last-year) and no remaining quoted launch prompts; bob task reconcile applied_files=[] and chip lines unchanged; glossary:copy-chip readable after sase memory init; vault-sync landed gtd_daily.md and obsidian_vimrc.md as bc60835f3. No epic-symbol leftovers. nh.8 Summarize yesterday row not yet present; existing COPY CHIP note matches shipped syntax. Follow-ups recorded on this bead.

## Dependencies

- **Depends on:** [bob-cli-ni.4](bob-cli-ni.4.md) ✓ · ⧖ 2026-11-19
- **Depends on:** [bob-cli-ni.5](bob-cli-ni.5.md) ✓ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ni.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ni.6/README.md) | [bob-cli-ni.6](bob-cli-ni.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`f0e59e8`](https://github.com/bobs-org/bob-cli/commit/f0e59e8297dedb0180dd0a29bd5d5a6c46c67a2d) | docs(memory): add Copy Chip glossary strand | [bob-cli-ni.6](bob-cli-ni.6.md) | 2026-11-19 14:10:05 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ni.6][1] | Need notes and remaining work from prior agents | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ni.6/README.md

<!-- sase:referenced-by:end -->
