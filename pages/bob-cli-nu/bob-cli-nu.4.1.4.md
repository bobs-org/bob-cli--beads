# Bead: bob-cli-nu.4.1.4 — Reading, embeds, hover previews, and query source attribution

[Bead Pages](../README.md) / [bob-cli-nu.4.1](bob-cli-nu.4.1.md) / bob-cli-nu.4.1.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-nu.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nu.4.md) · **Assignee:** `bob-cli-nu.4.1.4` · **Size:** medium
**Created:** 2026-11-20 07:37:01 EST · **Closed:** 2026-11-20 09:45:17 EST
**Plan:** [202611/command\_chips\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips_inline.md)

## Description

reading: extend the single Markdown processor with accessible command buttons and render-child cleanup. Verify Tasks and Dataview source hooks, prevent dashboard paths from authorizing imported content, and test stale source and protected folders across reading surfaces.

## Notes

[2026-11-20T14:44:28Z · bob-cli-nu.4.1.4] QUERY-HOOK EVIDENCE (Obsidian 1.15.1, Tasks 8.6.0, Dataview 0.5.68; isolated scratch vault on athena via xvfb + /snap/bin/obsidian, temp profile/HOME/XDG, never the live vault; artifact file:explicit:1bc02b397cce03115b224425). Installed-source reads: Tasks TaskLineRenderer.renderDescription calls textRenderer(app, text, el, task.path, component) inside li.plugin-tasks-list-item > span.tasks-list-text > span.task-description; Tasks addGroupHeading renders h4/h5/h6.tasks-group-heading with this.tasksFile.path (the query note); Tasks backlink <a> carries no href/data-href, so it is not a usable hook. Dataview TaskItem/ListItem render <Markdown sourcePath=item.path> in li.dataview.task-list-item / li.dataview.task-list-basic-item (no data-line); TABLE/LIST/group headers/inline queries/inline fields/dataviewjs render with the query note path. Post-processor records: ordinary, embed, and hover sections run detached (no parent) WITH section info; Tasks and Dataview rows have NO section info and are sometimes detached, but the row li is already an ancestor; Obsidian exposes el.onNodeInserted. Real faces (Command Mode deliberately absent, so the state line shows which rule decided), identical in Reading and Live Preview: own dashboard chip, Tasks rows and Dataview TASK rows from notes/ = "Command Mode is not enabled" (path passed policy); the same rows from ref/ = "notes under ref/ never run commands"; Tasks group heading, Dataview TABLE cell, LIST item, dataviewjs paragraph = "source note unknown" (render path was dash.md); ref/ embed and hover preview in an allowed dashboard = ref/ refusal. The throwaway probe script stays uncommitted; the evidence phase owns the reusable stub-bob harness.

[2026-11-20T14:44:43Z · bob-cli-nu.4.1.4] PROPOSED FOLLOW-UP: baseline check failures, not caused by this phase — `npm run docs:check` passes lint (no warnings), generated drift, and the strict build, and fails only the published-URL step docs/develop/plugins/architecture.md:74 -> /develop/validation/ (bob-cli docs page outside this diff; tracked by bob-cli-nv). Full `npm test` (7718 tests) fails only the load-sensitive 25 ms perf asserts in test-ledger-tools-event-link-times.cjs and test-ledger-tools-frees-marks.cjs (40/40 green in isolation; tracked by bob-cli-km and bob-cli-io; ledger-tools untouched here).

[2026-11-20T14:44:52Z · bob-cli-nu.4.1.4] PROPOSED FOLLOW-UP: docs word budget — docs/develop/plugin-apis.md is now 7,980 words (wc) after this phase added the Reading bullet, against the 8,000-word develop/ warning cap (docs lint still reports ok). The evidence phase will push it over, so the land agent should move the command-chip runtime contracts to their own develop page (same lead as the live phase note).

