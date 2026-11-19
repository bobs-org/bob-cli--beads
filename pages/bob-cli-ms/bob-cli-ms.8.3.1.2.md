# Bead: bob-cli-ms.8.3.1.2 — Prove Record Card entry points and guarded keyboard edits

[Bead Pages](../README.md) / [bob-cli-ms.8.3.1](bob-cli-ms.8.3.1.md) / bob-cli-ms.8.3.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ms.8.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.3.md) · **Assignee:** `bob-cli-ms.8.3.1.2` · **Size:** medium
**Created:** 2026-11-18 08:59:24 EST · **Closed:** 2026-11-19 04:08:14 EST
**Plan:** [202611/record\_card\_obsidian\_proof.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/record_card_obsidian_proof.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:5c45e0c873bf93b2fdf765be | attached via sase artifact create --bead |
| related | file:explicit:5ed730e7dc7e25751c173f79 | attached via sase artifact create --bead |
| related | file:explicit:b5d9f297d9a1816494117d5c | attached via sase artifact create --bead |
| related | file:explicit:c7152b287d5c14283393fafe | attached via sase artifact create --bead |
| related | file:explicit:cf5f71ee9a86c4b5d6f8453f | attached via sase artifact create --bead |
| related | file:explicit:d261482c78a83d29fd563381 | attached via sase artifact create --bead |
| related | file:explicit:f4d35aae42abc765e89ee7ed | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

card-workflows: extend the same CDP runner with all Record Card entry points, typed keyboard saves, Undo, refusal cases, YAML return, Schema Card navigation, and byte-neutrality checks; fix failures and publish inspected evidence.

## Notes

[2026-11-18T23:16:19Z · bob-cli-ms.8.3.1.2] Initial workflow implementation, 2026-11-18: predecessor work is landed in bob-plugins 395088a (selective native Properties hiding); primary bob-cli is unchanged at 2f1dca1ce1e29383f52957dfb01e1e8c983d8f99. Added a separate real-CDP workflow module and byte/inventory assertion helpers. Default runner scope is now full with 44 required interaction assertions; explicit --scope sheet marks all interaction assertions skipped. Covered connected toolbar/row/value/ghost/missing controls and keyboard activation, Ctrl+Shift+P, palette, actual Command Mode row, Vim == and observable negative reindents, Schema Card Ctrl+J/K and digits, Record Card Shift+J/K, YAML Done, guarded digit save and Undo, seven typed Tab stages with comma-containing list, Shift+Tab, today/clear, invalid/required/stale refusal drafts, byte boundaries and sheet freshness. Fixed test shim to forward envelope stdin and record real start/finish calls separately from dry-run previews. No production behavior or memory files changed. Updated validation docs. Focused command node --test scripts/test-obsidian-record-card-e2e.cjs scripts/test-ledger-tools-record-card.cjs scripts/test-ledger-tools-record-card-stages.cjs scripts/test-ledger-tools-record-update.cjs passes 53/53; JS syntax and git diff --check pass. epic-symbols has no entries. Athena SSH, node, Xvfb and Electron preflight pass. Real UI acceptance is NOT yet claimed. Prepared .build/record-workflows/verify.py in primary checkout for monitored build, validation, fresh exact-source Bob build, full-manifest source/binary verification on an owned Athena scratch directory, and full CDP run. Outputs are retained under .build/record-workflows/run-TIMESTAMP with latest.json pointer, summary, source manifest, command logs, JSON report and screenshots. The remaining work is real verification and any evidenced runner/product repairs, then full plugin gates, non-force sync plus required deployed-vault startup smoke, inspection/publication of every screenshot and reports, and closure of ONLY this bead. No parent/ancestor closure is authorized. Apply the documented clean-base known-red policy; do not strand this bead for already tracked timing/held-lock failures.

[2026-11-18T23:36:20Z · bob-cli-ms.8.3.1.2--1] Recovery after monitored run fwnt317ehbyj: the real Obsidian report passed all 99 sheet checks and mouse toolbar entry, then failed keyboard toolbar entry; remaining interaction checks were unexecuted and stay failed. Inspected ALL nine captured PNGs with view_image, including the focused-Edit/no-card failure state. Visual verdict preserves FAIL overall; sheet layout checks looked sound. Initial first three captures were actually 1024x800 despite a requestedWidth label of 1400, now recorded honestly; new captures read dimensions from PNG bytes. Native identity/legacy Properties remain visible as required.

Fixed proof input: native button Enter needs CDP character text CR; old helper emitted only keydown without text. Added physical codes and raw modifier key events, focused regression coverage, keyboard focus evidence, and finally capture of writer invocations even after workflow failure. No production change or version bump. Auditing writer source also showed typed Undo canonicalizes quoted choice scalars; its assertion now requires the restored value, exact unrelated record bytes, exact album bytes and all other Markdown bytes, without requiring obsolete scalar quote style. Negative tests reject changed values/body/album/other files. Today expectation uses browser local calendar date instead of a hardcoded date. 55 focused tests pass; JS syntax and diff whitespace checks pass.

Initial proof provenance: bob-cli 2f1dca1ce1e29383f52957dfb01e1e8c983d8f99, Bob 0.5.0 SHA256 a77e9734923b62d4577543d00f7c5f0d1bd76e8b241791c3cacfb3ae797c270c; plugins base 395088ab817187f9d1a3651634166d515f4cad49 plus exact file manifest SHA256 49f57b6fae8ceb51ca1c53e9c9bcd90f0f2a77063f55c67ab9e3e8a123bef1fb. Exact argv and logs are in summary/report artifacts below. Empty writer evidence from that aborted old runner is explicitly INCOMPLETE, not a no-write claim.

Fetched both origins; plugins already current; fast-forwarded CLI to a1e876cc (includes album-walk planner changes). Next .build/record-workflows/verify.py monitor will run build/docs:gen/validate, npm test, BOB_CLI_DIR=this checkout npm run docs:check, rebuild exact Bob and rerun full Athena proof; test/docs nonzero outcomes are retained without preventing real UI diagnosis. Still required: inspect every new PNG and repair any failure; compare new unrelated reds identically on clean base under existing known-red policy; fetch/integrate/rebuild before non-force bob plugins sync; mandatory post-sync deployed-vault smoke and all 31 managed hashes/participating versions; final evidence publication and closure of ONLY this bead. Prior phase notes contain the fixed-command HTTP reverse-tunnel workaround for Athena-to-Apollo SSH denial; its successful smoke is file:explicit:61bb4a9e33506642bbab8d33, summary file:explicit:ce8c9c46d442edd0b88c4d6d. Use audited artifact reads, not sibling workspaces. No memory changes/new beads. epic-symbols is empty. Bead remains in progress; all ancestors remain open.

Published failed-run evidence (all screenshots inspected):
summary.json: file:explicit:56b1574e6b0e35bf4ea531fc
record-proof.json: file:explicit:5d1c261f63d36f29858d0022
visual-verdict.json: file:explicit:8a3111f7a7d84910f684a843
writer-evidence.json: file:explicit:874301c2df2e5cc264be8258
plugin-files.json: file:explicit:bf6d3a319e8e851ea5b54ebe
real-obsidian.log: file:explicit:e94bef88d12a8f3ac716a04b
focused-54-tests.log: file:explicit:12452c26d54613d47f5c2e42
record-card-entry-toolbar.png: file:explicit:82aa701db77c409f2063c050
record-sheet-collapsed.png: file:explicit:fbdce3ff0db100da336c943a
record-sheet-fold-open.png: file:explicit:c321e2b8a1d0c450c25af487
record-sheet-frontmatter-only-reading.png: file:explicit:66efe0ebe73c4a06e1614342
record-sheet-live-dark-wide.png: file:explicit:37a7606d7c18e0d2e8ae21d4
record-sheet-live-light-375.png: file:explicit:e5742fe7fa83af9cb0de8d44
record-sheet-live-light-wide.png: file:explicit:8f804ac4c68dcc121f4e0d79
record-sheet-runner-failure.png: file:explicit:43c73e4c1a4a04da23a17a3a
record-sheet-tab-return.png: file:explicit:5d9acb32d02d9118c6b6f1af

[2026-11-18T23:36:39Z · bob-cli-ms.8.3.1.2--1] Count clarification: the failed real run had 99 passing assertions TOTAL: 98 sheet/lifecycle assertions plus entry-click-toolbar. Final focused regression result (55/55): file:explicit:69ccc73912024a54f0a5464e. Complete immutable failed-run publication index (including all nine inspected PNGs): file:explicit:f0223f5806fe8bb8cf2aabaf.

[2026-11-19T00:00:22Z · bob-cli-ms.8.3.1.2--2] Recovery after monitor m9yba86kqj93 (run-20261118-233740): 98 sheet assertions plus toolbar mouse/keyboard and row mouse passed (101 total); row keyboard focus failed and the remaining interaction workflows remain unverified. Inspected EVERY one of the nine captured PNGs with view_image. Layouts remain legible and selective native Properties hiding is intact. Failure screenshot honestly shows the editor caret rather than a focused Claim row. Original report remains FAIL. Writer capture now survives failure: 454 invocation events, zero actual record apply calls because no save workflow was reached.

Reproduced product cause in shipped CSS: the focusable .bob-record-sheet-row uses display: contents, so the wide row has no layout box despite tabindex=0. Replaced it with a grid spanning both parent columns and subgrid columns; the narrow block rule and all selective Properties selectors remain unchanged. Bumped bob-ledger-tools from 1.136.0 to the next free 1.137.0 and regenerated inventory. No Schema Card key changes; navigation-hotkeys stays 2.88.0 and command-mode 0.2.0. Added a regression for the row box/column CSS contract, retained real keyboard-entry acceptance, added computed-display/layout-box/active-element focus evidence and a focused-row PNG. A source audit also caught an escaped-newline bug in the later Vim probe; extracted and regression-tested the generated expression, including missing-fixture refusal. No other product behavior changed.

Focused verification: node --test scripts/test-obsidian-record-card-e2e.cjs scripts/test-ledger-tools-record-sheet.cjs scripts/test-ledger-tools-record-card.cjs scripts/test-ledger-tools-record-card-stages.cjs scripts/test-ledger-tools-record-update.cjs passes 96/96. Syntax and git diff --check pass; docs:gen passes. Real repair acceptance is pending, not claimed.

The completed monitored run passed npm run build, npm run docs:gen, npm run validate, cargo build --locked --bin bob and BOB_CLI_DIR=this CLI checkout npm run docs:check (447 docs tests passed, 1 skipped). npm test: 7352 tests, 7347 passed, 2 failed, 3 skipped; separate serial perf stage 5/5 passed. Both failures are exact existing known-red nodes from the parent policy: event-link-times 200-link 25 ms budget (109.2 ms, bob-cli-km) and frees-marks 200-link/2000-task 25 ms budget (107 ms, bob-cli-io). Read both trackers through the audited bead interface. No new unrelated failure, no duplicate follow-up filed. Gate classification: file:explicit:ece16aa762ae7e2c87ca1153.

Failed-run provenance: CLI a1e876cc80368d973f05a8c6c00cdab8743654dc, Bob 0.5.0 SHA256 f92cbecab3340842562928f400ecb6f0f79d54a81ca3b065efae857341f49543, plugin base 395088ab817187f9d1a3651634166d515f4cad49 and file-manifest SHA256 26acc001f508a2609bae5bef7b6c3dddb2a3246e75dcb2bfdf0ab5eaf25a60e4. Exact argv, transfer verification and source files are in summary/manifest/report artifacts. Refreshed origins for next proof; plugins already current, CLI ff-integrated to b73f4aad53c2190f96224eb68483343fd901d4d0. The next monitor will rebuild that exact Bob and rerun all gates plus the full Athena proof.

Published immutable artifact index (21 files in

… and 90359 more characters

## Dependencies

- **Depends on:** [bob-cli-ms.8.3.1.1](bob-cli-ms.8.3.1.1.md) ✓ · ⧖ 2026-11-18
- **Blocks:** [bob-cli-ms.8.3.1.3](bob-cli-ms.8.3.1.3.md) ◐ · ⧖ 2026-11-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ms.8.3.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.2.md) | [bob-cli-ms.8.3.1.2](bob-cli-ms.8.3.1.2.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`e07a26b`](https://github.com/bobs-org/bob-cli/commit/e07a26bf86b93fe12df571ac6cb00f8b71d28cca) | fix(records): preserve literal YAML values in reads and undo | [bob-cli-ms.8.3.1.2](bob-cli-ms.8.3.1.2.md) | 2026-11-19 04:10:03 EST |
| bob-plugins | [`bob-plugins@b88bc46`](https://github.com/bobs-org/bob-plugins/commit/b88bc46423e08851fb97ba6dfa7115fb1370a547) | fix(record-card): preserve drafts and prove keyboard workflows in Obsidian | [bob-cli-ms.8.3.1.2](bob-cli-ms.8.3.1.2.md) | 2026-11-19 04:10:50 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ms.8.3.1.1--c][1] | Confirm the dependent phase remains in progress as requested | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ms.8.3.1.1.md

<!-- sase:referenced-by:end -->
