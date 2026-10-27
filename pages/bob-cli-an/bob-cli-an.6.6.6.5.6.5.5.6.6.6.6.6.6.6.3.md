# Bead: bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3 — Keep bob plugins sync from overwriting another agent's uncommitted deploy

[Bead Pages](../README.md) / [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.md) / bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.land.md) · **Assignee:** `bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3` · **Size:** large
**Created:** 2026-10-26 15:53:09 EDT · **Closed:** 2026-10-26 17:01:35 EDT
**Plan:** [202610/backlog\_batch15\_vault\_safety\_pdf\_moves\_and\_red\_gates.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch15_vault_safety_pdf_moves_and_red_gates.md)

## Description

plugin-deploy-guard: resolve bob-cli-cu by recording a deploy stamp for every synced plugin and guarding overwrites of a dirty or unpushed deploy from another checkout.

## Notes

[2026-10-26T21:01:35Z · bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3] Verified plugin-deploy-guard (deploy_guard=refuse). bob plugins sync now writes .bob-deploy.json beside each plugin (SHA-256 asset fingerprints + aggregate digest, source root/HEAD, tri-state dirty, host, time, complete/pending). Same-host fs2 lock keyed by canonical vault identity. Git vaults require the stamp ignored and untracked; --force does not bypass that, lock contention, or I/O. Force overrides deploy-provenance and dirty-vault protection only. Ancestry is local git merge-base --is-ancestor. Exact bundle equality includes optional CSS presence. Clean landing: dirty A then committed identical bytes from clean B reconciles the stamp without force. Backup run dirs are collision-safe.

Tests: 38 plugins lib tests + 24 plugins:: CLI tests; just check passed (fmt, clippy -D unused, full suite). just docs-check with BOB_DOCS_BOB_PLUGINS_DIR at the opened bob-plugins checkout: lint/generated/Zensical passed after dropping source_root path literals from docs/plugins.md JSON examples so privacy hits stay at baseline 6. bob-plugins npm test && npm run docs:check passed. Isolated live preview: linked bob-plugins already at origin/master (1621bd6); npm run build (all unchanged); rebuilt workspace bob plugins sync --repo <opened-checkout> --no-pull --dry-run: exit 0, 0 to copy / 22 unchanged, previews uncommitted stamp (docs-only dirty checkout), vault snapshot unchanged, no .bob-deploy.json written. No live vault deploy.

PROPOSED FOLLOW-UP: workspace just docs-check published-URL gate fails on unmodified-on-HEAD docs/guides/run-bob-from-obsidian.md:111 (https://bobs-org.github.io/bob-command-mode/ -> no built page for /bob-command-mode). Identical related-links block on master; bob-plugins docs:check against its cache clone of bob-cli passed (173 pages). Does not keep this phase open.

Limitations: existing binaries without stamps cannot enforce the guard; stamp-aware bob must be the sync caller. Non-Git sources require --force after the first deploy. Do not close bob-cli-cu or ancestor epics.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3.md) | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`115a361`](https://github.com/bobs-org/bob-cli/commit/115a3610bdb2caabf9763f49a487b29e2bc16efa) | feat(plugins)!: refuse overwriting another checkout's uncommitted deploy | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3.md) | 2026-10-26 17:02:42 EDT |
| bob-plugins | [`bob-plugins@0b02193`](https://github.com/bobs-org/bob-plugins/commit/0b0219310c4887bfcfaf1c84ffcb1a615de4d822) | docs(deploy): document plugin deploy stamps and overwrite refusal | [bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3](bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.6.3.md) | 2026-10-26 17:03:49 EDT |
