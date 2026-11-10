# Bead: bob-cli-jf.1 — Restore bob-mac-capture master and stop linked clones from mutating their host repo

[Bead Pages](../README.md) / [bob-cli-jf](README.md) / bob-cli-jf.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-jf](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-jf.md) · **Assignee:** `bob-cli-jf.1.land`
**Created:** 2026-11-10 06:47:59 EST · **Closed:** 2026-11-10 08:14:30 EST
**Plan:** [202611/bob\_mac\_capture\_history\_restore.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_mac_capture_history_restore.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bob_mac_capture_history_restore.md][1] | derived from the plan's `bead_id:` frontmatter field |

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bob_mac_capture_history_restore.md

<!-- sase:links:end -->

## Description

bobs-org/bob-mac-capture master again holds only Mac history (29147289 plus the genuine Mac commits pushed since), no checkout on athena, apollo, or the Mac still carries the bob-cli history that was pushed onto it, `just docs-check` passes again, and SASE can no longer rewrite or push a host checkout when a linked or sidecar path has no Git directory of its own.

## Notes

[2026-11-10T13:14:30Z · bob-cli-jf.1.land] LANDED. Verified both phases against live state, not only their notes. The approved restore_method=rewrite decision was honored.

RESTORE (bob-cli-jf.1.1): bobs-org/bob-mac-capture master is 0958974f (feat(capture): forward comma separator switch). Its first-parent chain is 28aa5b32 -> restored af604c6d -> 37933a14 -> a36f3e81 -> 6dddea35 -> GOOD 29147289, which matches the recorded four-commit mapping (b20ceca5->6dddea35, 3fb3a2be->a36f3e81, 5e29dd26->37933a14, 2c406dd5->af604c6d). From the opened linked checkout, I fetched every advertised head (master, ci/precommit/4c1e5994, mac-refs-hotkey-o, persist-canceled-draft-stash) and all 13 refs/pull/*/head. BAD 9a0bb25c is not in the object store afterward, so no ref contains it. There are no tags. The linked checkout's toplevel is itself, its origin is bob-mac-capture.git, and the host bob-cli_10 origin is bob-cli.git. The phase's 19-checkout survey (athena 12, apollo 6, mac 1) found no BAD refs or stashes. Green exact-SHA macOS CI: run 42816665790 at 28aa5b32. The original af604c6d run 42813392077 stays recorded as red; its highlight failure was fixed in the next commit and the other two failures are flakes (bob-cli-jb and the new bob-cli-jk).

GUARD (bob-cli-jf.1.2): sase commit a14bffcdbf ("fix(workspaces): guard Git mutations and pushes by checkout identity") is on sase origin/master. I read the diff. The new _git_worktree.is_worktree_root/require_worktree_root probe is bounded by GIT_CEILING_DIRECTORIES and compares realpaths. ensure_git_clone_at removes empty non-worktree targets and raises on nonempty ones, and its clone-failure fallback uses the probe. heal_clone_origin_if_needed, reconcile_managed_checkout_origin, set_origin_url/set_origin_push_url, _set_clone_origin, refresh_clean_linked_checkout, materialize_linked_repo_workspace (excludes and SDD), _materialize_remote_identified_sidecar, and the SDD/bare-sidecar origin setters are all guarded. The new push_guard.require_push_identity runs at the CommandRunner git push choke point and in bare_git_submit, checks origin and every push URL against the expected remote with remote_urls_match/git_remotes_match, and makes the retry loop stop on refusal. A 317-line real-Git test_checkout_identity_guard.py was added. The phase ran 117 focused tests and the full suite; its unrelated failures are triaged below.

INTEGRATION: bob-cli commits since the epic started (4219d70a, 7ff24c82, ffcb9864, 1f912b8c, plus f2882ea6 macos-ci-check workflow selection) don't touch linked-repo handling and don't duplicate the guard. macos-ci-check derives its push target from the checkout's own origin, so it needs no change. No source edits were needed. bob-cli has no references to BAD or GOOD.

DOCS-CHECK on clean bob-cli 1f912b8c: mount assembly and validation pass (the incident's mac-capture index collision is gone, and bob-cli-it did not reproduce). Lint still fails on pre-existing word budgets: mac-capture capture-panel 6014, capture-previews 6088, keyboard 6051, protocol 6149 (all bob-cli-h9), and json-outputs 6071 (active epic bob-cli-j8). The restore did not cause these.

FOLLOW-UP TRIAGE (5 PROPOSED FOLLOW-UP notes):
1. jf.1.1 #4 docs word budgets: duplicate. Added a +1 to bob-cli-h9 (now +7) with current counts, and a supplementary DISCOVERED ISSUE note on active epic bob-cli-j8 for json-outputs.md. No new task.
2. jf.1.1 #6 alias-tip timeout: created flake task bob-cli-jk (CaptureAliasTipPanelTests.testSecondEligibleSigilInASessionShowsNoTip), linked to jb, j9, and jf. No duplicate exists, and the epic that introduced the test (j9) is closed.
3. jf.1.2 #1 external-repo reuse validator: reproduced it (an empty nested dir reports is-inside-work-tree=true with toplevel=host). Created bug task bob-cli-jl (small) to move repo_open_external._is_valid_git_repo onto is_worktree_root, linked to bob-cli-jf. This is pre-existing and outside the epic's linked/sidecar scope; pushes from such a path are already refused by a14bffcdbf.
4. jf.1.2 #3 sase agent-state full-suite failures: created flake task bob-cli-jm. They pass on rerun and on the clean base, so the epic did not cause them.
5. jf.1.2 #4 sase publication-output test with long paths: created ci task bob-cli-jn (small). It fails identically on the clean base bd97664e07 because Rich wraps the path.

epic-symbols: none.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-jf.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-jf.1.land/README.md) | [bob-cli-jf.1](bob-cli-jf.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@1faead0`](https://github.com/bobs-org/bob-cli--plans/commit/1faead0bfb5224fb6dd7b7a2fafa7596f9a5c783) | chore(plans): mark bob-mac-capture history restore epic done | [bob-cli-jf.1](bob-cli-jf.1.md) | 2026-11-10 08:15:29 EST |
