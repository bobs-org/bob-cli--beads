# Bead: bob-cli-9c.6 — Per-host drains, bridge retirement, docs, and rollout

[Bead Pages](../README.md) / [bob-cli-9c](README.md) / bob-cli-9c.6

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.research.4s.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.research.4s.linker.w0.md) · **Assignee:** `bob-cli-9c.6` · **Size:** medium
**Created:** 2026-10-18 14:40:04 EDT · **Closed:** 2026-10-18 16:57:15 EDT
**Plan:** [202610/ref\_ingest\_at\_birth.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_ingest_at_birth.md)

## Description

tailnet-rollout: in chezmoi, add the Linux bob-ref-intake systemd timer, retire the bob_xlib_pull bridge and pre_scan_hook, and fix the maybe_bob_highlights_sync gate. Rewrite the Highlights intake docs. Deploy to the hosts per the rollout decision, verify, and record the decision strand.

## Notes

[2026-10-18T20:56:53Z · bob-cli-9c.6--3] MAC HANDOFF: The one permitted SSH retry to mac timed out. When reachable, run on the Mac: mkdir -p ~/projects; if [ -d ~/projects/bob-cli/.git ]; then git -C ~/projects/bob-cli pull --ff-only; else git clone git@github.com:bobs-org/bob-cli.git ~/projects/bob-cli; fi; cargo install --path ~/projects/bob-cli --locked --force; chezmoi update -a --force; bob ref doctor. Do not edit the crontab during rollout; the exact existing schedule is in docs/vault-git-sync.md.

[2026-10-18T20:57:15Z · bob-cli-9c.6--3] Verified the chezmoi gate test (5/5), clean linked chezmoi checkout, and the new local intake timer on athena and apollo: enabled and active, with successful empty-queue service runs and dry runs on both. The authorized decision strand is present; docs/config no longer configure or invoke the bridge. The single Mac SSH retry timed out; exact local install/apply commands are recorded in the bead note and final handoff. Mac crontab was left untouched.

## Dependencies

- **Depends on:** [bob-cli-9c.1](bob-cli-9c.1.md) ✓ · ⧖ 2026-10-18
- **Depends on:** [bob-cli-9c.2](bob-cli-9c.2.md) ✓ · ⧖ 2026-10-18
- **Depends on:** [bob-cli-9c.3](bob-cli-9c.3.md) ✓ · ⧖ 2026-10-18
- **Depends on:** [bob-cli-9c.4](bob-cli-9c.4.md) ✓ · ⧖ 2026-10-18
- **Depends on:** [bob-cli-9c.5](bob-cli-9c.5.md) ✓ · ⧖ 2026-10-18

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-9c.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-9c.6.md) | [bob-cli-9c.6](bob-cli-9c.6.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| chezmoi | [`chezmoi@9ee5fd2`](https://github.com/bbugyi200/dotfiles/commit/9ee5fd2aa664f6986d0921b5bc15e3c3ae200253) | feat(chezmoi)!: retire cross-host highlights intake bridge | [bob-cli-9c.6](bob-cli-9c.6.md) | 2026-10-18 16:22:07 EDT |
| bob-cli | [`2a11d05`](https://github.com/bobs-org/bob-cli/commit/2a11d0514103a08ef5c29b4100196c5543e2028e) | feat(ref): roll out per-host intake drains | [bob-cli-9c.6](bob-cli-9c.6.md) | 2026-10-18 16:58:03 EDT |
