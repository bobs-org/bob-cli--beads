# Bead: bob-cli-a0.11.1 — Mac Capture reference, media, and documentation front door

[Bead Pages](../README.md) / [bob-cli-a0.11](bob-cli-a0.11.md) / bob-cli-a0.11.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.11](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.11.md) · **Assignee:** `bob-cli-a0.11.1.land`
**Created:** 2026-10-20 03:05:22 EDT · **Closed:** 2026-10-20 08:11:10 EDT
**Plan:** [202610/mac\_capture\_reference.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_reference.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/mac_capture_reference.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 3 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/mac_capture_reference.md

<!-- sase:links:end -->

## Description

Complete bob-cli-a0.11 with preserved Mac Capture reference, actionable recovery guides, CI-rendered images, a useful README, and verified shared-site mounts.

## Notes

[2026-10-20T11:43:12Z · bob-cli-a0.11.1.land] LAND AUDIT / FOLLOW-UP TRIAGE (2026-10-20): Read this epic (no own notes at first read), all four children and every child note, plan:202610/mac_capture_reference.md, parent phase bob-cli-a0.11 and plan:202610/bob_public_docs_site.md. Reviewed epic commits in bob-cli 1f3b90e5/8ba29959/d4b1ab31/8ced873d and Mac 1fff6aa/3b944d8/bd9b1e2/48c871a, source-owned pages, mounted hubs, guides, media importer/wrapper/tests, resolver/settings/stash/notification source. All phases are closed; their interim README links and remaining gate notes were addressed in subsequent phases. MIT/search indexing/published decisions remain selected; no memory edits or runtime behavior changes are needed. The source-hub deviation in phase 1 is consistent with the existing committed mount ownership tests. Baseline README 065908f has all 13 code fences preserved; 100 of 125 long paragraphs survive verbatim, with the remaining sections redistributed into install/settings/permissions/developer pages and five recovery guides.

Integration review: fetched bob-cli origin/master, no unreviewed newer commits at that point. Non-epic bob-cli 110624b8 adds publish runners and gh JSON color handling; no Mac mount conflict. Mac b0282a8 repairs cross-section row identity without changing the documented ranking contract. Concurrent Mac ddea5df adds a Docs block that duplicates the epic front door in 48c871a: README now has two Docs headings (lines 8,47) and repeated site lines. Consolidate these. Live read-only gh run/artifact queries parse successfully in the media helper both normally and with FORCE_COLOR=1 (NO_COLOR removed), so no speculative importer change. Fresh just docs-test passes all eight tests; final combined docs/build/check gates remain for the repair coder. No epic-symbol entries at this audit. Neither repository has a symvision recipe currently.

PROPOSED FOLLOW-UP outcome: bob-cli-a0.11.1.4 note #2 (RefsRanking.swift and RefsKeyRouter.swift still cite removed README tables) is accepted as this epic's migration work, not deferred. Confirmed three stale comments at RefsCore/RefsRanking.swift:6,38 and BobMacCapture/Refs/RefsKeyRouter.swift:40. /sase_new_task same-type and all-type searches plus the one-week task sweep found no duplicate; active-epic inspection identifies this epic as the cause. No separate task created, and no proposal is dropped. The remaining-work tale must repair only those comments, preserve executable Swift and README Signing, and follow the Mac compile requirements.

Additional bounded documentation completion: remove the public develop/mac-capture/index.md sentence about what is allowed in this epic; correct fix-mac-capture-bob-resolution.md's claim that unsigned bob causes Not resolved (BobExecutableResolver checks absolute override and executable permission, not signature); qualify recover-mac-capture.md and the matching reference summary for Control-C with stash capacity 0 and task-Go-To cancellation (stashDraftAndClose always discards, CanceledDraftStash.push returns nil at zero); reconcile permissions.md's never-in-notification-bodies claim with settings.md and NotificationService.singleCaptureBody/semanticText, preserving draft/log redaction while acknowledging semantic capture text and scan reference titles in notifications. These are accuracy/consistency of the migrated documentation, not new app work. No distinct unrelated follow-up found. Leave this epic and parent phase open for a medium tale that finishes these repairs, required verification, epic close/plan status done, and normal parent-phase bob-cli-a0.11 close; leave containing bob-cli-a0 to its waiting lander.

[2026-10-20T12:11:10Z · bob-cli-a0.11.1.land] Land repairs verified in working tree (host commits after turn). Prior audit stands: 4 phases closed, 13 fenced examples preserved, 100/125 baseline paragraphs verbatim with rest redistributed, MIT/search/published-decisions kept, source ownership kept. Concurrent integration: Mac ddea5df duplicate Docs block consolidated into one front-door Docs section (exactly one ## Docs, ## Signing intact, install/MIT preserved); b0282a8 row-identity compatible; bob-cli 110624b8 no mount conflict. Repairs: 3 stale Swift comments retargeted (RefsRanking x2 -> docs/refs.md Sorting, RefsKeyRouter -> docs/keyboard.md), comment-only, BundleSigningInspector intact; develop/mac-capture/index.md epic sentence replaced with durable ownership guidance; fix-mac-capture-bob-resolution If-it-goes-wrong now states absolute/executable/four-paths causes with no signature inspection and separate signing link; recover-mac-capture distinguishes Escape-retain vs Control-C stashDraftAndClose (capacity-0 nil, Task-Go-To discard) with Settings link, Delete All rules preserved; capture-panel Submit/Stash and keyboard Control-C aligned (Go-To + capacity-0 exceptions); permissions Privacy now states raw-draft redaction vs semantic success-notification text with notification-copy link, other guarantees preserved. Comment-proposal disposition: phase 1.4 note 2 accepted as epic migration work, no duplicate found, no standalone task created. Gates: bob-cli just check exit 0; just docs-check with Mac source override exit 0 (421 passed 1 skipped); Mac BOB_CLI_DIR wrapper exit 0; just docs-build-material exit 0; rendered fix/recover/permissions pages inspected in built HTML; athena portable-check 1445 tests 0 failures; mac scratch copy Scripts/bundle.sh exit 0 and just typecheck-tests exit 0, scratch deleted. No drift (no HEAD..origin/master commits in either repo). epic-symbols none; no symvision recipe in either repo. No verification limitation.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.11.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.11.1.land.md) | [bob-cli-a0.11.1](bob-cli-a0.11.1.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`3f0b4a8`](https://github.com/bobs-org/bob-cli/commit/3f0b4a879cb1688f049a757c2c8b446bf51bc8ad) | docs(mac-capture): correct recovery claims and durable develop-hub guidance | [bob-cli-a0.11.1](bob-cli-a0.11.1.md) | 2026-10-20 08:13:10 EDT |
| bob-mac-capture | [`bob-mac-capture@532c376`](https://github.com/bobs-org/bob-mac-capture/commit/532c376c7e1844909315732f68b96d68cf72207d) | docs(mac-capture): consolidate README front door, repair stale refs, correct retention and privacy | [bob-cli-a0.11.1](bob-cli-a0.11.1.md) | 2026-10-20 08:14:23 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.11.1.1][1] | Need epic DECISIONS | 1 |
| read-by | [agent:bob-cli-a0.11.1.2][2] | Need epic DECISIONS that this phase must honor | 1 |
| read-by | [agent:bob-cli-a0.11.1.4][3] | Need prior phase notes, DECISIONS, and README-section mappings | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.11.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.11.1.2/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.11.1.4/README.md

<!-- sase:referenced-by:end -->
