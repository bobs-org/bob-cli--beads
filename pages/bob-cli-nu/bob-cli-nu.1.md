# Bead: bob-cli-nu.1 — Rename bob-copy-chips to bob-chips with no behavior change

[Bead Pages](../README.md) / [bob-cli-nu](README.md) / bob-cli-nu.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5k.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5k.linker.w0.md) · **Assignee:** `bob-cli-nu.1` · **Size:** medium
**Created:** 2026-11-20 05:59:33 EST · **Closed:** 2026-11-20 06:44:16 EST
**Plan:** [202611/command\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips.md)

## Description

rename: move the copy-chip plugin to the id bob-chips. The phase includes a dual-listed transition and a double-load guard. It updates every touchpoint: the navigation C-row lookup, docs, chezmoi allowlist, vault enablement, the vimrc obcommand ids, and a bob-cli docs redirect. Copy-chip behavior and api.copyChips v2 stay byte-stable.

## Notes

[2026-11-20T11:39:20Z · bob-cli-nu.1] PROPOSED FOLLOW-UP: Retire the dual-listed bob-copy-chips plugin after every desktop host has deployed bob-chips; remove the stale old plugin folder and enabled-list entry only after all hosts have synced, since bob plugins sync does not retire old ids.

[2026-11-20T11:39:27Z · bob-cli-nu.1] PROPOSED FOLLOW-UP: Make the timing-budget tests robust under parallel npm test load. This run failed scripts/test-ledger-tools-event-link-times.cjs (190.8 ms vs 25 ms) and scripts/test-ledger-tools-frees-marks.cjs (72 ms vs 25 ms); both passed serially (18.5 ms and 32.2 ms). Existing tracking: bob-cli-km and bob-cli-io.

[2026-11-20T11:39:35Z · bob-cli-nu.1] PROPOSED FOLLOW-UP: Repair the existing docs-check URL in docs/develop/plugins/architecture.md:74, which points to missing docs/develop/validation.md. The source file is unchanged and the target is absent in the clean base tree; no matching bead was found.

[2026-11-20T11:43:56Z · bob-cli-nu.1] PROPOSED FOLLOW-UP: Apply the vault config change to the live ~/bob checkout after these changes land, then run bob plugins sync. This turn synced only the SASE-opened vault checkout; the live bob plugins list still reports bob-chips not_installed.

[2026-11-20T11:44:16Z · bob-cli-nu.1] Renamed the plugin and its touchpoints to bob-chips; verified the dual-list guard, legacy navigation fallback, build, docs inventory, focused unit tests, and all 9 plugin performance tests. Docs generation passes; docs-check only reports an unchanged base-tree URL. npm test had two existing parallel timing flakes that passed serial rerun; the real Obsidian E2E could not run because this environment has no Obsidian binary or xvfb. Sync/list verified enabled in the SASE-opened vault checkout; the live ~/bob still needs deployment after these changes land.

## Dependencies

- **Blocks:** [bob-cli-nu.3](bob-cli-nu.3.md) ◐ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.1/README.md) | [bob-cli-nu.1](bob-cli-nu.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@bf13f43`](https://github.com/bobs-org/bob-plugins/commit/bf13f430fade45369de709523c321b72d3761ce3) | feat(plugins): rename bob-copy-chips to bob-chips | [bob-cli-nu.1](bob-cli-nu.1.md) | 2026-11-20 06:50:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.1][1] | Need the assigned phase scope, recorded progress, parent decisions, and design file before continuing the work | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.1/README.md

<!-- sase:referenced-by:end -->