[2026-11-20T14:45:00Z · bob-cli-nu.4.1.4] PROPOSED FOLLOW-UP: Reading copy-only edge — a run: chip inside a Dataview inline field value (span.dataview.inline-field) in an ordinary note is copy-only ("source note unknown"), because every .dataview subtree is treated as unverified query output. Dataview renders those values with the note own path, so a verified inline-field hook could let them run; left conservative pending real-vault demand.

[2026-11-20T14:45:17Z · bob-cli-nu.4.1.4] Reading phase landed in bob-plugins (Bob Chips 0.9.0 -> 0.10.0; deployed with bob plugins sync, bob plugins list shows bob-chips 0.10.0 synced). 060-reading.js now parses each code element once for both kinds (copy first), dispatches run spans to the new 061-reading-command.js, skips .bob-run-chip hosts, honors only the kind-aware data-bob-chip-processed marker (so an older copy-only marker never consumes a run span), and leaves run spans inside nested embed/hover/query renders to their own pass. Run spans become shared-builder <button type=button> faces mounted through commandChipMount, with one MarkdownRenderChild per pass owning unmount, attach listeners, and feedback; no MutationObserver. Provenance is separate from payload and read from the button ancestors on every paint and activation: Tasks .task-description rows and Dataview task/list item lis are verified query rows (their render sourcePath is the owner); any other block-language-*/.dataview output is "source note unknown"; embeds/hover keep their own render path, with an embed src mismatch treated as unknown; the TFile follows renames; detached buttons without section info stay copy-only until onNodeInserted/frames/hover repaint. Section info yields exact {line,from,to,raw} evidence (k-th rendered match = k-th source match, only when counts agree); otherwise activation requires the span somewhere in the note. Verified: new scripts/test-command-chips-reading.cjs 20/20 (source matrix over reading/embed/hover/Tasks/Dataview x allowed + mail/ref/ref_history/.bob/_conflicts/REF; dashboard-path query output; embed mismatch; rename into ref/; stale/disappeared; mobile, Command Mode absent/disabled/loading/unavailable; runText/openText counts, byte-exact copy, one refusal Notice, zero run/copy while rendering/hovering; Enter/Space/Shift+Enter/Shift+Click once; duplicate mounts open output; mid-run re-render and render-child teardown; detached attach repaint). All chip suites 201/201; perf 5/5. npm run build, validate pass. Full npm test 7712/7718, only the known load-sensitive ledger perf asserts (40/40 isolated; bob-cli-km/io). docs:gen done; docs:check passes lint, drift, strict build, fails only the baseline published-URL step (bob-cli-nv). Real Obsidian 1.15.1 + Tasks 8.6.0 + Dataview 0.5.68 scratch-vault probe on athena confirmed every hook in Reading and Live Preview (see evidence note and artifact file:explicit:1bc02b397cce03115b224425). Docs: bob-chips.md gains the Command chips section with the run/copy/refuse table; plugin-apis.md gains the Reading contract bullet. No epic symbols.

## Dependencies

- **Depends on:** [bob-cli-nu.4.1.3](bob-cli-nu.4.1.3.md) ✓ · ⧖ 2026-11-20
- **Blocks:** [bob-cli-nu.4.1.5](bob-cli-nu.4.1.5.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.4.1.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.4/README.md) | [bob-cli-nu.4.1.4](bob-cli-nu.4.1.4.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@f381abc`](https://github.com/bobs-org/bob-plugins/commit/f381abc5640a86c29a8e332d0b52482e55afd3dc) | feat(bob-chips): render and run command chips in Reading view | [bob-cli-nu.4.1.4](bob-cli-nu.4.1.4.md) | 2026-11-20 10:00:06 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.4.1.3][1] | Check why dependent phase is in progress already | 1 |
| read-by | [agent:bob-cli-nu.4.1.4][2] | Need the phase scope and design file | 1 |
| read-by | [agent:bob-cli-nu.4.1.5][3] | Check prior phase notes for evidence-phase handoff | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.3/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.4/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.5/README.md

<!-- sase:referenced-by:end -->
