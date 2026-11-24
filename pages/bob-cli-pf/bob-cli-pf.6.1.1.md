# Bead: bob-cli-pf.6.1.1 — Prove whole-container ownership in real Obsidian

[Bead Pages](../README.md) / [bob-cli-pf.6.1](bob-cli-pf.6.1.md) / bob-cli-pf.6.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.6.md) · **Assignee:** `bob-cli-pf.6.1.1` · **Size:** medium
**Created:** 2026-11-23 20:38:15 EST · **Closed:** 2026-11-23 21:20:06 EST
**Plan:** [202611/frontmatter\_takeover.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/frontmatter_takeover.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:39fe95cda7cc68bc5008313b | attached via sase artifact create --bead |
| related | file:explicit:817ec5a2f4f13360442b081c | attached via sase artifact create --bead |
| related | file:explicit:934db24e538e78fe20a37f64 | attached via sase artifact create --bead |
| related | file:explicit:9361b027911b8426729dd3be | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

focus-proof: run and strengthen the existing S1 probe, fix bounded ownership/focus defects, and retain the observed Add file property command contract and mode verdicts. Keep production adapters unwired.

## Notes

[2026-11-24T02:19:35Z · bob-cli-pf.6.1.1] S1 GO 18/18 in real Obsidian 1.15.1 on athena (plugin 1.157.1 @ 305b637c, clean tree). Report file:explicit:934db24e538e78fe20a37f64; shots file:explicit:817ec5a2f4f13360442b081c file:explicit:9361b027911b8426729dd3be file:explicit:39fe95cda7cc68bc5008313b file:explicit:07b251a066e4c7d43f150f63 (all 4 inspected: owned notes hide the in-document Properties block in live+reading x light+dark; geometry probes confirm display:none + inert + aria-hidden). Command contract: id markdown:add-metadata-property, callbackType undefined, checkCallbackType function, dry-run true, default Mod+; binding, exactMatches 1; registered dispatch (executeCommandById, seen) and Mod+; native effect (focus lands in .metadata-property-key-input) both observed; 0 console exceptions; 79 bob spawn attempts all refused by the shim and bytes-unchanged proves no passive writes. Probe fixes (scripts/ only, no production/primitive changes): trust-dialog click before startup wait; Vim-proof CDP key shape (vk 0, code echoes key); cm.dispatch cursor placement (editor.setCursor silently no-ops in Live Preview); effect-based Mod+; proof (hotkey path bypasses executeCommandById, proven via Ctrl+P); page-keydown delivery counters on Tab paths; buffer-vs-disk typing proof (autosave window) with fast undo; top-of-doc checks start at the Live Preview frontmatter cursor clamp (anchor 0 resolves to offset 64). Adapters stay unwired: propertyCardOwnFrontmatter is only defined (240q) and exported (374), never called by album/record/temporal adapters. Full npm test 9175/9182; see PROPOSED FOLLOW-UP.

[2026-11-24T02:19:51Z · bob-cli-pf.6.1.1] PROPOSED FOLLOW-UP: flake — 25 ms perf budgets in test-ledger-tools-event-link-times.cjs (one build over a 200-link ledger, took 69 ms) and test-ledger-tools-frees-marks.cjs (200-link/2000-task build, took 169 ms) fail under full-suite parallel load on apollo but pass in isolation with and without this phase change (40/40 isolated); same known pattern already noted on bob-cli-ph.2, bob-cli-on.11.1.2, bob-cli-pf.1.1.4, bob-cli-oj.5.1.3.

[2026-11-24T02:20:06Z · bob-cli-pf.6.1.1] S1 GO 18/18 both modes in real Obsidian 1.15.1 on athena; command markdown:add-metadata-property contract recorded (checkCallback, dry-run true, Mod+; default, dispatch+effect observed); 0 console exceptions; bytes-unchanged; adapters unwired; report+4 inspected shots retained as artifacts; 2 unrelated perf-budget flakes recorded as follow-up (pass isolated).

## Dependencies

- **Blocks:** [bob-cli-pf.6.1.2](bob-cli-pf.6.1.2.md) ✓ · ⧖ 2026-11-23

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.6.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.1/README.md) | [bob-cli-pf.6.1.1](bob-cli-pf.6.1.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@8a7c8dd`](https://github.com/bobs-org/bob-plugins/commit/8a7c8dd81db809e74a13d387a51043b239558093) | test(bob-plugins): harden frontmatter-ownership S1 Obsidian probe to 18/18 | [bob-cli-pf.6.1.1](bob-cli-pf.6.1.1.md) | 2026-11-23 21:21:18 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.6.1.1][1] | Need fields | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.1/README.md

<!-- sase:referenced-by:end -->
