# Bead: bob-cli-o6.1 — Title-slot spike and kit mount primitive (go/no-go)

[Bead Pages](../README.md) / [bob-cli-o6](README.md) / bob-cli-o6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1eh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1eh.md) · **Assignee:** `bob-cli-o6.1` · **Size:** large
**Created:** 2026-11-20 11:49:16 EST · **Closed:** 2026-11-20 13:25:14 EST
**Plan:** [202611/property\_card\_title\_block.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/property_card_title_block.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:54ed5cd5a3b1c9ca6c6e93a7 | attached via sase artifact create --bead |
| related | file:explicit:64d464d81a9f0ae2ffe4f882 | attached via sase artifact create --bead |
| related | file:explicit:68c92af0c392d037f818b460 | attached via sase artifact create --bead |
| related | file:explicit:701020bf46a1f4159b2faf3b | attached via sase artifact create --bead |
| related | file:explicit:7445c06d4941d3f1da6db75d | attached via sase artifact create --bead |
| related | file:explicit:7c3998bd670bf99871eb2591 | attached via sase artifact create --bead |
| related | file:explicit:a6554bf2ff05cfc86047f952 | attached via sase artifact create --bead |
| related | file:explicit:a7c76d388b6c68a3b3f2f727 | attached via sase artifact create --bead |
| related | file:explicit:e3d5351361f5ec48f64c37af | attached via sase artifact create --bead |

<!-- sase:links:end -->

## Description

title-slot: build the kit primitive that mounts a property card in Obsidian's title slot (after the hidden inline title, before native Properties) in Live Preview and Reading, prove it with a real-Obsidian CDP spike on athena across switches, splits, re-renders, settings, and teardown, record a GO or NO-GO verdict with evidence on this phase bead, and deploy the unused primitive.

## Notes

[2026-11-20T18:23:47Z · bob-cli-o6.1] TITLE SLOT: GO — Live Preview and Reading both mount in the title slot; no surface or setting falls back to the body.

Evidence: real Obsidian 1.15.1 under xvfb on athena, bob-ledger-tools 1.145.0 (main.js sha256 f618e1da3c3e85f6…, built on bob-plugins ee941a1 plus this tale's commit). Three consecutive final-build runs, all GO. Required checks: live 8/8, reading 5/5, both 13/13. Settings matrix: 24/24 per surface (Properties visible/hidden/source × inline title on/off × readable line length on/off × light/dark).

Artifacts: report file:explicit:54ed5cd5a3b1c9ca6c6e93a7. Shots: Live Preview light file:explicit:7445c06d4941d3f1da6db75d, Reading light file:explicit:a7c76d388b6c68a3b3f2f727, Live Preview dark file:explicit:a6554bf2ff05cfc86047f952, Reading dark file:explicit:64d464d81a9f0ae2ffe4f882, tall 600px file:explicit:68c92af0c392d037f818b460, grown to 1400px file:explicit:e3d5351361f5ec48f64c37af, 375px Live Preview file:explicit:7c3998bd670bf99871eb2591, 375px Reading file:explicit:701020bf46a1f4159b2faf3b. All 24 shots are inspected, with verdicts in the report.

Measurements, with a 600px card grown to 1400 and shrunk to 200:
- Click to cursor: 0-line delta in 9 of 9 clicks.
- coordsAtPos: 2.2px below the .cm-line top in every phase. That is the native no-card font offset, so the card adds 0, and CodeMirror line geometry also differs by 0.
- Scroll restore (eState / history.back): Live Preview +1/+1 lines, Reading 0/0.
- Heading jump vs native: Live Preview +0.5px, Reading +1px.
- Vim: G reaches the visible last line. gg lands on the first body line, the same as native.
- Metadata re-render with the adapter paused: 0 reinserts needed across key add, change, and remove, and frontmatter added to a note without it. The card stayed before Properties.
- Viewport resize to 1400, 900, 375, and back to 1400; split panes; the same file in two panes: all placed correctly.
- Embeds, hover popover, and canvas: every mount returned null.
- Plugin disable: 0 slot nodes, 0 entries in the old module, and no re-insert after a metadata edit. Re-enable mounts through a fresh module.
- Fixture bytes unchanged; 0 console exceptions.

The spike forced four fixes into 240e:
1. Reading calls previewMode.renderer.updateHeader() after each insertion and resize. The renderer caches the .mod-header height for scroll restore and virtualization; without the call, restore was off by the card height (+17 lines).
2. Reading detaches .mod-header from the DOM when scrolled far. The primitive treats that as parked, not lost.
3. Live Preview: CodeMirror marks itself out of view and drops a pending scroll target while its whole content sits below the pane. This also happens natively: a 40-key note with no card sends its heading jump to the top. An editor update listener, registered once and inert while nothing is mounted, scrolls the content into view and keeps the measure loop running, so jumps and restores land exactly.
4. The Live Preview scroller has overflow-anchor:none, so the primitive adjusts scrollTop when an off-screen card resizes or a fresh card mounts late. Growing 600 to 1400 and back kept the top line.

API: propertyCardMountInTitleSlot(scope, node, { path, kind, view, currentPath, onLost }) returns a release handle, or null meaning body fallback. onLost(reason) means remount or fall back; the reason is denied, path-changed, disconnected, unstable, or insert-failed.
- scope is the leaf's .cm-editor (view.editor.cm.dom), or the .markdown-preview-view child of previewMode.containerEl.
- view is the CodeMirror EditorView in Live Preview and previewMode.renderer in Reading.
- Expect path-changed on every file switch within a leaf, and remount from onLost.

Adopter notes:
- With a tall card, gg leaves the card above the viewport, as tall native Properties would.
- With Properties hidden and the inline title off, Reading puts the H1 close below the card. The kit hides that H1 in adoption anyway.

[2026-11-20T18:24:04Z · bob-cli-o6.1] PROPOSED FOLLOW-UP: bob-plugins npm test 25 ms perf budgets flake under host load. These failed during this tale's gates at load average 124-208: test-ledger-tools-event-link-times.cjs ('perf — one build over a 200-link ledger stays under 25 ms' and '200-link / 2000-task build stays within the 25 ms budget') and test-navigation-dependencies-stage-performance.cjs ('stage opening builds 200/400/1000-task notes without cubic growth'). They fail the same way on a clean origin/master worktree and pass in isolation 3 of 3, so they are not caused by the title slot. No task bead tracks them. Consider load-tolerant budgets, or moving them to test:perf with retries.

[2026-11-20T18:24:08Z · bob-cli-o6.1] PROPOSED FOLLOW-UP: bob-ledger-tools keeps re-running failing bob list and report commands on ordinary workspace events. In the title-slot spike (5-note scratch vault, bob refused by a shim, 102 s of file switches and mode changes) it made 755 calls, about 7.4/s: gmail list 150, albums list 99, notebooks list 97, projects list 97, areas list 85, and bank report, config, and subscriptions 74 each. Consider caching failures or backing off while bob is missing or failing, so a broken bob does not cost a subprocess per event.

[2026-11-20T18:25:14Z · bob-cli-o6.1] Closed with TITLE SLOT: GO; both Live Preview and Reading mount in the title slot, and nothing falls back. Spike: Obsidian 1.15.1 on athena, three consecutive final-build runs GO (live 8/8, reading 5/5, both 13/13); report artifact file:explicit:54ed5cd5a3b1c9ca6c6e93a7. Primitive: 240e propertyCardMountInTitleSlot plus 374a exports, a teardown releaseAll, one inert editor update listener, and a CSS block scoped to the mount class. Unit tests: 24 in test-ledger-tools-property-card-title-slot plus the offline spike wrapper. Gates: npm run build and build:check pass, validate 12/12, docs:check passes. npm test passes except load-sensitive 25 ms perf budgets that fail identically on a clean origin/master (see PROPOSED FOLLOW-UP). Version: bob-ledger-tools 1.145.0 (identity-kit took 1.144.0). Deploy: bob plugins sync -p bob-ledger-tools with no -F, after re-stamping identity-kit's landed 6278b78 through the runbook's clean-tree recipe. Vault main.js, styles.css, and manifest.json are byte-identical to the build (main.js sha256 f618e1da3c3e85f6…). Docs: a Title slot section in docs/develop/architecture.md. The bob-plugins commit lands at this tale's finalization.

## Dependencies

- **Blocks:** [bob-cli-o6.4](bob-cli-o6.4.md) ◐ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-o6.5](bob-cli-o6.5.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-o6.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-o6.1.md) | [bob-cli-o6.1](bob-cli-o6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@c5f5a1b`](https://github.com/bobs-org/bob-plugins/commit/c5f5a1b5faf6a10a456dfa122cb26adb54bb16d9) | feat(ledger-tools): add title-slot mount primitive and real-Obsidian spike | [bob-cli-o6.1](bob-cli-o6.1.md) | 2026-11-20 13:26:11 EST |
