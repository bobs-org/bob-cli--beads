# Bead: bob-cli-rb.5 — Enable the five leads in chezmoi and verify end to end

[Bead Pages](../README.md) / [bob-cli-rb](README.md) / bob-cli-rb.5

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1hh](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1hh.md) · **Assignee:** `bob-cli-rb.5` · **Size:** small
**Created:** 2026-11-27 15:03:21 EST · **Closed:** 2026-11-27 20:42:02 EST
**Plan:** [202611/capture\_type\_leads.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/capture_type_leads.md)

## Description

lead_rollout: add the `capture.type_leads` block to the chezmoi bob config, apply it, verify with a master-built bob, and write the approved memory records.

## Notes

[2026-11-28T01:42:02Z · bob-cli-rb.5] Enabled capture.type_leads in chezmoi bob config (BUILD/FIX/PLAN/READ/WRITE) and applied ~/.config/bob/config.yml. Master-built bob: types shows lead "Build"/"Fix"/"Plan"/"Read"/"Write" on those five rows with empty stderr (no type-lead warnings); capture-complete --cursor 2 -f json -- "#f" returns FIX lead {text:Fix, insert_at:5, insertion:"Fix ", cursor_after:9}; "#c" returns CHORE with no lead. Reviewer memory decisions were no, so no decisions/glossary records. BUILD/READ/WRITE are the predicted low-hit-rate canaries; a one-line config edit prunes or rewords them (e.g. WRITE: Draft).

## Dependencies

- **Depends on:** [bob-cli-rb.1](bob-cli-rb.1.md) ✓ · ⧖ 2026-11-27
- **Depends on:** [bob-cli-rb.4](bob-cli-rb.4.md) ✓ · ⧖ 2026-11-27

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-rb.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-rb.5.md) | [bob-cli-rb.5](bob-cli-rb.5.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@be8a467`](https://github.com/bbugyi200/dotfiles/commit/be8a467677057393a42bd39fa4bdabcf1f981201) | feat(bob): enable capture type leads for BUILD FIX PLAN READ WRITE | [bob-cli-rb.5](bob-cli-rb.5.md) | 2026-11-27 20:44:35 EST |
