# Bead: bob-cli-a0.5.1.5 — Bootstrap the public host and prove publication safety

[Bead Pages](../README.md) / [bob-cli-a0.5.1](bob-cli-a0.5.1.md) / bob-cli-a0.5.1.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.md) · **Assignee:** `bob-cli-a0.5.1.5` · **Size:** medium
**Created:** 2026-10-19 23:18:37 EDT
**Plan:** [202610/docs\_gated\_publication.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_gated_publication.md)

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

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.12a/README.md

<!-- sase:referenced-by:end -->
