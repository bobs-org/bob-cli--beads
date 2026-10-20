# Bead: bob-cli-a0.6.1 — Complete the Bob Learn path

[Bead Pages](../README.md) / [bob-cli-a0.6](bob-cli-a0.6.md) / bob-cli-a0.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.6.md) · **Assignee:** `bob-cli-a0.6.1.land`
**Created:** 2026-10-19 23:17:16 EDT · **Closed:** 2026-10-20 01:41:50 EDT
**Plan:** [202610/learn\_path.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/learn_path.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202610/learn_path.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202610/learn_path.md

<!-- sase:links:end -->

## Description

New readers can follow a verified first Bob day in a synthetic vault, understand component requirements, and continue into Obsidian or Mac Capture; executable tutorial checks and deterministic CLI media keep the published path accurate.

## Notes

[2026-10-20T05:19:19Z · bob-cli-a0.6.1.land] FOLLOW-UP TRIAGE COMPLETE before repair tale proposal: (1) bob-cli-a0.6.1.2 note #1 is merged with bob-cli-a0.6.1.3 note #1 into one clean-machine CLI/Obsidian/Mac walkthrough; independent task declined because plan:202610/bob_public_docs_site.md already explicitly assigns this manual deliverable to bob-cli-a0.13 handoff. Recorded on active parent bob-cli-a0 via /sase_new_task. (2) bob-cli-a0.6.1.3 note #2 is shared-theme accessibility work corroborated by earlier bob-cli-a0.3 note #2; recorded as DISCOVERED ISSUE on active causal epic bob-cli-a0 for its final sweep, not a new task. No tasks matched all-status search or the one-week all-type sweep. No proposal was silently dropped. Known Learn instruction/runtime defects are retained as remaining epic work in the repair tale, not deferred follow-ups.

[2026-10-20T05:22:03Z · bob-cli-a0.6.1.land] LAND AUDIT before repair tale: Read the epic, every child and all child notes, plan:202610/learn_path.md, enclosing phase bob-cli-a0.6 and its final DECISIONS, parent plan:202610/bob_public_docs_site.md, actual sandbox/tutorial/media/check source and tests, reader pages/templates/fixture, and epic commits 7751f505, 48f3ef22, 50d0e990. Reviewed non-epic changes since creation (including pre-first-epic-commit changes): publication planning/workflows/host/weekly gates, product references, and plugin mount b1f98d99. HEAD and remote master both 50d0e990138287513304fbde2487cf54defbb86c. Product-reference continuation links from cf7a9e98 and mount-aware docs-check integration are already retained; Learn must now link the plugin mount. Final license/indexing/public-decisions/no-unneeded-memory-edit choices remain honored. Focused tests: uv run --project tools/docs pytest tools/docs/tests/test_tutorial.py tools/docs/tests/test_media.py tools/docs/tests/test_compatibility.py tools/docs/tests/test_check.py -m 'not integration' -q => 29 passed, 3 deselected in 3.69s. Not a new full docs or GUI pass. Reproduced two untested defects: a selected executable named versioned-bob leaves literal bob resolving to an ambient decoy; a PTY child closing descriptors 0/1/2 and sleeping 1s returns 0 after 1.03s despite timeout=0.1. Also rendered the compatibility partial with an absolute synthetic private checkout path and confirmed it is exposed. Source review found the thin-client claim incorrectly expanded to Obsidian plugin writes; custom plugins incorrectly described as Community installs and sync omits explicit clone/repo path; Mac continuation lacks launch/link details and reuses the tutorial's existing seedlings ID. These are remaining epic work, not follow-ups. Prepared medium tale sase_plan_learn_landing_repairs.md covering only repairs/integration and complete closeout of bob-cli-a0.6.1 then phase bob-cli-a0.6 in the coder turn. First validation diagnosed missing title/goal; fixed and revalidation passed with 0 warnings. Follow-up triage is fully recorded in the preceding note and on bob-cli-a0. Both bob-cli-a0.6.1 and bob-cli-a0.6 have no epic-symbol entries; current justfile has no symvision recipe. Do not close yet: proposing the repair tale as required, with actual docs-check, both builders/visual checks, just check, symbol recheck, original-plan status done, and normal parent-phase close as its final steps. No check-full run, no forced close, no product source changes in this audit.

[2026-10-20T05:41:50Z · bob-cli-a0.6.1.land] Learn landing repairs complete. Scope: (1) sandbox PATH authority via sandbox-owned bin/bob shim (resolves distinct basenames and resolved-symlink parents; checkpoints/media stay on selected executable; invalid BOB_BIN, Cargo target-dir, single preparation, cleanup preserved); (2) PTY EOF bound by remaining deadline with group terminate/reap, descriptor close, actionable DocsError (Linux EIO/macOS EOF, ANSI, nonzero status preserved); (3) reader repairs: Obsidian Tasks-only from Community plus clone/sync with explicit --repo/--bob-dir, inbox routing before Alt+F stamp, Ctrl+Alt+J review gesture with mounted plugin/ledger links; Mac Capture build/bundle/install/launch with Executable override/Vault path labels, README Requirements/Development/Signing links, fresh ^shears draft validated post-tutorial; concepts thin-client limited to Mac Capture with success-response diagram and direct plugin-write prose; first-day Bash prerequisite, fixed-clock zero-minute note, desktop continuations first while retaining cf7a9e98 reference links; compatibility floors with mounted plugin link and Mac README links, headless-vs-desktop Tasks distinction kept. Verification: focused pytest 24 passed + new sandbox/PTY/compat regressions; integration 3 passed (both tutorial dates, media); just docs-check passed (tutorial replay, media determinism, 409 unit passed); just docs-build-material and just docs-build (Zensical) strict passed with diagram/snapshot/continuation links in built HTML; just check passed; epic-symbols clean for bob-cli-a0.6.1 and bob-cli-a0.6; no demo/media drift; HEAD still 50d0e990. Triage (from land audit, not reopened): clean-machine Obsidian/Mac walkthrough is bob-cli-a0.13 handoff, recorded as DISCOVERED ISSUE on bob-cli-a0; theme-wide axe/zoom findings are bob-cli-a0.3-predating shared work, recorded as DISCOVERED ISSUE on causal epic bob-cli-a0 for its final sweep; no duplicate tasks.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.6.1.land.md) | [bob-cli-a0.6.1](bob-cli-a0.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`928c195`](https://github.com/bobs-org/bob-cli/commit/928c1955e1f3f63a579cddd25162298e60e25c6b) | feat(docs): repair Learn sandbox, PTY, reader, and compatibility gaps | [bob-cli-a0.6.1](bob-cli-a0.6.1.md) | 2026-10-20 01:44:17 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.6.1.3][1] | Need parent epic DECISIONS | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.6.1.3/README.md

<!-- sase:referenced-by:end -->
