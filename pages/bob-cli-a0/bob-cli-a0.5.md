# Bead: bob-cli-a0.5 — Deploy repo, hourly gated publish, and launch

[Bead Pages](../README.md) / [bob-cli-a0](README.md) / bob-cli-a0.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.md) · **Assignee:** `bob-cli-a0.5` · **Size:** large
**Created:** 2026-10-19 18:55:42 EDT
**Plan:** [202610/bob\_public\_docs\_site.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_public_docs_site.md)

## Description

publish: add reusable publish/weekly workflows in bob-cli, bootstrap bobs-org/bobs-org.github.io, launch the site, and prove the fail-safe path with a drill.

## Notes

[2026-10-20T08:00:34Z · bob-cli-a0.5.1.5--g] PROGRESS (2026-10-20): Launch groundwork from bob-cli-a0.5.1.5: host bootstrap applied and pushed host commit e9f447ab6a0059df0e8b2a928f4fef80db903782; second preview/apply was idempotent. Host status is active but still unpublished (no manifest, live build, accepted publish/weekly runs, or managed issues). The first attempted publish was rejected pre-acceptance with HTTP 422 because reusable jobs lacked runs-on. On current bob-cli origin/master 8ba29959d4aab047bff060c2bc082bbb92213803, the Node setup and Bob README site links are present, while all seven publish/weekly jobs still need ubuntu-latest; the fix and regression assertions are pending SASE finalization. Mac Capture default branch is 3b944d877a7a0890b29c2d8d5d93d2c677d4b9d5 and its matching README links are pending. Current-source docs-check passed (419 passed, 1 font-dependency skip); formatting passed. Keep the launch phase open until the first publish, no-op, broken-link drill/recovery, weekly check, and complete provenance evidence are recorded.

[2026-10-20T11:26:53Z · bob-cli-a0.5.1.5] PROGRESS (2026-10-20) from launch phase bob-cli-a0.5.1.5: Host is bootstrapped (latest host commit 74205a8; Pages workflow; both callers active). Homepages already https://bobs-org.github.io/. README docs links: bob-cli and bob-plugins on master; Mac Capture links are in the launch worktree pending land. Reusable publish/weekly jobs still lack runs-on on bob-cli origin/master, so GitHub rejects publication (scheduled run 39405915133 failed as a workflow-file issue; earlier dispatch was HTTP 422). Launch worktree adds ubuntu-latest to all seven jobs, host JSON color stripping, and the Mac Capture README links; docs-check ToolRun 81c46a0710a8e1cceddd4bfa2e39245f passed. Keep .5 open until first publish, no-op, drill/recovery, weekly, and provenance evidence are recorded after those source changes land on master.

[2026-10-20T11:49:02Z · 98] PROGRESS (2026-10-20): Existing runner/color fixes and all three repository README links have landed on source default branches. bob-cli base is 8ced873d7c2f6d1550168dcc17c4cfb7d116fa89. All four repository homepages are https://bobs-org.github.io/; host Pages uses workflow builds and both callers are active.

Found and fixed further launch defects in the current worktree:
- Verification and failure reporting referenced handoff/next-publication.json, but the uploaded handoff only contains published.json and urls.txt. Both now read the produced published.json.
- Handoff staging used a dot directory excluded by upload-artifact v4 defaults; it now uses publish-handoff. Confirmed against actions/upload-artifact v4 source and documentation through an audited external checkout.
- Documented just commands placed -- after the recipe, forwarding an invalid separator to bob-docs. Examples now put it before the recipe: just -- docs-publish --drill. Regression checks execute the handoff producer/consumer scripts and dry-run/parse all documented host commands. The new tests failed on the prior source and pass with these corrections.

Verification: just docs-check ToolRun 0f898214edb24c9d84035fd3e282ab61 succeeded (146 pages, 411 URL mentions, 8 curated links, 105 search cases, tutorial/media, 425 tests passed). Focused workflow/command checks passed again after the final handoff adjustment: 26 passed. git diff --check passed. No epic-symbol entries.

Host README correction was applied with authorized bootstrap; pushed host commit 4b3036187b852d46470aac0e2cbe53cd1da43b93. Repeat preview is a no-op and still preserves absent published.json. No successful publish exists yet. The six-file source fix must land before dispatch. Remaining acceptance is first publish/live provenance, unchanged no-op, drill preserving page/manifest hashes and opening one issue, ordinary recovery closing it, weekly success, and final status. Keep this phase and all ancestors open until those checks succeed.

## Dependencies

- **Depends on:** [bob-cli-a0.1](bob-cli-a0.1.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.13](bob-cli-a0.13.md) ◐ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.2](bob-cli-a0.2.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.3](bob-cli-a0.3.md) ✓ · ⧖ 2026-10-19
- **Depends on:** [bob-cli-a0.4](bob-cli-a0.4.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.md) | [bob-cli-a0.5](bob-cli-a0.5.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:12a][1] | Deploy phase status: why bobs-org.github.io still 404s | 1 |
| read-by | [agent:bob-cli-a0.5.1.1][2] | Need binding decisions and prior phase notes for this implementation | 1 |
| read-by | [agent:bob-cli-a0.5.1.3][3] | Need the approved publication scope, DECISIONS, and current notes | 1 |
| read-by | [agent:bob-cli-a0.5.1.5][4] | Need the approved publication scope and current notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.12a/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.1/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.3/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.5/README.md

<!-- sase:referenced-by:end -->
