# Bead: bob-cli-h8.4 — Stop vault edits from leaking SASE plans into ~/bob

[Bead Pages](../README.md) / [bob-cli-h8](README.md) / bob-cli-h8.4

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.18c](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.18c.md) · **Assignee:** `bob-cli-h8.4` · **Size:** small
**Created:** 2026-11-04 16:39:09 EST · **Closed:** 2026-11-04 16:48:27 EST
**Plan:** [202611/top\_ten\_bead\_bundles.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/top_ten_bead_bundles.md)

## Description

vault-commit-guard: rewrite ~/bob/AGENTS.md so agents let bob vault-sync commit, or use plain git for their own files, and never use /sase_git_commit. Replace the stale Obsidian Sync sentence. Make the vault .gitignore keep sdd/ out. Close bob-cli-8n, and propose the SASE-side root cause of bob-cli-gy as a follow-up.

## Notes

[2026-11-04T21:48:13Z · bob-cli-h8.4] PROPOSED FOLLOW-UP: SASE must never archive a plan into a repo that is not that plan home -- root cause of bob-cli-gy. Likely trigger is the legacy gitignored ~/bob/sdd/beads store; vault side guarded via /sdd/ gitignore and AGENTS.md ban on /sase_git_commit; sdd/beads left in place

[2026-11-04T21:48:27Z · bob-cli-h8.4] AGENTS.md rewritten and committed by vault-sync as a5a8d6561, pushed, local==remote 43687b000, status clean; .gitignore ends with anchored /sdd/ at line 136, check-ignore shows it for sdd/plans and sdd/beads paths, ls-files sdd empty; shims and sdd/beads untouched; 8n closed; gy follow-up noted

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-h8.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-h8.4/README.md) | [bob-cli-h8.4](bob-cli-h8.4.md) | 0 |
