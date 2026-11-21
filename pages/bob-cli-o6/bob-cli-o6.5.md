# Bead: bob-cli-o6.5 — Day and period cards always mount as the title block with a docked rail

[Bead Pages](../README.md) / [bob-cli-o6](README.md) / bob-cli-o6.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1eh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1eh.md) · **Assignee:** `bob-cli-o6.5` · **Size:** large
**Created:** 2026-11-20 11:49:17 EST · **Closed:** 2026-11-20 14:38:40 EST
**Plan:** [202611/property\_card\_title\_block.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_title_block.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:04c2de58cec3c97532141a44 | attached via sase artifact create --bead |
| related | file:explicit:526c6d191f83b84ea35eb8c1 | attached via sase artifact create --bead |
| related | file:explicit:800d52b5866507824f14ae0b | attached via sase artifact create --bead |
| related | file:explicit:8446f75d3c5fc1b954fdc8e7 | attached via sase artifact create --bead |
| related | file:explicit:ab70904ec3f5e73ecd6b1e70 | attached via sase artifact create --bead |
| related | file:explicit:d2a2c24fb1efffb5026ed1ba | attached via sase artifact create --bead |
| related | file:explicit:f41ca288c10dd6dc97169faa | attached via sase artifact create --bead |
| related | file:explicit:f644ddee5d89c2b8b81b22ad | attached via sase artifact create --bead |
| related | file:explicit:fa36383bd08442974d1067e1 | attached via sase artifact create --bead |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

day-period-cards: the intention card becomes the day card and period card: it always mounts on canonical daily, week, quarter, and year notes with a path-computed title, leaf tile, temporal accent, state pill, docked nav rail with children strip, and a set-intentions ghost on current and future subjects; recognized H1, nav, and child-link lines hide with reveal; content bands stay gated; docs, editor header, and deploy follow.

## Notes

[2026-11-20T19:38:01Z · bob-cli-o6.5] bob-cli-o3 SUPERSEDED: the set-intentions ghost shipped in day-period-cards (current and future subjects, opens the card editor on the intention stage); the land agent may close bob-cli-o3 as superseded after the obsidian-proof phase confirms it.

[2026-11-20T19:38:06Z · bob-cli-o6.5] PROPOSED FOLLOW-UP: bob-plugins test-command-mode-runner.cjs 'read budgets kill; writer budgets mark overdue; stop stops' failed once in a full npm test on athena (load average ~60) — it times read/writer budgets against the wall clock (4.8 s in the failing run). It passed 2/2 alone on this tree and 1/1 on a clean c5f5a1b worktree. No bead tracks it (bob-cli-d9 and bob-cli-dd.2 fixed a different test in the same file, the FIFO/parallel-read race). Consider gating its lifecycle on fake-bob events instead of elapsed time, as bob-cli-dd.2 did for FIFO.

[2026-11-20T19:38:29Z · bob-cli-o6.5] DAY-PERIOD-CARDS SHIPPED in bob-ledger-tools 1.146.0 (uncommitted in linked bob-plugins until this turn finalizes; commit: feat(ledger-tools): day and period cards own the title block). Rebased on origin/master 9b3c339 (bob-chips copy well; package.json test:unit merged keeping both sides). Surfaces that fell back: none — Live Preview and Reading both mount in the title slot in the real-Obsidian run.

What shipped: 296a always returns a model for valid canonical subjects (hasContent drives owned rows; malformed still fails open; H1-less notes place at the first body line). New 296ab (pure identity, state pill, kit recognizer with aliases, rail model from the recognized nav and child-link lines, ghost rule). 296b builds the kit title block (path-computed title, DAY · W47 · 2026 kicker linking the parent, leaf tile, pill, period subtitle), the ＋ Set intentions ghost button (opens the card editor on the add stage), and the docked rail with children chips (today's chip current), with unresolved marking. 296c attaches identity, recognizer, rail, ghost, and a signature (including link resolution) and opts the host into titleOwnership plus active-leaf-change and an onRefresh sweep. New 296d title-slot controller: slot mount with signature dedupe, sticky per-scope fallback on null/unstable/insert-failed (fallback never owns the title), onLost remount, LP microtask mount, Reading mount via the leaf's renderer, a sweep that frees hidden Reading cards and paints unpainted Reading panes, keys owned only with content, and link routing (Keymap.isModEvent pane types, middle click = tab, rail prev/next through bob-navigation-hotkeys open-prev/next-link in the card's pane — confirmed those commands match the daily prev/next and period ‹/› labels). 297cc card editor header shows the tile and species word. CSS: one block after the intention-card rules (card display grid/width auto, rail margin, ghost, editor identity, forced-colors, reduced motion); the old .bob-intention-card .is-unresolved rule is now scoped to body .internal-link so kit rail/kicker links keep the kit's quiet unresolved style. Docs: docs/intention-card.md retitled "Day and Period Cards" (URL kept), nav and reference link updated. Note: identity-only cards also show the existing parent-intentions line when the parent has intentions (its gate is unchanged).

Gates: npm run build and build:check clean; npm test 7924/7930 pass, 2 fail, 4 skipped — the frees-marks 25 ms budget (bob-cli-io) and the command-mode runner budget test (PROPOSED FOLLOW-UP above); both pass alone on this tree and on a clean c5f5a1b worktree. New suite test-ledger-tools-intention-card-title-block 20/20; intention-card suites updated (overlay last-remove keeps the identity-only card; placement no-H1). npm run docs:check fails only at lint on bob-cli's docs/reference/vault-format.md budget (6016/6000), identical on the clean base and already tracked on epic bob-cli-o6 note #1; bob-docs build --strict, links (0 errors), and urls pass with this checkout mounted. The plugin reference stays within its 6000-word cap.

Real-Obsidian e2e (athena, xvfb, Obsidian with real debug bob from bob-cli 2443e0a4): PASS 82/82 on the final build (main.js sha256 3c6fc190…), 85 screenshots, 0 console exceptions; one earlier attempt died at startup (Obsidian getUnpinnedLeaf race at load average 62) and the rerun passed. New checks: display-empty-identity-card, display-reveal-on-cursor, display-ghost-opens-editor, display-rail-navigates, display-period-children, display-legacy-daily, display-bytes-neutral; placement checks now assert the title slot, hidden inline title/H1/nav, exactly one visible level-1 heading, and the rail targets; fail-open checks assert native title rendering returns. Preview: preview-intention-card renders 52 captures (13 cases incl. empty-today ghost, past empty, future, week children, quarter, year, legacy); all 24 baseline captures changed only by the intended title block, rail, temporal accent, and full width (inspected). Deploy: bob plugins sync -p bob-ledger-tools refused over the landed title-slot build (vault bytes == c5f5a1b); followed the deployment.md clean-tree recipe, no -F; vault main.js, styles.css, manifest.json byte-identical to the build. Artifacts: e2e report file:explicit:8446f75d3c5fc1b954fdc8e7; preview report file:explicit:526c6d191f83b84ea35eb8c1; e2e sheets file:explicit:800d52b5866507824f14ae0b (today/week), file:explicit:f644ddee5d89c2b8b81b22ad (empty/legacy/ghost/reveal), file:explicit:ab70904ec3f5e73ecd6b1e70 (375px); preview sheets file:explicit:d2a2c24fb1efffb5026ed1ba (days), file:explicit:f41ca288c10dd6dc97169faa (periods), file:explicit:04c2de58cec3c97532141a44 (375px), file:explicit:fa36383bd08442974d1067e1 (before/after). No memory edits; no epic symbols.

[2026-11-20T19:38:40Z · bob-cli-o6.5] Closed: day and period cards ship in bob-ledger-tools 1.146.0 as the title block in Live Preview and Reading (no fallback surfaces). Verified: unit suites (new title-block suite 20/20; full npm test passes except two load-only timing tests that pass alone on this tree and on a clean base), build:check clean, docs build/links/urls pass (docs:check lint fails only on the tracked vault-format budget), real-Obsidian e2e PASS 82/82 on the final build (report file:explicit:8446f75d3c5fc1b954fdc8e7), preview matrix inspected, and the vault deploy is byte-identical to the build (deployed via the clean-tree recipe, no -F). The bob-plugins commit lands at this turn's finalization.

## Dependencies

- **Depends on:** [bob-cli-o6.1](bob-cli-o6.1.md) ✓ · ⧖ 2026-11-20
- **Depends on:** [bob-cli-o6.2](bob-cli-o6.2.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-o6.6](bob-cli-o6.6.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.5.md) | [bob-cli-o6.5](bob-cli-o6.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@eed318e`](https://github.com/bobs-org/bob-plugins/commit/eed318e0542a09d99278ff936763ab1666d6d3ee) | feat(ledger-tools): day and period cards own the title block | [bob-cli-o6.5](bob-cli-o6.5.md) | 2026-11-20 14:39:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oj.5.1.1][1] | Check open o6 phases for fragment coordination before editing 240g/styles.css | 1 |
| read-by | [agent:bob-cli-oj.5.1.2][2] | Coordination precondition: which o6 phases are open and which fragments they touch | 1 |
| read-by | [agent:bob-cli-oj.5.1.3][3] | bob-cli-o6 precondition: check open phases editing fragments I will touch | 1 |
| read-by | [agent:bob-cli-oj.6][4] | Need o6 child phase statuses to avoid editing fragments an open o6 phase is changing | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.5.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-oj.6/README.md

<!-- sase:referenced-by:end -->
