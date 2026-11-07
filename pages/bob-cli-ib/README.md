# Bead: bob-cli-ib — Crontabs as code through chezmoi, with first-class agent access

[Bead Pages](../README.md) / bob-cli-ib

**Status:** ◐ in_progress · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.5w.linker.w1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.5w.linker.w1.md) · **Assignee:** `bob-cli-ib.land`
**Created:** 2026-11-07 12:43:37 EST
**Plan:** [202611/crontab\_as\_code.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/crontab_as_code.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/crontab_as_code.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 7 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/crontab_as_code.md

<!-- sase:links:end -->

## Description

One committed cron: block in the chezmoi repo is the single source of truth for every machine's user crontab; chezmoi update -a converges each machine's own marked block without touching other lines, and agents can read and write any machine's crontab from any machine through cronctl, a /crontab skill, and a global memory note.

## Notes

[2026-11-07T21:49:39Z · bob-cli-ib.land] LAND TRIAGE (bob-cli-ib land agent): outcomes for every PROPOSED FOLLOW-UP from the phase notes.
(1) chezmoi just test-nvim/test-hammerspoon busted.runner missing in non-interactive shells (ib.1 #1, ib.2 #2, ib.5 #1): filed as bob-cli-ie (bug, small). Reproduced at 6af21b40; not caused by the epic.
(2) poseidon_chezmoi_isolation_test 2 failures (ib.4 #2, ib.5 #2, ib.6 #5): filed as bob-cli-id (ci, small). chezmoi master CI has been red on every push since 9430387a (tailnet-h.1). The epic's cron suites pass in CI on the latest chezmoi.
(3) Delete cron.retire once status allows it (ib.6 #1): filed as bob-cli-if (small). It cannot happen yet: the post-commit 'cronctl apply mac' (monitor n7hy5x) failed with the expected macOS TCC 'Operation not permitted', so the Mac stays unmanaged with its 3 legacy lines until Bryan runs chezmoi update -a locally or grants Remote Login Full Disk Access.
(4) Upgrade athena chezmoi v2.13.1, then move data to .chezmoidata/cron.yaml (ib.6 #2): filed as bob-cli-ig (medium), linked as related to bob-cli-if.
(5) apollo duplicate ~/go/bin/chezmoi (ib.6 #3): filed as bob-cli-ih (xsmall). Verified: ~/bin v2.70.2 and ~/go/bin dev (Oct 18); asks Bryan before deleting.
(6) sase epic watchdog loses XDG_RUNTIME_DIR/DBUS after the env-line retirement (ib.6 #4): the code lives in the sase project and is causally tied to the live sase-1r2 watchdog, so it is recorded as a DISCOVERED ISSUE note on sase-1r2, not as a bob-cli task. The same-boot path still works.
INTEGRATION: closed bob-cli-30 (Mac crontab drift / ssh install) as superseded by this epic, with bob-cli-if tracking the Mac apply. Noted on bob-cli-5g that its Mac ref-jobs line must now be a cron: data job via /crontab. bob-cli docs/vault-git-sync.md: added the TCC/Full Disk Access caveat for 'cronctl apply mac', and pointed Nightly maintenance at the bob-nightly cron: job and cronctl logs.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ib.1](bob-cli-ib.1.md) | Cron data schema, partials, and per-machine rendering | ✓ closed | medium | 2026-11-07 | 1 | 1 |
| [bob-cli-ib.2](bob-cli-ib.2.md) | Machine-agnostic job runner | ✓ closed | small | 2026-11-07 | 1 | 1 |
| [bob-cli-ib.3](bob-cli-ib.3.md) | Local reconciler, hook, and offline cronctl commands | ✓ closed | medium | 2026-11-07 | 1 | 1 |
| [bob-cli-ib.4](bob-cli-ib.4.md) | Fleet commands for status, diff, apply, logs, run, and edit | ✓ closed | medium | 2026-11-07 | 1 | 1 |
| [bob-cli-ib.5](bob-cli-ib.5.md) | Crontab skill, memory note, README, and alias cleanup | ✓ closed | small | 2026-11-07 | 1 | 1 |
| [bob-cli-ib.6](bob-cli-ib.6.md) | Move athena and Mac jobs into the data and cut over | ✓ closed | medium | 2026-11-07 | 1 | 2 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ib: Crontabs as code through chezmoi, with first-class agent access [in_progress]"]
    n1["bob-cli-ib.1: Cron data schema, partials, and per-machine rendering [closed]"]
    n2["bob-cli-ib.2: Machine-agnostic job runner [closed]"]
    n3["bob-cli-ib.3: Local reconciler, hook, and offline cronctl commands [closed]"]
    n4["bob-cli-ib.4: Fleet commands for status, diff, apply, logs, run, and edit [closed]"]
    n5["bob-cli-ib.5: Crontab skill, memory note, README, and alias cleanup [closed]"]
    n6["bob-cli-ib.6: Move athena and Mac jobs into the data and cut over [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n0 --> n4
    n0 --> n5
    n0 --> n6
    n1 -.-> n3
    n2 -.-> n4
    n2 -.-> n6
    n3 -.-> n4
    n4 -.-> n5
    n4 -.-> n6
    n5 -.-> n6
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ib.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ib.1/README.md) | [bob-cli-ib.1](bob-cli-ib.1.md) | 1 |
| [bbugyi200.athena.bob-cli-ib.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ib.2/README.md) | [bob-cli-ib.2](bob-cli-ib.2.md) | 1 |
| [bbugyi200.athena.bob-cli-ib.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.3.md) | [bob-cli-ib.3](bob-cli-ib.3.md) | 1 |
| [bbugyi200.athena.bob-cli-ib.4](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.4.md) | [bob-cli-ib.4](bob-cli-ib.4.md) | 1 |
| [bbugyi200.athena.bob-cli-ib.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.5.md) | [bob-cli-ib.5](bob-cli-ib.5.md) | 1 |
| [bbugyi200.athena.bob-cli-ib.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ib.6.md) | [bob-cli-ib.6](bob-cli-ib.6.md) | 2 |
| [bbugyi200.athena.bob-cli-ib.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ib.land/README.md) | [bob-cli-ib](README.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@d15ace3`](https://github.com/bbugyi200/dotfiles/commit/d15ace344c84b4d9c9bb8ab39a85305caf75f446) | feat(cron): add cron: data schema, validating partials, and per-machine crontab targets | [bob-cli-ib.1](bob-cli-ib.1.md) | 2026-11-07 13:04:28 EST |
| chezmoi | [`chezmoi@a2c680b`](https://github.com/bbugyi200/dotfiles/commit/a2c680bce7eb4b912d8d58453fee858672df0310) | feat(cron): add cronrun, the machine-agnostic cron job runner | [bob-cli-ib.2](bob-cli-ib.2.md) | 2026-11-07 13:07:25 EST |
| chezmoi | [`chezmoi@0b8e738`](https://github.com/bbugyi200/dotfiles/commit/0b8e73884bdf1cc28d753e37fb74c3d04b26d389) | feat(cron): add cronctl list/render/check/sync and the crontab sync hook | [bob-cli-ib.3](bob-cli-ib.3.md) | 2026-11-07 14:01:55 EST |
| chezmoi | [`chezmoi@102e823`](https://github.com/bbugyi200/dotfiles/commit/102e8238aa24840afa0783d5d497e1bbbde4f66e) | feat(cron): add cronctl fleet commands status, diff, apply, logs, run, and edit | [bob-cli-ib.4](bob-cli-ib.4.md) | 2026-11-07 15:07:46 EST |
| chezmoi | [`chezmoi@16701bf`](https://github.com/bbugyi200/dotfiles/commit/16701bfa8745723d040a8b8f701c9631b8adea86) | feat(cron): add the /crontab skill, crontab memory note, and Crontabs README section | [bob-cli-ib.5](bob-cli-ib.5.md) | 2026-11-07 15:31:57 EST |
| bob-cli | [`591bde8`](https://github.com/bobs-org/bob-cli/commit/591bde8dc82b4aacc08ad511602434b57d29cb0b) | docs(cron): point Mac scheduled maintenance at the chezmoi cron: data | [bob-cli-ib.6](bob-cli-ib.6.md) | 2026-11-07 15:55:07 EST |
| chezmoi | [`chezmoi@6af21b4`](https://github.com/bbugyi200/dotfiles/commit/6af21b405fa1b0888f169c0908ef9c0340baf4a0) | feat(cron): migrate athena and Mac jobs into cron: data | [bob-cli-ib.6](bob-cli-ib.6.md) | 2026-11-07 15:55:32 EST |
| bob-cli | [`b73ac38`](https://github.com/bobs-org/bob-cli/commit/b73ac383c239a1f058742050f84b70c94e6c5732) | docs(cron): note the Mac SSH install caveat and the bob-nightly cron job | [bob-cli-ib](README.md) | 2026-11-07 16:53:26 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-ib.1][1] | Need epic context and notes | 1 |
| read-by | [agent:research.3m.cdx][2] | Understand the in-progress declarative crontab epic before recommending Gmail scheduling | 1 |
| read-by | [agent:research.3m.cld][3] | Understand the in-progress crontab-as-code epic so the gmail sync research can recommend a cron entry | 1 |
| read-by | [agent:research.3m.final][4] | Verify crontab epic status and deferred reply-detection bead for gmail sync consolidated research | 1 |
| read-by | [agent:research.3m.gem][5] | Review context on crontab config and gmail sync | 1 |
| read-by | [agent:research.3m.grk][6] | Need the in-progress crontab-as-code epic for where to schedule gmail sync | 1 |
| read-by | [agent:research.3m.mus][7] | research gmail sync crontab context | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ib.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.3m.cdx/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.3m.cld/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.3m.final/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.3m.gem/README.md
[6]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.3m.grk/README.md
[7]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.3m.mus/README.md

<!-- sase:referenced-by:end -->
