# Bead: bob-cli-oz.6 — Mac Pull-In reason: the tasks mode and NAME stage, plus Return never confirms while the band is open

[Bead Pages](../README.md) / [bob-cli-oz](README.md) / bob-cli-oz.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.ff](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.ff.md) · **Assignee:** `bob-cli-oz.6` · **Size:** medium
**Created:** 2026-11-21 17:39:52 EST · **Closed:** 2026-11-22 00:19:10 EST
**Plan:** [202611/prompt\_task\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/prompt_task_links.md)

## Description

mac-pull-in-tasks: request -T in the Pull-In LINK band and render wikilink_task rows. It adds the BlockIDField NAME stage backed by capture-task-id and dims the reason row's own task. It also fixes Return confirming the Pull-In while the band is open, plus docs and macOS CI.

## Notes

[2026-11-22T05:18:51Z · bob-cli-oz.6] PROPOSED FOLLOW-UP: bob-cli `just docs-check` fails its published-URLs step on clean master — src/native/highlights_ref/podcast/feed.rs:70 links docs/1.0.md -> /1.0/ with no built page for /1.0; unrelated to the Mac Pull-In phase (lint step passes, reproduces without these changes).

[2026-11-22T05:19:10Z · bob-cli-oz.6] Mac Pull-In LINK band gains the tasks mode: -T requested (capability cached per executable, retries without it), wikilink_task rows with group capsules/locators/subject dimming, BlockIDField NAME stage via capture-task-id (--allow-closed for closed rows), splice of bob's wikilink_replacement as one undo step, and Return never confirms while the band is open (controller test). Verified: 2677 portable swift tests pass on athena; Scripts/macos-ci-check green on the exact snapshot (lint, build, test, bundle, launch smoke) incl. the new XCTest cases; docs lint passes net-zero (docs/wikilink-completion.md, keyboard.md, capture-previews.md). just docs-check still fails only its published-URLs step on a bob-cli page unrelated to this phase (recorded as PROPOSED FOLLOW-UP). Mac stays [[-only until a released bob ships -T.

## Dependencies

- **Depends on:** [bob-cli-oz.1](bob-cli-oz.1.md) ✓ · ⧖ 2026-11-21

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-oz.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oz.6/README.md) | [bob-cli-oz.6](bob-cli-oz.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-mac-capture | [`bob-mac-capture@355cfd9`](https://github.com/bobs-org/bob-mac-capture/commit/355cfd99e85fbd34ff45e418aeaf7d85ed9121e2) | feat(capture): complete (( task links in the Pull-In reason LINK band | [bob-cli-oz.6](bob-cli-oz.6.md) | 2026-11-22 00:20:04 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-oz.6][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-oz.6/README.md

<!-- sase:referenced-by:end -->
