# Bead: bob-cli-j8.6.1 — Notebook catalog cards, live chips, and linked headers in Obsidian

[Bead Pages](../README.md) / [bob-cli-j8.6](bob-cli-j8.6.md) / bob-cli-j8.6.1

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-j8.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.6.md) · **Assignee:** `bob-cli-j8.6.1.land`
**Created:** 2026-11-09 15:15:01 EST
**Plan:** [202611/notebook\_catalog\_ui.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/notebook_catalog_ui.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/notebook_catalog_ui.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:bc690a37fdcaf7a084746ce3 | attached via sase artifact create --bead |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/notebook_catalog_ui.md

<!-- sase:links:end -->

## Description

Complete bob-cli-j8.6 with notebook catalog cards and live metadata in Reading view and Live Preview, linked notebook headers, and debounced structural sync.

## Notes

[2026-11-10T00:05:25Z · bob-cli-j8.6.1.land] FOLLOW-UP TRIAGE (all proposals from bob-cli-j8.6.1.3): #1 palette-contract failures are CAUSED BY THIS EPIC: plugin commit 56b3604 introduced #c98500 outside the palette; independently reproduced both stylesheet contract failures on 32a8545. Declined separate task; retained as required epic repair. #2 production CSS reduced-motion 90-second timeout matches existing bob-cli-fz; read prior evidence and recorded +1 with proposing phase attribution (now +6); no duplicate or new task, and no fresh browser reproduction claimed. #3 docs/reference/glossary.md generated drift is no longer reproducible: uv run --project tools/docs bob-docs gen --check passes at bob-cli 076fdc48; intervening 3f8c49d4/076fdc48 include generated glossary updates. Declined stale proposal; no task. Searched same-type and all-type tasks, swept all tasks created in the last week, and reviewed all 17 in-progress epic scopes. No active epic has a credible causal link to the existing Chromium timeout. Remaining notebook defects belong to this epic and will be in its repair tale.

[2026-11-10T00:10:48Z · bob-cli-j8.6.1.land] LAND AUDIT: Read this epic, all three closed children and every note, approved child and parent plans, plugin commits db5accf/56b3604/32a8545, actual 241a-g source/lifecycle/styles/tests, and the Rust schema-1 model. DECISIONS are preserved; UI work changes no memory/capture choices. 53 focused notebook and create-API tests pass; build:check and validate pass (9/9). Actual remaining defects: LP cleanup deletes its own widget (mounted header 1 -> 0), widget equality ignores label/hue/toggle changes, Reading embeds escape into the outer note and get removed by its renderer, stale/first-fetch errors lack visible retry state, H1-less missing catalogs lack an action, host colors use root_hue and ignore local overrides/mute, and phase .2 introduced the failing #c98500 stylesheet fallback. Startup setting refresh, ancestry completeness and scoped cleanup need integration coverage. Reproduction/evidence: file:explicit:bc690a37fdcaf7a084746ce3. Reviewed concurrent history since 2026-11-09T20:15:01Z, including fe7097f notebook-create API (must share existing refresh path), capture composition, archive pairing/writer, merge-copy and tip docs. Fast-forwarded primary to 2327590f; inspected newer plugin-base f06c7e8 Navigation-only copy changes, no notebook conflict. No epic-symbol entries; no current symvision recipe. Real smoke exits 2/unrun: /snap/bin/obsidian not executable and xvfb-run absent. No real Obsidian/visual success claimed; no full npm or just check rerun pending repairs; never ran check-full. Follow-up triage is complete in prior note. Remaining work is one medium tale whose final step closes this epic and parent phase bob-cli-j8.6 normally, marks plan:202611/notebook_catalog_ui.md done, and leaves containing epic bob-cli-j8 to its own land agent. Keep this epic open until that work and evidence are complete.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-j8.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.6.1.land.md) | [bob-cli-j8.6.1](bob-cli-j8.6.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-j8.6.1.1--1][1] | Need parent epic decisions before closing this implementation phase | 1 |
| read-by | [agent:bob-cli-j8.6.1.2][2] | Need DECISIONS block from parent epic | 2 |
| read-by | [agent:bob-cli-j8.6.1.3][3] | Need parent epic scope and decisions | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-j8.6.1.1.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.6.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-j8.6.1.3/README.md

<!-- sase:referenced-by:end -->
