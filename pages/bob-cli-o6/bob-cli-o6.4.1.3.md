# Bead: bob-cli-o6.4.1.3 — Bank Setup card and the two card editors show the species tile and word

[Bead Pages](../README.md) / [bob-cli-o6.4.1](bob-cli-o6.4.1.md) / bob-cli-o6.4.1.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-o6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.4.md) · **Assignee:** `bob-cli-o6.4.1.3` · **Size:** medium
**Created:** 2026-11-20 13:42:58 EST · **Closed:** 2026-11-20 15:13:24 EST
**Plan:** [202611/collection\_cards\_title\_block.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/collection_cards_title_block.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:06ac5bda11561f50cbb70939 | attached via sase artifact create --bead |
| related | file:explicit:74d6baad122ff5d4a098008d | attached via sase artifact create --bead |
| related | file:explicit:c18918352df0c879b13cfa09 | attached via sase artifact create --bead |
| related | file:explicit:f9426b02e3616fb0a9bd0b33 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

bank-and-editors: in bob-ledger-tools, add an additive kit identity badge (tile plus species word), put it on the bank Setup card head row with data-card-kind="bank" and an unchanged "Bank setup" aria-label, and on the Record Card and album card editor (Schema Card) modal headers, update unit, preview, and bank e2e checks and the docs header sentences, bump, deploy, and run the bank e2e on athena.

## Notes

[2026-11-20T19:31:38Z · bob-cli-o6.4.1.3] PROPOSED FOLLOW-UP: bob-cli docs/reference/vault-format.md is over its word budget (6016 > 6000 for reference/) on bob-cli master 2443e0a4 — bob-plugins `npm run docs:check` (BOB_CLI_DIR set) fails on it with a clean bob-plugins tree; no bead tracks it.

[2026-11-20T19:31:46Z · bob-cli-o6.4.1.3] PROPOSED FOLLOW-UP: real-Obsidian Ctrl+J/Ctrl+K group/field jumps fail in card editors — bank Setup e2e setup-group-jump-ctrl-k and album UI e2e schema-field-jump-ctrl-j (real key moved=false) fail identically on clean bob-plugins c5f5a1b; untracked.

[2026-11-20T19:31:50Z · bob-cli-o6.4.1.3] PROPOSED FOLLOW-UP: obsidian-bank-ui-e2e-setup.cjs aborts at "timed out waiting for bank arrangement saved after one Enter" (state preview-ready, dirty) and setup-arrange-dry-run-budget times out on preview 2 in 2 of 3 runs, all on clean c5f5a1b too; the abort skips every later Setup e2e section (processFrontMatter header, plugin-disabled), so those go unverified.

[2026-11-20T19:31:55Z · bob-cli-o6.4.1.3] PROPOSED FOLLOW-UP: obsidian-bank-ui-e2e.cjs fails queue-card-live/queue-card-reading ("missing import command"), invalid-fence, and walk-learn-coffee/walk-learn-accept (RangeError: Invalid line number 0) with identical verdicts on clean c5f5a1b; untracked.

[2026-11-20T19:32:00Z · bob-cli-o6.4.1.3] PROPOSED FOLLOW-UP: in Live Preview the bank card is an inline widget at the end of the `# 🏦 Bank` line, so it inherits the H1 font size (head, collapsed line, and buttons render at heading size; pre-existing on c5f5a1b); the new BANK badge uses --font-ui-small and reads small beside it. Consider a block widget or resetting font-size on .bob-bank-setup.

[2026-11-20T19:32:04Z · bob-cli-o6.4.1.3] PROPOSED FOLLOW-UP: obsidian-album-ui-e2e.cjs default executable /snap/obsidian/current/app/obsidian exits before the fixture vault window on athena ("owned Obsidian process exited"), as does obsidian-bank-ui-e2e.cjs with that path; -e /snap/bin/obsidian works. Default the album e2e to /snap/bin/obsidian or document it.

[2026-11-20T20:13:24Z · bob-cli-o6.4.1.3--1] Bank and card-editor species badges shipped in bob-plugins commit f16ddea (bob-ledger-tools 1.146.0), now on origin/master. The species identity badge (fragment 240j, export propertyCardBuildIdentityBadge) appears on the bank Setup card head row (data-card-kind=bank, bank tile + BANK) and on the Record Card and album card editor headers (sheet tile + RECORD, stack tile + ALBUM, above an emoji-free title). Deploy: after bob-cli-o6.5 closed, the vault already held a later dirty bob-cli_13 build. That agent landed it as a68e29b (album title block, 1.147.0), which descends from f16ddea. A clean checkout at a68e29b passed npm run build and build:check, dry-run and real bob plugins sync -p bob-ledger-tools reported up to date (0 copied, no refusal, no -F), and the stamp now reads clean at a68e29b. Vault main.js, styles.css, and manifest.json sha256 match the checkout, deployed version 1.147.0, and the deployed main.js contains the badge code. eed318e and a68e29b changed no bank, badge, Record Card, or album-editor source (they overlap only in generated files), so the bank Setup e2e was not rerun. The touched suites pass 167/167 on a68e29b. Gates on our tree: npm test green except tracked load flakes bob-cli-io and bob-cli-lp. docs:check fails only on bob-cli's vault-format.md word budget, which fails on base too (recorded as a follow-up). Real-Obsidian e2e: Bank Setup 48 pass, all 4 badge checks pass, its 2 failures and early abort also on base. Bank UI 73 pass, 5 failures identical on base. Album UI 120/121, the 1 failure also on base. Record Card 144/144. Artifacts: file:explicit:c18918352df0c879b13cfa09, file:explicit:74d6baad122ff5d4a098008d, file:explicit:06ac5bda11561f50cbb70939, file:explicit:f9426b02e3616fb0a9bd0b33. No epic symbols; no memory edits.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.4.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.4.1.3.md) | [bob-cli-o6.4.1.3](bob-cli-o6.4.1.3.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f16ddea`](https://github.com/bobs-org/bob-plugins/commit/f16ddeaad40616cad8133fbe6d93348c8b39e955) | feat(ledger-tools): show the species badge on the bank card and card editors | [bob-cli-o6.4.1.3](bob-cli-o6.4.1.3.md) | 2026-11-20 14:34:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.4.1.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.4.1.land.md

<!-- sase:referenced-by:end -->
