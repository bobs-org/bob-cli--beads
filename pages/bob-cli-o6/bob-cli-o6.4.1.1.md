# Bead: bob-cli-o6.4.1.1 — Album card becomes the title block and owns the album title from the title slot

[Bead Pages](../README.md) / [bob-cli-o6.4.1](bob-cli-o6.4.1.md) / bob-cli-o6.4.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-o6.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.4.md) · **Assignee:** `bob-cli-o6.4.1.1` · **Size:** large
**Created:** 2026-11-20 13:42:58 EST · **Closed:** 2026-11-20 15:01:30 EST
**Plan:** [202611/collection\_cards\_title\_block.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/collection_cards_title_block.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:0db478a43c806e285e9af985 | attached via sase artifact create --bead |
| related | file:explicit:34d56e5c34205c66a34ba821 | attached via sase artifact create --bead |
| related | file:explicit:5911d19e7c9aae058cbad08d | attached via sase artifact create --bead |
| related | file:explicit:63b2e58aa15bb66b78b40933 | attached via sase artifact create --bead |
| related | file:explicit:9bff905d85249923b188a56d | attached via sase artifact create --bead |
| related | file:explicit:c1d737b81078a806eca0ce52 | attached via sase artifact create --bead |
| related | file:explicit:cc79220b38c7fa09e7f2b143 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

album-card: in bob-ledger-tools, give notebookHeaderNoteTitle the album title rule, paint the album card's title block (stack tile, ALBUM kicker with owner links, title, summary subtitle, actions) from local data before the report, fold the schema to one line by default, mount the card in the title slot with title ownership through a reusable adopter glue fragment (body fallback otherwise), update unit, preview, and album e2e checks, update docs, bump, deploy, and run the album e2e on athena.

## Notes

[2026-11-20T20:00:20Z · bob-cli-o6.4.1.1] PROPOSED FOLLOW-UP: bob-plugins album UI e2e check schema-field-jump-ctrl-j fails on athena (real Ctrl+J sent through CDP Input.dispatchKeyEvent does not move the album card editor selection; the synthetic keydown fallback does). It fails identically on a clean origin/master worktree (121 checks, same single failure), so it is not caused by the album card. No tracking bead found.

[2026-11-20T20:00:38Z · bob-cli-o6.4.1.1] PROPOSED FOLLOW-UP: scripts/obsidian-album-schema-writer-e2e.cjs --self-test with BOB_BIN=bob 0.5.0 fails with 'held-lock apply must create exactly one commit, saw 2'. It fails identically on a clean bob-plugins origin/master, so it is bob writer behavior (likely the album write plus a post-sync commit), not this phase. No tracking bead found.

[2026-11-20T20:00:44Z · bob-cli-o6.4.1.1] PROPOSED FOLLOW-UP: bob-cli docs gate fails: docs/reference/vault-format.md is over budget at 6016 words (cap 6000 for reference/) since bob-cli bb91c370 (albums tidy). npm run docs:check fails identically from a clean bob-plugins origin/master; the bob-plugins pages pass. Trim vault-format.md or split it.

[2026-11-20T20:00:51Z · bob-cli-o6.4.1.1] PROPOSED FOLLOW-UP: in Live Preview the blank lines around a hidden album H1 stay visible as empty lines (about two lines between native Properties and the first body content on eat.md). The kit range (240h propertyCardTitleSourceRangeFromLines) ends at the H1 unless a follower line follows, while the design contract says the title block includes the blank lines that follow. Consider letting the kit swallow trailing (and leading) blank lines for recognizers without followers; 240h is shared with the day and period cards, so change it in one kit phase.

[2026-11-20T20:00:57Z · bob-cli-o6.4.1.1] PROPOSED FOLLOW-UP: scripts/obsidian-album-ui-e2e.cjs passes process.env.TMPDIR to Obsidian; under SASE the agent TMPDIR is long enough that Chromium aborts with 'Socket path too long ... SingletonSocket' and the run fails with 'owned Obsidian process exited while waiting for the fixture vault window'. preview-property-cards.cjs already pins TMPDIR=/tmp in its spawn env; the album e2e (and likely the other Obsidian e2e harnesses) should do the same. Workaround used here: TMPDIR=/tmp in the command.

[2026-11-20T20:01:30Z · bob-cli-o6.4.1.1] Album card is the title block. bob-plugins commit 'feat(ledger-tools): album card owns the title block from the title slot' lands at this turn's finalization; bob-ledger-tools 1.147.0 (o6.4.1.3 f16ddea and o6.5 eed318e both shipped 1.146.0, merged here). Kit additions are additive: adopter glue 240k-plugin-property-card-title-adopt.js + exports 374c (240j/374b were taken by the bank-and-editors identity badge); o6.5 built its own 296d controller, so no glue to reuse. Album: notebookHeaderNoteTitle album rule (valid title:, H1 before ##/column-0 bullet, alias, humanized stem), local identity + card model, kit title block (stack tile, ALBUM kicker links with modifier-aware opener, title, summary subtitle, actions on the kicker row), body joins in place, record row hides only after the body, healthy schema folds to one line. Walker-footer album title aligned to the rule; 291h unchanged (Gmail subject/title, not an album reader). Dispose scope verified: every host dispose runs only from teardownLedgerToolsSurfaces() in onunload(), so no scoping change. Gates: build and build:check pass; npm test green on the f16ddea-merged tree (7929/7929); on the final eed318e-merged tree 7948/7949, the one failure the frees-marks 25 ms budget (bob-cli-io), 3/3 in isolation. docs:check fails only on bob-cli docs/reference/vault-format.md over budget, identical on clean origin/master (follow-up). Real Obsidian on athena (TMPDIR=/tmp, bob 0.5.0): album UI e2e 129/130, the only failure schema-field-jump-ctrl-j, identical on clean master (follow-up); report file:explicit:5911d19e7c9aae058cbad08d; shots Reading file:explicit:63b2e58aa15bb66b78b40933, Live file:explicit:0db478a43c806e285e9af985, 375px file:explicit:cc79220b38c7fa09e7f2b143, reveal file:explicit:34d56e5c34205c66a34ba821. vim-yank-flash --only geometry passes 23 cases incl. the album header case. album-schema-writer self-test fails identically on master (follow-up). Previews: ADOPTED_KINDS merged {bank, album}; structural 20/20, gated record/bank 8/8 pixel-identical; report file:explicit:c1d737b81078a806eca0ce52, index file:explicit:9bff905d85249923b188a56d. Changed e2e expectations: assertHeaderIntegrity(probe, {title}) now checks title slot, before Properties, data-card-kind, 'Album: <title>', hidden inline title, one visible aria-level=1; new checks reading-h1-hidden, card-identity, schema-fold-default, live-h1-hidden-and-revealed, post-tidy-title-hides-nothing, preview/live title-block-before-report and body-joins-same-node; h1less-album.md gains title: Bites (post-tidy shape). Unit expectation changes: healthy summary starts folded; an unchanged repaint keeps node and focus; the Live Preview switch fixture changes text with path. Deploy: sync refused because o6.5's pre-rebase dirty build was deployed and its bytes are in no commit; rebuilding eed318e's changes on 9b3c339 reproduced the deployed main.js and styles.css byte for byte and the manifest equals eed318e's, so per deployment.md I deployed clean eed318e with -F (backup kept), then synced 1.147.0 without -F; vault main.js, styles.css, manifest.json byte-identical to the build. No memory edits, no new beads.

## Dependencies

- **Blocks:** [bob-cli-o6.4.1.2](bob-cli-o6.4.1.2.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.4.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.4.1.1.md) | [bob-cli-o6.4.1.1](bob-cli-o6.4.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@a68e29b`](https://github.com/bobs-org/bob-plugins/commit/a68e29be2b0bb50aee47a19d65a3485c207b59bb) | feat(ledger-tools): album card owns the title block from the title slot | [bob-cli-o6.4.1.1](bob-cli-o6.4.1.1.md) | 2026-11-20 15:03:15 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-o6.4.1.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.4.1.land.md

<!-- sase:referenced-by:end -->
