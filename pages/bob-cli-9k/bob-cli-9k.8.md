# Bead: bob-cli-9k.8 — Finish Pomodoro homes — contract parity, review time, override labels, and panel fixes

[Bead Pages](../README.md) / [bob-cli-9k](README.md) / bob-cli-9k.8

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-9k.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.land.md) · **Assignee:** `bob-cli-9k.8.land`
**Created:** 2026-10-18 20:20:11 EDT
**Plan:** [202610/pomodoro\_homes\_landing.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes_landing.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/pomodoro_homes_landing.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | file:explicit:0f1409dbf3236065be038cb1 | attached via sase artifact create --bead |
| related | file:explicit:d590262a37f7c98de4bfc541 | attached via sase artifact create --bead |

_Plus 2 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pomodoro_homes_landing.md

<!-- sase:links:end -->

## Description

Close the gaps the bob-cli-9k landing review found between the shipped Pomodoro homes feature and its approved plan (plan:202610/pomodoro_homes.md). Rust and the bob-ledger-tools mirror agree on every shared vector. The review_time tile always equals the GTD review row. Stats theme parts are unchanged when no home filter applies. `bob ref today`, human `bob plan`, and the `=` override surfaces that landed during the epic label unnamed sessions by their derived homes. The Stats panel follows chart pins. Bob Mac Capture never routes by a derived label and draws forecast dots hollow.

## Notes

[2026-10-19T01:57:02Z · bob-cli-9k.8.land] LAND REVIEW / FOLLOW-UP TRIAGE: Read this epic, all four children and every note, both approved plans, parent bob-cli-9k and phases 9k.1-.7/notes. The sole current-child proposal is 9k.8.3 note 1 (live Obsidian LP/Reading and chart-pin validation): declined as a new task because it is an explicit acceptance requirement and remains epic work in the landing tale. 9k.8.4 note 1 macOS CI limitation: independently inspected run 39186590898 on 3a671761; Lint and Build green, Test has the existing RefsNewestTests.zone/NSObject.zone compile failure. Corroborated bob-cli-9m (+1), no new task; no causal active epic owns that pre-existing Newest failure. Mac SSH timed out. Parent proposals retain prior landing dispositions: scan_hooks fmt already fixed; six plugin failures tracked by 6v/6w/7i, timing flake by 3w, previous Mac test compilation by 9m, other placeholder surfaces by 9n. No new distinct out-of-scope follow-up was found. Both 9k.8 and 9k epic-symbols are empty.

[2026-10-19T01:57:06Z · bob-cli-9k.8.land] DISCOVERED ISSUE / REMAINING LANDING WORK: bob-plugins ed72a42 still calls metadataCache.getCache(file objects) at 142-pomodoro-home-chips.js:209/217; the existing noteFrontmatterFor helper in fragment 330 documents the same already-fixed API mistake elsewhere. Changing only the in-memory test double to require getCache(string) makes 12/18 homes tests fail (project labels become unfiled). Reading view includes its own inserted chip in ownText: after rendering the existing BLOG/sase test, pomodoroHomeReadingEntry(...).entry.name is BLOGsase, not BLOG. JS parent unwrapping also follows single-element list parent ["[[dev]]"] to dev.md whereas the Rust scalar-wikilink contract stops at @unfiled; plain parent dev is similarly accepted by JS. Mac 3a67176 still initializes restart pomodoroName from summary.pomodoroName ?? next session, so unnamed restart title/status/notification miss previous.homes. CaptureCompleteOverrideRunning does not decode homes and pomodoroStartPickerStatus omits it, leaving the empty-name override context integrated by concurrent 9j commits af3b4bb/9288244 without its derived label. 9k.8.4 explicitly hand-edited rather than regenerated fixtures; refs-today-homes.json still has impossible named-row homes and labeled empty parts. A medium tale will repair these, perform real Obsidian checks, and close this epic plus recheck parent 9k.

[2026-10-19T01:59:22Z · bob-cli-9k.8.land] LAND VERIFIED / INTEGRATION: Source and commit review confirms 77c7741 implements R5 remainder, closed-state attribution, review_row_time=yes, preserved unfiltered theme shares, used-key catalog, CLI alignment/caveat/hue and expanded vectors; c2c9f5c wires homes to ref today, human plan and Rust override previous/demoted/running. Live bob stats show worked review_time -f json -r 4w gives 1732m for both tile and GTD row. Mirrored vector bytes match; existing focused plugin homes/panel tests pass 33/33; npm run validate passes 7/7. bashunit tmux suite passes 6/6. Reviewed origin/master and non-epic drift since child creation: af3b4bb and Mac 9288244 empty-name override context needs Mac homes consumption; parent-era f4cdf0b intake changes require no homes integration. No other newer unrelated plugin/chezmoi changes. The validated medium tale sase_plan_pomodoro_homes_runtime_closeout.md plans only the confirmed remaining defects and validation, includes normal 9k.8 closeout and conditional fully rechecked parent 9k closeout, and never waits for its own commit/push/CI. No just check-full was run; final just check belongs after the repair edits.

[2026-10-19T02:52:21Z · bob-cli-9k.8.land--1] FINAL CHECKPOINT (2026-10-18). The monitored just check bjdsewr7tskk completed exit 0; just install completed. Live and pinned BOB_NOW=2026-10-18T12:00:00-04:00 bob stats show worked review_time -f json -r 4w both report review_time=1732m and 1732m summed @review:GTD project parts for Sep 20-Oct 17; the Oct 18 partial-day point is excluded from the reported total. Plugin build:check passes, the shared vector SHA-256 is identical in both repos (1b5293bfc9a1d935ca1aee74fa801f2b0bed1b8ac35f186a8d9276df3f9f4a97), edited fragments are 849 and 331 lines, npm run validate passes 7/7. npm test is 3110/3116; its only six failures exactly match clean-base artifact file:explicit:b50fabd7793647c91cc93653: Live Preview places one glyph after each unblocked link; widget mousedown places the cursor past the link; rebuild triggers skip the cursor but take doc, viewport, and refresh; Reading view glyphs unblocked rows and dedupes (bob-cli-6v); Keep counts once and saturates at 999 without reset (bob-cli-6w); forward conversion carries a Depends-On line and reverse restores it (bob-cli-7i). Explicit bob plugins sync --repo copied 2 files; its dry-run reports 0 to copy. Mac just portable-check passes 1389 tests after the regenerated wire fixture assertions were corrected and the named-row forward-compatibility model case kept synthetic. Mac-only typecheck-tests and macOS CI remain unverified; the prior XCTest compile issue is bob-cli-9m. Required live Obsidian acceptance remains blocked: artifacts file:explicit:0f1409dbf3236065be038cb1 and file:explicit:d590262a37f7c98de4bfc541 record isolated Obsidian 1.14.4 stuck on Loading for over 20 seconds with community plugins disabled and DevTools port 9226 timing out. The real profile and vault were not used for this acceptance. Keep this epic and parent open, and leave plan statuses unchanged. Follow-up dispositions remain: scan_hooks formatting fixed in 196af9b; plugin baseline tracked by 6v/6w/7i; stage-ranker timing flake by 3w; Mac XCTest compile issue by 9m; other pre-existing placeholders by 9n; no new tasks. Both epic-symbol checks are empty, just symvision is unavailable, and plan-links validation reports 64 legacy errors/0 warnings with no finding for either Pomodoro homes plan. No commits are ahead of the fetched origins.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9k.8.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.8.land.md) | [bob-cli-9k.8](bob-cli-9k.8.md) | 3 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`9217a47`](https://github.com/bobs-org/bob-cli/commit/9217a475779fe0a7368f8ac99428fbca0bfbc100) | fix(pomodoro-homes): add scalar-parent vectors | [bob-cli-9k.8](bob-cli-9k.8.md) | 2026-10-18 22:53:08 EDT |
| bob-mac-capture | [`bob-mac-capture@1df3411`](https://github.com/bobs-org/bob-mac-capture/commit/1df3411f46d965ff8f05de97daceba4927d0e652) | fix(capture): align homes fixtures and tests | [bob-cli-9k.8](bob-cli-9k.8.md) | 2026-10-18 22:54:07 EDT |
| bob-plugins | [`bob-plugins@5ef8cbe`](https://github.com/bobs-org/bob-plugins/commit/5ef8cbe4eb29c9a27a72623ec1ca5c7d9f639604) | fix(ledger-tools): correct homes runtime handling | [bob-cli-9k.8](bob-cli-9k.8.md) | 2026-10-18 22:54:52 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-9k.8.2][1] | need epic notes and prior phase state | 1 |
| read-by | [agent:bob-cli-9k.8.land--1][2] | Need the current child epic scope, descendants, and notes before recording final verification | 3 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-9k.8.2/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9k.8.land.md

<!-- sase:referenced-by:end -->
