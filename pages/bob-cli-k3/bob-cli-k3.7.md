# Bead: bob-cli-k3.7 — Obsidian album cards, live chips, and the album header

[Bead Pages](../README.md) / [bob-cli-k3](README.md) / bob-cli-k3.7

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.43.linker.w0` · **Assignee:** `bob-cli-k3.7` · **Size:** large
**Created:** 2026-11-11 04:56:44 EST · **Closed:** 2026-11-12 11:18:02 EST
**Plan:** [202611/album\_and\_record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_and_record_notes.md)

## Description

plugins-albums: in bob-ledger-tools, style the `[!albums]` and `[!records]` callouts as hue-accented cards, draw live count, lead-group, peek, and freshness chips from `bob albums list -f json`, fold long index groups, render the album header with breadcrumb, add-record affordance, and schema card, and run a debounced `bob albums sync`.

## Notes

[2026-11-12T16:17:45Z · bob-cli-k3.7.1.land] LAND RECORD (album UI acceptance, bob-cli-k3.7.1.land): implemented plan 202611/album_ui_acceptance_and_land.md. Delivered scripts/obsidian-album-ui-e2e.cjs + obsidian-album-ui-e2e-lib.cjs (scratch vault via real bob, BOB_NOW fixed, BOB_CONFIG_FILE missing, cargo-metadata fresh build with BOB_BIN/BOB_CLI_BIN override) and scripts/test-obsidian-album-ui-e2e.cjs registered in package.json test:unit. Offline self-test asserts generated [!albums]/[!records] bytes, bob albums list -f json shape (index state objects, issues, groups, peek<=3, last_record), fold rule (first group 2 expanded, later liked group 13 folded with location subgroups), and probe helpers; prints offline self-test complete. Real-Obsidian CDP walkthrough on athena (xvfb, Electron binary): PASS 35 checks 0 failed across Reading+Live, light+dark, 375px narrow wrap, owner [!albums] card (counts, lead tally, peek text, last-added age, stale/missing/invalid states, never zero-when-unavailable), lead-chip group jump, [!records] folds (first expanded, later >12 folded, per-pane view state), visited/watched_on chips with distinct tooltips, breadcrumb resolve, H1-less header, Name @stem/ copy (clipboard verified Name @eat/, disabled with reason on invalid), scoped record-property hiding, malformed-JSON failure + Retry recovery, file-switch/unload cleanup, byte-identical fixture notes for presentation-only steps, one debounced albums sync ~3s after two frontmatter edits. Screenshots inspected: no overlap/clipping/focus/contrast/visibility defect in album fragments. Artifacts: report file:explicit:9ae486976c079f219df059bc, owner-reading file:explicit:6230ce612ee64dca3dd635e6, records-reading file:explicit:6d8b063162070659a9595460, narrow-375 file:explicit:87c126a8a0998ec9a8e7798, dark file:explicit:f9dffba616cbfcd014d78646, records-live file:explicit:447ce6ff62f89f134cf87d73. Docs: validation.md album paragraph, albums.md Verification section, bob-cli records.md Album cards link. Gates: npm run build ok, docs:gen stable, npm run validate 11/11, docs:check strict has only the known pre-existing validation.md:55 warning (reproduces identically on clean base, tracked kk/kb). npm test: only known clean-base failures remain (task-tag-marks session toggle 2!==1 tracked kw, reproduced on clean base; 200-link keep-moving budget load flake tracked ki, passes in isolation 14/14). just check in bob-cli passes on retry (one timing flake in subprocess_runner pipe-drain, passes in isolation). Deployment: bob plugins sync from linked checkout, 11 synced 0 drift, bob-ledger-tools + bob-navigation-hotkeys synced.

## Dependencies

- **Blocks:** [bob-cli-k3.11](bob-cli-k3.11.md) ✓ · ⧖ 2026-11-11
- **Depends on:** [bob-cli-k3.6](bob-cli-k3.6.md) ✓ · ⧖ 2026-11-11

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-k3.7](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-k3.7.md) | [bob-cli-k3.7](bob-cli-k3.7.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:research.4b.cld][1] | Check status of the plugin album header phase which covers the record property row and schema card | 1 |
| read-by | [agent:research.4b.gem][2] | Understand phase 7 scope and status for obsidian album cards and header | 1 |
| read-by | [agent:research.4b.grk][3] | Need the Obsidian album cards/header phase that should render the record field | 1 |
| read-by | [agent:research.4b.mus][4] | research record frontmatter Obsidian rendering | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.cld/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.gem/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.grk/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4b.mus/README.md

<!-- sase:referenced-by:end -->
