# Bead: bob-cli-3n.10 — Migrate the vault to Depends-On lines

[Bead Pages](../README.md) / [bob-cli-3n](README.md) / bob-cli-3n.10

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.0vl](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vl.md) · **Assignee:** `bob-cli-3n.10` · **Size:** medium
**Created:** 2026-10-02 16:54:39 EDT · **Closed:** 2026-10-02 22:25:20 EDT
**Plan:** [202610/task\_dep\_links.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/task_dep_links.md)

## Description

vault-migrate: preflight the fleet (ask Bryan only if the Mac is unverified), add a tested dry-run-first migration script, rehearse on a vault copy with before/after hooks checks, run it live, prove idempotence, update the CSS comment, and sync.

## Notes

[2026-10-03T02:24:52Z · bob-cli-3n.10] Preflight: MacBook UNREACHABLE (ssh ConnectTimeout, matches 3n.9 after ~10min x8 retries). This host (athena) capability TRUE. Single-turn phase cannot wait on Bryan, so took the plan migrate-now path: Blocked is unaffected (fields carry ids; old hooks read fields), cost is only lost dependency promotion for migrated parents on the Mac until it updates. LEFT FOR BRYAN: bring Mac online, cargo install --locked --force from its bob-cli checkout, pull bob-plugins + bob plugins sync, verify hooks capability, reload plugins in each running Obsidian.

[2026-10-03T02:25:01Z · bob-cli-3n.10] Rehearsal on /tmp vault copy (excl .git): before legacy=14, projection/adopted/healed/canonicalized empty, warnings 0. After --write: 16 files, 33 lines, 34 folded, 0 field/target/adopted updates, 0 conflicts/unresolved/unadoptable/ambiguous. Hooks after: legacy 0, all arrays identical (zero Blocked flips, rank edges identical - no #^ref diffs at all). Second --write run: 0 files (idempotent). Live run identical counts. Changed files: bob_plugins, body, cash, job, sase_actstat, sase_agents_repo, sase_anti_gravity, sase_better_plans, sase_better_vars, sase_doctor, sase_dyn_agent_fam, sase_gate, sase_model, sase_model_panel, sase_parallel_fams, sase_toobig_symvision (16 notes; report expected ~18).

[2026-10-03T02:25:05Z · bob-cli-3n.10] Script: bob-plugins scripts/migrate-dependency-lines.mjs (parseArgs/planMigration/runMigration, nav helpers for grammar+link form+formatter) + scripts/test-dependency-line-migration.cjs (18 vectors) + npm test registration; committed 46ddd1e and pushed. Full plugin suite 1291/1291 green. Vault background sync auto-committed the 16 migrated notes (66c6d47c, 33+/34-) and the CSS comment (ea9cfc6a); tree verified clean, bob vault-sync run pushed, local==remote ea9cfc6a. Spot-check: body/cash excerpts show canonical first-child lines with fields mirroring; hooks post-run shows legacy 0, zero warnings/projection/adopted.

[2026-10-03T02:25:20Z · bob-cli-3n.10] Migrated: 16 notes, 33 Depends-On lines, 34 legacy children folded, 0 conflicts/unresolved/ambiguous. Verified: plugin suite 1291/1291 green incl 18 new migration vectors; rehearsal on vault copy showed zero Blocked flips, projection/adopted/healed/canonicalized empty, legacy 14->0, second run idempotent; live run identical; post-run hooks legacy 0 with zero warnings; vault-sync pushed local==remote. MacBook preflight unverified (ssh timeout) - migrate-now path taken, Blocked unaffected, Mac steps left for Bryan in bead notes.

## Dependencies

- **Blocks:** [bob-cli-3n.11](bob-cli-3n.11.md) ✓ · ⧖ 2026-10-02
- **Depends on:** [bob-cli-3n.9](bob-cli-3n.9.md) ✓ · ⧖ 2026-10-02

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-3n.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-3n.10/README.md) | [bob-cli-3n.10](bob-cli-3n.10.md) | 0 |
