# Bead: bob-cli-a0.5.1.5 — Bootstrap the public host and prove publication safety

[Bead Pages](../README.md) / [bob-cli-a0.5.1](bob-cli-a0.5.1.md) / bob-cli-a0.5.1.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.md) · **Assignee:** `bob-cli-a0.5.1.5` · **Size:** medium
**Created:** 2026-10-19 23:18:37 EDT · **Closed:** 2026-10-20 09:26:41 EDT
**Plan:** [202610/docs\_gated\_publication.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_gated_publication.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:95d246b4df6302904b85c55e | attached via sase artifact create --bead |

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

launch: add the three README docs links, configure the authorized public host and homepages, run first publish, broken-link drill, normal recovery and weekly checks, and record live URL and provenance evidence.

## Notes

[2026-10-20T05:26:43Z · bob-cli-a0.5.1.5--3] Verification: monitor p00gkv9h54xj ran `just docs-check` to exit 0 on 2026-10-20, including strict Zensical build, published URL checks, offline fragment checks, search smoke, tutorial, media determinism, and documentation tests. The first `just docs-publish` attempt (monitor gq2v1b4t1rve) failed before a workflow run was accepted: GitHub HTTP 422 rejected the reusable `docs-publish.yml` because its five jobs lacked `runs-on`. Added `runs-on: ubuntu-latest` to all five publish jobs and both weekly jobs; the exact updated source passes docs-check. Changes are pending SASE finalization before the first actual publish.

[2026-10-20T06:14:29Z · bob-cli-a0.5.1.5--7] Verification: monitor mqmy7m20drs4 ran `just check` to exit 0 on 2026-10-20 (ToolRun 61961ad48ebd3d7c22dc6aa0b3cdcf98). It validates the pending reusable workflow runner fixes and README links; source is still unlanded pending SASE finalization. The initial rejected publish created no accepted run.

[2026-10-20T08:00:29Z · bob-cli-a0.5.1.5--g] PROGRESS (2026-10-20): Current-source `just docs-check` passed (140 published routes, 378 URL mentions, 8 curated links; 419 passed, 1 skipped because font-generation dependencies were absent); `sase tool run -- just fmt` passed (4baae25ef757f40bdac22632ad8dee9b). Current bob-cli origin/master is 8ba29959d4aab047bff060c2bc082bbb92213803: it has the Node 24 setup and the three README site links, but the five docs-publish jobs and two docs-weekly jobs still lack runs-on. Worktree adds ubuntu-latest to all seven jobs, runner assertions to both workflow test files, and corrects `just` command examples; these source changes are not yet on master. Mac Capture origin/master is 3b944d877a7a0890b29c2d8d5d93d2c677d4b9d5; three matching README site links are pending in its worktree. Host bootstrap applied and pushed commit e9f447ab6a0059df0e8b2a928f4fef80db903782; repeat preview/apply was a no-op. `just docs-status`: workflows active, no published.json, no live /build.json, no accepted publish/weekly runs, no managed issues. Earlier publish dispatch gq2v1b4t1rve was rejected with HTTP 422 before acceptance for missing runners; do not count it as a run. NEXT: finalize the current bob-cli/Mac Capture edits through SASE with bead_action keep, verify both default branches, then inspect docs-status and dispatch first publish once; complete live URL/provenance checks, ordinary no-op, drill/no-deploy issue proof, ordinary recovery, weekly run, evidence, epic-symbols, and close only this phase.

[2026-10-20T11:26:37Z · bob-cli-a0.5.1.5] PROGRESS (2026-10-20): Source remainder for first publish is in this worktree and verified; it is not on origin/master yet.

Done now:
- Added `runs-on: ubuntu-latest` to all five docs-publish jobs and both docs-weekly jobs. YAML-aware tests require that on every reusable job and forbid it on both caller jobs (caller `uses:` jobs must not set runs-on).
- `bob-docs` host commands now parse `gh api` JSON when FORCE_COLOR is set: subprocess env disables color, and `gh_api` strips ANSI. Without that, host-bootstrap/status fail with `cannot parse ... metadata`.
- Mac Capture README now has the three site links (Get started / Reference / Develop) near the top. bob-cli and bob-plugins already had them. GitHub homepages for bob-cli, bob-plugins, bob-mac-capture, and the host are already https://bobs-org.github.io/.
- Host bootstrap --yes --deploy-dir (opened via sase repo) pushed 74205a8 to sync README just examples to `just … -- --flag`. Repeat preview: maintained files match, no commit, published.json still absent, Pages workflow, both callers active.
- `just docs-check` ToolRun 81c46a0710a8e1cceddd4bfa2e39245f succeeded (141 pages, 380 URL mentions, 8 curated links; 421 passed, 1 font-generation skip). Mac Capture `just docs-test` passed. No --epic-symbol leftovers.

Not first publish:
- Scheduled host run https://github.com/bobs-org/bobs-org.github.io/actions/runs/39405915133 (2026-10-20T10:09:26Z) failed as a workflow-file issue with zero jobs. Master still lacks runs-on. Earlier dispatch gq2v1b4t1rve was HTTP 422 before acceptance. Do not treat either as a publication.
- `just docs-status`: no published.json, no live /build.json, no weekly runs, no managed issues.

NEXT after this source lands on bob-cli origin/master AND bob-mac-capture origin/master:
1. Confirm `rg runs-on .github/workflows/docs-publish.yml docs-weekly.yml` on origin/master; do not dispatch until both reusable workflows on master declare ubuntu-latest.
2. `just docs-status`
3. First publish: `just docs-publish` under `/sase_monitor` (watch the dispatched run, not an unrelated scheduled failure). Record run URL/id, deployed SHAs, fingerprint, manifest commit, clean build.json flags; verify every /urls.txt page 200, curated fragments, footer SHAs, robots indexing.
4. Ordinary no-op (no deploy, no manifest commit).
5. Drill=`true`: live site/manifest unchanged, real link gate fails, one docs-publish blocked issue.
6. Ordinary recovery (no --force): gates run, deploy verifies, that issue closes.
7. Weekly dispatch once; record run URL and docs-weekly issue state.
8. Bootstrap preview remains a no-op; status matches live provenance.
9. `sase bead epic-symbols bob-cli-a0.5.1.5` then close only this phase.

[2026-10-20T11:48:56Z · 98] PROGRESS (2026-10-20): Existing runner/color fixes and all three repository README links have landed on source default branches. bob-cli base is 8ced873d7c2f6d1550168dcc17c4cfb7d116fa89. All four repository homepages are https://bobs-org.github.io/; host Pages uses workflow builds and both callers are active.

Found and fixed further launch defects in the current worktree:
- Verification and failure reporting referenced handoff/next-publication.json, but the uploaded handoff only contains published.json and urls.txt. Both now read the produced published.json.
- Handoff staging used a dot directory excluded by upload-artifact v4 defaults; it now uses publish-handoff. Confirmed against actions/upload-artifact v4 source and documentation through an audited external checkout.
- Documented just commands placed -- after the recipe, forwarding an invalid separator to bob-docs. Examples now put it before the recipe: just -- docs-publish --drill. Regression checks execute the handoff producer/consumer scripts and dry-run/parse all documented host commands. The new tests failed on the prior source and pass with these corrections.

Verification: just docs-check ToolRun 0f898214edb24c9d84035fd3e282ab61 succeeded (146 pages, 411 URL mentions, 8 curated links, 105 search cases, tutorial/media, 425 tests passed). Focused workflow/command checks passed again after the final handoff adjustment: 26 passed. git diff --check passed. No epic-symbol entries.

Host README correction was applied with authorized bootstrap; pushed host commit 4b3036187b852d46470aac0e2cbe53cd1da43b93. Repeat preview is a no-op and still preserves absent published.json. No successful publish exists yet. The six-file source fix must land before dispatch. Remaining acceptance is first publish/live provenance, unchanged no-op, drill preserving page/manifest hashes and opening one issue, ordinary recovery closing it, weekly success, and final status. Keep this phase and all ancestors open until those checks succeed.

[2026-10-20T12:03:41Z · 98--1] PROGRESS (2026-10-20): Following the answered launch-commit gate, committed and pushed the six-file handoff/command fix as 8783d49822ea546261cfbc8f0862878e5854c600 with sase_git_commit (exit 0). Checkout is clean and HEAD equals origin/master; default-branch publish/weekly runners and corrected handoff paths are confirmed. Prior full docs-check ToolRun 0f898214edb24c9d84035fd3e282ab61 is succeeded/exit 0; focused workflow tests passed again, 26 passed, and git diff --check passed. Host bootstrap preview remains a no-op at host commit 4b3036187b852d46470aac0e2cbe53cd1da43b93; both callers are active, no published.json or live build.json exists yet, and there are no managed issues. Next is the first actual publish under a SASE monitor, then live provenance/URLs, unchanged no-op, drill, ordinary recovery, weekly, final status, consolidated evidence on bob-cli-a0.5, and close only bob-cli-a0.5.1.5. User authorization explicitly covers additional verified intermediate commits; do not ask again. SASE separately reported deferred/quarantined prompt-archive publication from a pre-existing agents-sidecar rebase conflict; the source commit itself completed and pushed successfully.

[2026-10-20T12:16:15Z · 98--2] PROGRESS (2026-10-20): Inspected exact first dispatch https://github.com/bobs-org/bobs-org.github.io/actions/runs/39419509246 from monitor v4j52s9mgnzq. It failed before gates because publish-plan ran from GITHUB_WORKSPACE instead of the tooling checkout (no origin remote). The failure reporter also failed with HTTP 403 because gh targeted the tooling repo rather than the caller host; no site, manifest, or managed issue was created. Fixed planner cwd and set GH_REPO to github.repository in publication and weekly open/close reporting. Also request state in gh issue list and normalize uppercase values so closed managed issues reopen, and emit plan/gates stage before execution for accurate failures. Regression tests reproduced five failures on prior source and now pass; focused workflow/issue checks: 51 passed. Full docs-check ToolRun c4b2bf43cb79ca5754cdb30431a32110 succeeded: 146 pages, 411 URL mentions, 8 curated links, 105 search cases, tutorial/media, 430 tests passed. All five changed files committed/pushed with authorized sase_git_commit as 1b1758fdd907cbb824b7f8f54271668f689ca58d; clean HEAD equals origin/master. Existing prompt-archive sync/quarantine warnings did not prevent source commit success. Next: retry first publication under monitor, then live provenance/URL checks, unchanged no-op, drill preserving live hashes and manifest with one blocked issue, ordinary

… and 11480 more characters

## Dependencies

- **Depends on:** [bob-cli-a0.5.1.4](bob-cli-a0.5.1.4.md) ✓ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.5.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.5/README.md) | [bob-cli-a0.5.1.5](bob-cli-a0.5.1.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`110624b`](https://github.com/bobs-org/bob-cli/commit/110624b8df65bd81853b0a55660f9a3da233e9da) | fix(docs): run reusable publish jobs on ubuntu-latest | [bob-cli-a0.5.1.5](bob-cli-a0.5.1.5.md) | 2026-10-20 07:28:11 EDT |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:12a][1] | Host bootstrap phase status; diagnosing why site 404s | 1 |
| read-by | [agent:98--1][2] | Recover remaining live launch checks and closure requirements | 1 |
| read-by | [agent:98--2][2] | Resume failed first publication and verify remaining launch acceptance | 1 |
| read-by | [agent:98--3][2] | Recover launch evidence | 2 |
| read-by | [agent:98--4][2] | Inspect remaining launch scope and earlier verification | 1 |
| read-by | [agent:bob-cli-a0.5.1.5][3] | Need the phase scope and design file | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.12a/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.98.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.5/README.md

<!-- sase:referenced-by:end -->
