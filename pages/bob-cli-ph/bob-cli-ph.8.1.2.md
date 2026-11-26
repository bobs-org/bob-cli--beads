# Bead: bob-cli-ph.8.1.2 — Tray and verbatim title on annotated preview drawer headers

[Bead Pages](../README.md) / [bob-cli-ph.8.1](bob-cli-ph.8.1.md) / bob-cli-ph.8.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ph.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.md) · **Assignee:** `bob-cli-ph.8.1.2` · **Size:** medium
**Created:** 2026-11-25 20:56:00 EST · **Closed:** 2026-11-26 00:50:50 EST
**Plan:** [202611/finish\_mac\_true\_case\_drawers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/finish_mac_true_case_drawers.md)

## Description

preview-tray: BlockDiffCard renders a Bob-annotated drawer header as SF Symbol tray plus the semibold verbatim title, muted when empty, with accessible labels and light/dark/increased-contrast render fixtures.

## Notes

[2026-11-26T04:34:37Z · bob-cli-ph.8.1.2--1] Gate diagnosis: mac typecheck failed for real — DrawerHeaderDesignTests.testRenderDrawerHeaders called throwing edgeRows() inside the VStack ViewBuilder (error at line 59) which cascaded to a key-path inference error at line 80. Fixed in c2dd7fbf by hoisting let edge = try edgeRows() above the builder; just typecheck-tests now PASS on all 4 macOS targets on rebased HEAD. Pre-existing script bug (not a product defect): /tmp/bob-cli-ph-8-1-2-gates.sh wraps the mac ssh in GNU timeout, which does not exist on macOS — reran those steps without timeout per AGENTS.md. Pushed c2dd7fbf (rebased onto b422fbdc draft-styling); docs-check passed in the gate run; macos-ci-check still to run.

[2026-11-26T05:20:37Z · bob-cli-ph.8.1.2--2] CI 45756431583 (SHA c2dd7fbf) failed 2 tests, both real assertion bugs, fixed in 5d50d5a6 and pushed (master==origin/master). (1) DrawerHeaderDesignTests expected transfer destination '› Perf Budget' but capture-transfer-drawer-merge.json names merges[0].target.drawer FUTURE WORK and containerLabel renders it verbatim — expectation corrected to '› FUTURE WORK' with comment; fixture untouched. (2) b422 (closed bead 8.1.3) paints the caret-touched drawer delimiter as bare .primary while its own test expects .labelColor; NSColor(Color.primary) is a customDynamic wrapper that never == .labelColor, so both full-ink asserts failed. Changed to Color(nsColor: .labelColor), matching the paired tertiaryLabelColor branch; no visual change. Neither failure involves preview-tray behavior. Mac scratch typecheck did NOT complete: rsync+bundle.sh passed on the scratch copy, but the just typecheck-tests ssh hung and the mac then went offline (tailscale: offline, last seen ~8m). CI Build step will compile; report macOS targets scratch-unverified. Scratch copy /tmp/bob-mac-typecheck-8-1-2 left on mac for cleanup. -r follow-up

[2026-11-26T05:22:21Z · bob-cli-ph.8.1.2--2] Visual review of drawer render fixtures from CI run 45756431583 (SHA c2dd7fbf; my 5d50d5a6 changes no rendering — string expectation + same-ink color form only). Inspected 10/16 drawer-headers PNGs: edge+real x 760/620 x light/dark/high-contrast (incl. hc-dark real, 620 narrow real+edge). All sane: outline tray distinct from checkbox/diamond, semibold verbatim titles, muted empty Drafts, removed Old Drawer struck+dimmed, legacy FUTURE WORK all-caps preserved, long title wraps sanely at both widths, no raw ** on drawer rows, Just-bold keeps its stars as a verbatim non-drawer line, requirement diamond keeps precedence, no bold/strike leakage. Remaining 6 PNGs are appearance/width recombinations of verified rows. Hashes: /tmp/drawer-png-hashes.txt (also in run 45756431583 render-fixtures artifact). No defects; no re-gate needed for visuals. -r follow-up

[2026-11-26T05:50:50Z · bob-cli-ph.8.1.2--3] preview-tray done: BlockDiffCard renders Bob-annotated drawer header as outline-tray SF Symbol plus semibold verbatim title, muted when empty, with accessible labels; light/dark/high-contrast fixtures sane. Commits 4d9e845e (tray+verbatim), c2dd7fbf (hoist throwing edgeRows out of ViewBuilder), 5d50d5a6 (fix DrawerHeaderDesignTests verbatim expectation to FUTURE WORK and delimiter full-ink to Color(nsColor:.labelColor)). CI green on base 5d50d5a6ddf46b4aa35efefbb83739734b6094f2 (snapshot fab1f219fcbc089d5e02580be0916e7a233c8394), run https://github.com/bobs-org/bob-mac-capture/actions/runs/45761321912 : Lint ok, Build ok, Test ok (incl. DrawerHeaderDesignTests.testDrawerHeadersKeepVerbatimTitles and CaptureEditorHighlightTests.testDrawerTitlesAreSemiboldAndDelimitersDimAwayFromCaret), Bundle/Verify-plist/Launch-smoke/Install ok. Render-fixtures artifact from run 45761321912: all 16 drawer-headers-*.png byte-identical to run 45756431583 inspected-clean set (diff empty; e.g. edge-760-light 3d363531bb045601b3ca0380f6a63ae8cb8bc7dca7ee283142c61ea72f295c9f, real-760-light 0932234b9f97470b96e9a98c05f9cbc7a68617bd8eb7229addba2e9ae10bfdbb). epic-symbols clean. HEAD has since moved to c561b26a (phase 8.1.4 star-expansion, parallel bead owns its gate); 8.1.2 commits are ancestors, no rebase needed. Mac scratch typecheck was superseded by green CI Build (mac was offline at fix time).

## Dependencies

- **Depends on:** [bob-cli-ph.8.1.1](bob-cli-ph.8.1.1.md) ✓ · ⧖ 2026-11-25
- **Blocks:** [bob-cli-ph.8.1.6](bob-cli-ph.8.1.6.md) ✓ · ⧖ 2026-11-25

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ph.8.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ph.8.1.2.md) | [bob-cli-ph.8.1.2](bob-cli-ph.8.1.2.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@4d9e845`](https://github.com/bobs-org/bob-mac-capture/commit/4d9e845e5a76e20d8f3b34406c9b30feba12fbbf) | feat(mac-capture): tray and verbatim title on drawer preview headers | [bob-cli-ph.8.1.2](bob-cli-ph.8.1.2.md) | 2026-11-25 23:08:02 EST |
| bob-mac-capture | [`bob-mac-capture@c2dd7fb`](https://github.com/bobs-org/bob-mac-capture/commit/c2dd7fbfdf85f6bf7679a38be318eb8d457fb41b) | fix(mac-capture): hoist throwing edgeRows out of the drawer render builder | [bob-cli-ph.8.1.2](bob-cli-ph.8.1.2.md) | 2026-11-25 23:30:44 EST |
| bob-mac-capture | [`bob-mac-capture@5d50d5a`](https://github.com/bobs-org/bob-mac-capture/commit/5d50d5a6ddf46b4aa35efefbb83739734b6094f2) | fix(mac-capture): correct drawer CI assertions and delimiter full-ink color | [bob-cli-ph.8.1.2](bob-cli-ph.8.1.2.md) | 2026-11-26 00:20:27 EST |
