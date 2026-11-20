# Bead: bob-cli-nu.4.1.5 — Visual previews, isolated Obsidian acceptance, and documentation

[Bead Pages](../README.md) / [bob-cli-nu.4.1](bob-cli-nu.4.1.md) / bob-cli-nu.4.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-nu.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-nu.4.md) · **Assignee:** `bob-cli-nu.4.1.5` · **Size:** medium
**Created:** 2026-11-20 07:37:01 EST · **Closed:** 2026-11-20 10:42:46 EST
**Plan:** [202611/command\_chips\_inline.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/command_chips_inline.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:bba2a234f264129a97f260c8 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

evidence: add production-backed light/dark previews and an isolated stub-bob Obsidian harness with offline self-tests; finish reference docs and run required gates. Record deploy and acceptance evidence for the child epic land agent; do not close bob-cli-nu.4 yourself.

## Notes

[2026-11-20T15:42:00Z · bob-cli-nu.4.1.5] PROPOSED FOLLOW-UP: bob-cli docs drift, not caused by this phase — bob-cli HEAD b7007011 (docs(memory): add intention and property-card glossary family) left docs/reference/glossary.md stale, so `npm run docs:check` against the workspace bob-cli stops at generated drift ("out of date: docs/reference/glossary.md (run just docs-gen)"). `uv run --project tools/docs bob-docs gen` in a clean bob-cli worktree regenerates only that file. With it regenerated, docs:check passes lint, drift, and the strict build and fails only the known published-URL step docs/develop/plugins/architecture.md:74 -> /develop/validation/ (bob-cli-nv).

[2026-11-20T15:42:13Z · bob-cli-nu.4.1.5] PROPOSED FOLLOW-UP: baseline npm test failures, not caused by this phase — full `npm test` (7751 unit + 11 perf) fails only the load-sensitive 25 ms asserts in test-ledger-tools-event-link-times.cjs and test-ledger-tools-frees-marks.cjs (40/40 in isolation; tracked by bob-cli-km and bob-cli-io).

[2026-11-20T15:42:21Z · bob-cli-nu.4.1.5] PROPOSED FOLLOW-UP: Reading-view wrap shape (low) — Chromium lays out <button> with display:inline as inline-block, so a long command chip in Reading view (and a long copy chip, which shares this) wraps inside its own box instead of flowing inline with cloned box decoration as in Live Preview. Text stays untruncated. See the preview artifact file:explicit:7212d2aecc939e1063dfd635 (Literal rows, narrow column). The plan requires real buttons in Reading, so this is recorded rather than changed.

[2026-11-20T15:42:46Z · bob-cli-nu.4.1.5] Evidence phase landed in the bob-plugins working tree (Bob Chips 0.10.0 -> 0.11.0; deployed with bob plugins sync; bob plugins list shows bob-chips 0.11.0 and bob-command-mode 0.4.0 synced and enabled; reload Obsidian for the CSS fix). (1) scripts/preview-command-chips.cjs + .template.html load the built bob-chips main.js and styles.css into Chromium: chipScanLine, both builders, a real CommandChipRunStore driven through onState shapes, commandChipPaintModel, and commandChipPaint, with verdicts from Command Mode cmResolveCommandText against the shared fixture catalog. It renders 63 faces covering every state, label and literal 3-step sequences (rest, step 2 of 3, failed at 2), alias, skips-preview, confirm, and report policy lines, copy-only (ref/, mail/, unknown query, mobile, CM off), loading, host, excluded, and shell refusals, mixed copy/run lines, a 240px column and a 390px viewport, hover tooltips, and keyboard focus. Captures: light, dark, narrow, reduced-motion, and print. In-page checks: each face matches its expected row, 1740 attributes are payload-free, ARIA is action+face, run-state geometry delta is 0, reduced motion has no spin or pulse, and print is plain for every state. The print check found a real CSS bug: the @media print reset lost on specificity to the two-class state rules, so dashes, the unavailable fill, the progress underline, and the completed pulse printed (29 failures on the old CSS). Fixed with .bob-run-chip[class] (0 failures); labels keep the text font, as copy-chip labels do. (2) scripts/obsidian-command-chips-e2e{,-lib}.cjs is an isolated stub-bob harness: one /tmp run root for profile, HOME, XDG, and vault; Command Mode bobPath names the stub; the stub is first on PATH; there are no bob candidates; the stub logs every invocation and writes only its own scratch note; the runner refuses to launch on any isolation failure. Offline --self-test runs the stub as Obsidian children would. Wrappers scripts/test-obsidian-command-chips-e2e.cjs and scripts/test-command-chips-preview.cjs are registered in test:unit. Real run on athena (Obsidian 1.15.1, Tasks 8.6.0, Dataview 0.5.68, xvfb, trusted CDP clicks): E2E PASS 23/23, covering every plan acceptance item 1-6 including the exact invocation set (see matrix). (3) Docs: bob-chips.md gains an intro run: line, a "What a command chip can never do" bounds section (bounds verified against the resolver), and the print wording; develop/validation.md documents the preview and e2e. plugin-apis.md is untouched (no API change; it is at 7980/8000 words). Gates: build, validate, and docs:gen pass. npm test passes 7744/7751 unit and 11/11 perf; the only failures are baseline ledger perf asserts (40/40 isolated; bob-cli-km/io). All chip suites pass 205/205. docs:check fails only on baselines: the bob-cli glossary drift from b7007011, and with that regenerated, only the published-URL step (bob-cli-nv). Artifacts: acceptance matrix file:explicit:bba2a234f264129a97f260c8; preview light/dark/narrow/reduced/print file:explicit:7212d2aecc939e1063dfd635, 51916594280c9ca9edeef12c, 522000a9a7b94b60ddcc6579, bae9165f5516d9297f31faef, 2b1821e3835f64353551eb30; preview report and checks e64e8ddf3bca9aa174b1ef93, 004bf9288210b83d6d64c7fa; Obsidian e2e screenshots 648bc17c533ab31c7ceb5d6e, 51ab04edfbf28c16bab350a5; e2e report 513477250e4fe86807e0861e. No epic symbols. The ancestors (nu.4.1, nu.4) were left for the land agent.

## Dependencies

- **Depends on:** [bob-cli-nu.4.1.4](bob-cli-nu.4.1.4.md) ✓ · ⧖ 2026-11-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-nu.4.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.5/README.md) | [bob-cli-nu.4.1.5](bob-cli-nu.4.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@b52dd3f`](https://github.com/bobs-org/bob-plugins/commit/b52dd3fcba720bbf4c799d163572f36a2cca9e9b) | feat(bob-chips): add command-chip previews, stub-bob Obsidian e2e, and print fix | [bob-cli-nu.4.1.5](bob-cli-nu.4.1.5.md) | 2026-11-20 10:43:46 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-nu.4.1.4][1] | Check why dependent phase is in progress already | 1 |
| read-by | [agent:bob-cli-nu.4.1.5][2] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.4/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-nu.4.1.5/README.md

<!-- sase:referenced-by:end -->
