# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3 — Stop the research-file hook from creating hash-suffixed duplicate references

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3` · **Size:** large
**Created:** 2026-10-27 06:23:58 EDT · **Closed:** 2026-10-27 06:59:46 EDT
**Plan:** [202610/backlog\_batch17\_macos\_gate\_source\_backfill\_hook\_dedupe\_dirty\_scans\_swift\_format.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch17_macos_gate_source_backfill_hook_dedupe_dirty_scans_swift_format.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:19e2c6c00fdc72a47b88c967 | attached via sase artifact create --bead |

_Plus 1 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

research-hook-dedupe: resolve bob-cli-cm per the hook_dedupe decision by deriving stems without the artifact hash, choosing -f overwrite or -f reread, and proposing the fold of the five existing duplicates.

## Notes

[2026-10-27T10:59:37Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3] Implementation complete for bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3.

Baseline: bob-cli c2b69089, chezmoi 027a28b9. Both histories and dirty state checked before editing; no concurrent work disturbed.

Files changed (chezmoi only):
- home/bin/executable_bob_research_capture (new): stable-stem adapter, stdlib JSON + subprocess argv arrays, no hint parsing, no shell evaluation.
- home/dot_config/sase/sase.yml: hook command now `bob_research_capture`; `use: sase-research-artifacts@research-highlights` and provider filtering preserved.
- tests/bash/bob_research_capture_test.sh (new): 14 offline tests covering all six required behaviors.

Commit: chezmoi 10e9f1d2 `feat(sase): stable research-file hook with deliberate recapture modes` via /sase_git_commit (-B keep). Tree clean and in sync after commit.

Tests: focused suite 14/14 pass (83 assertions); full `just test-bash` 283/283 pass; chezmoi `just check` pass (fmt, lint, bash, pytest 26 passed); bob-cli `just check` pass (full suite, exit 0).

Deployment: `chezmoi diff` for the two targets showed only this change; applied only those targets with `chezmoi apply --force ~/bin/bob_research_capture ~/.config/sase/sase.yml` and verified installed helper/config identical to source. Post-commit hook ran the standard whole-home update. No live-report smoke capture performed.

Repair proposal: read-only, registered as artifact file:explicit:19e2c6c00fdc72a47b88c967 (label research-hook-stable-recapture-repairs) on this phase. Rechecked all five hash-suffixed rows (493 chat rows total): first two have same-title clean counterparts with saved-source pointers (PDF bytes differ, so no content equality inferred) -> archive proposals; two __gem singles have no counterpart -> hash-strip rename proposals (preview currently refuses `not in sync`, needs Mac scan); abandoned annotated fifth has 1 highlight/comment plus inbound link from sase_final_polish.md -> preserve, gated coordinated archive only, no rename command. No live repair executed; no generic archive command added.

Limitations: rename -d previews refuse `not in sync` until a Mac scan runs; gated writes require a Bryan-approved /sase_gate turn under the parent epic. PROPOSED FOLLOW-UP: none beyond the gated repairs already recorded in the proposal.

Leaves bob-cli-cm and all ancestors open for the parent lander.

[2026-10-27T10:59:46Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3] Implemented stable research-file hook (chezmoi 10e9f1d2): hash-free -N adapter with reread/overwrite policy plus 14 offline tests; full just test-bash (283) and just check gates pass in chezmoi and bob-cli just check passes. Deployed only the two hook targets and verified installed helper/config. Repair proposal registered as file:explicit:19e2c6c00fdc72a47b88c967; no live repair executed (gated writes need Bryan-approved /sase_gate). Leaves bob-cli-cm and ancestors open for the parent lander.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.3.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land][1] | Need the child scope and notes | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.6.6.land.md

<!-- sase:referenced-by:end -->
