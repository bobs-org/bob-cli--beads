# Bead: bob-cli-a0.5 — Deploy repo, hourly gated publish, and launch

[Bead Pages](../README.md) / [bob-cli-a0](README.md) / bob-cli-a0.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.95](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.95.md) · **Assignee:** `bob-cli-a0.5` · **Size:** large
**Created:** 2026-10-19 18:55:42 EDT · **Closed:** 2026-10-20 10:12:57 EDT
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

[2026-10-20T13:03:35Z · 98--4] PROGRESS (2026-10-20): Live launch safety is proven. First full publication https://github.com/bobs-org/bobs-org.github.io/actions/runs/39422837056 succeeded; manifest commit 5910ffb7ad58793f43989bd2ee7cc79ec69e5b2f, fingerprint 902aeea93583d0100052049ee1ccc04632034f7049b36fa9b5898a7b42817d7a. Sources: bob-cli d51c160e60d200c830b620257944897934a42f89; bob-mac-capture 532c376c7e1844909315732f68b96d68cf72207d; bob-plugins ff369873dab5b34c853b4201c6816ef1f362d6b8. All build.json dirty flags false; all 146 urls.txt pages 200, one curated fragment present, all footers match provenance, robots permits indexing. Ordinary no-op 39423369898 skipped gates/upload/deploy/record/live verify without host changes. Real broken-link drill 39423449416 failed its gate, skipped upload/deploy/record, preserved host manifest and all representative page/build/urls/robots hashes, and reopened exactly issue #1. Ordinary recovery 39423607269 used no force or pinned flag, rebuilt the identical fingerprint, passed all gates/deploy/record/live verification and closed issue #1; recovery manifest commit 38773b636b6d07990f8c539bd607aba3e93fdcbd. Full evidence snapshot: file:explicit:f38a1fb7e7c84707f4a75b2f.

Weekly run 39424193019 passed strict Material but failed online links at the Adobe license URL. Its separate failure reporter then failed GitHub label creation because the docs-weekly description exceeds 100 characters. Current worktree repairs that label, records the attempted weekly stage before execution, and supplies weekly-specific recovery instructions. Regression tests reproduced five failures on prior source; 62 focused tests now pass. Full docs-check is still running; verified fix must land before the one remaining weekly retry and bootstrap/status checks. Do not rerun any successful launch stages.

PROPOSED FOLLOW-UP: Weekly online link check rejects the upstream font license Adobe URL — http://www.adobe.com/ returns HTTP 403 at docs/assets/fonts/OFL.txt:2:30. Exact production command: bob-docs links --online in run https://github.com/bobs-org/bobs-org.github.io/actions/runs/39424193019; 30343 total, 1899 unique, 30300 OK, 1 Error, 42 Unsupported. Reproduced independently on isolated untouched base d51c160e60d200c830b620257944897934a42f89: lychee --no-progress --timeout 20 --max-retries 0 docs/assets/fonts/OFL.txt exits 2 with the same HTTP 403, 7 total/5 unique/6 OK/1 Error. Searches across all task statuses and recent task sweep found no semantic duplicate. Preserve the upstream license and strict failure signal; triage the remote refusal separately under the approved plan clean-base exception. Next command after the reporter fix lands: gh workflow run weekly.yml --repo bobs-org/bobs-org.github.io --ref main, then watch that exact run. If the sole Adobe failure remains, leave the separate docs-weekly issue open and record it at phase closure; do not report weekly links green. Ancestor closure remains with the land agents.

[2026-10-20T13:26:30Z · 98--5] LAUNCH ACCEPTANCE COMPLETE (2026-10-20): bob-cli-a0.5.1.5 is complete under the approved plan's independently reproduced clean-base failure exception. The public site is https://bobs-org.github.io/. No successful launch stage was redispatched during this final review.

Completed evidence:
- First full publication: https://github.com/bobs-org/bobs-org.github.io/actions/runs/39422837056. Host manifest commit 5910ffb7ad58793f43989bd2ee7cc79ec69e5b2f.
- Ordinary unchanged no-op: https://github.com/bobs-org/bobs-org.github.io/actions/runs/39423369898. Gates, upload, deployment, manifest recording and live verification were skipped; host remained unchanged.
- Real broken-link drill: https://github.com/bobs-org/bobs-org.github.io/actions/runs/39423449416. The production gate failed, upload/deploy/record were skipped, live hashes and host manifest stayed unchanged, and exactly the managed publication issue reopened.
- Normal recovery without force or pinned inputs: https://github.com/bobs-org/bobs-org.github.io/actions/runs/39423607269. Gates/deploy/record/live verification passed with the identical fingerprint, and https://github.com/bobs-org/bobs-org.github.io/issues/1 closed. Recovery manifest commit 38773b636b6d07990f8c539bd607aba3e93fdcbd; fingerprint 902aeea93583d0100052049ee1ccc04632034f7049b36fa9b5898a7b42817d7a.
- Live provenance: bob-cli d51c160e60d200c830b620257944897934a42f89; bob-mac-capture 532c376c7e1844909315732f68b96d68cf72207d; bob-plugins ff369873dab5b34c853b4201c6816ef1f362d6b8. All dirty flags false; all 146 urls.txt pages returned 200, curated fragment and footer SHAs matched, and robots permitted indexing.
- Latest source fix 2f9ad5bd9908f6b0e1cda1bf2d5fb14f252e8610 repairs weekly reporting. Full docs-check ToolRun cd957ae4bb572fed30dc2c711aa11977 passed all implemented gates and 435 tests; 62 focused tests passed.
- Final weekly retry: https://github.com/bobs-org/bobs-org.github.io/actions/runs/39427654125. Strict Material build passed; online links failed solely on the same Adobe HTTP 403; the repaired reporter succeeded. Exactly one docs-weekly issue is open with the correct weekly (links) stage and recovery instructions: https://github.com/bobs-org/bobs-org.github.io/issues/2. Publication issue #1 remains closed.
- Bootstrap preview matched templates, made no commit and preserved published.json byte-for-byte. Host did not change during weekly verification. Both hourly publication and weekly workflows are active; final status reports manifest/live ok and hold=false. Final live verification again checked all 146 pages.

Monitor ggs0weyx1sjj / ToolRun 40644fadbd21e77c0a8854a32d9bbbb4 exited 0; evidence completed_at=2026-10-20T13:20:58.942320+00:00 with no finish_error. Independently cross-checked completion, drill hash equality, recovery fingerprint equality, weekly host immutability, clean matching source provenance, active workflows and issue separation; confirmed the exact weekly run and current issue states through GitHub. sase bead e

… and 2491 more characters

## Dependencies

- **Depends on:** [bob-cli-a0.1](bob-cli-a0.1.md) ✓ · ⧖ 2026-10-19
- **Blocks:** [bob-cli-a0.13](bob-cli-a0.13.md) ✓ · ⧖ 2026-10-19
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
| read-by | [agent:98--4][2] | Read consolidated launch notes before recording external failure exception | 1 |
| read-by | [agent:bob-cli-a0.5.1.1][3] | Need binding decisions and prior phase notes for this implementation | 1 |
| read-by | [agent:bob-cli-a0.5.1.3][4] | Need the approved publication scope, DECISIONS, and current notes | 1 |
| read-by | [agent:bob-cli-a0.5.1.5][5] | Need the approved publication scope and current notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.12a/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.98.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.1/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.3/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.5/README.md

<!-- sase:referenced-by:end -->
