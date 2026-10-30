# Bead: bob-cli-eg.1 — Fix client reuse and make the OAuth client step robust

[Bead Pages](../README.md) / [bob-cli-eg](README.md) / bob-cli-eg.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.165](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.165.md) · **Assignee:** `bob-cli-eg.1` · **Size:** medium
**Created:** 2026-10-30 09:42:40 EDT · **Closed:** 2026-10-30 10:11:58 EDT
**Plan:** [202610/gcal\_login\_redesign.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gcal_login_redesign.md)

## Description

client: normalize gog's stored client JSON and pipe it to `gog auth credentials set -`, skip keyring-held clients, validate `-c` files, let `-c` replace a stored client, and make fake gog reject what real gog rejects.

## Notes

[2026-10-30T14:11:49Z · bob-cli-eg.1] PROPOSED FOLLOW-UP: Pre-existing lib failure table_layout_records_prose_tables_on_snapshot_route fails identically on clean base — needs triage

[2026-10-30T14:11:58Z · bob-cli-eg.1] Implemented client phase: normalized client JSON via credentials set stdin, keyring skip, -c validation/replace, fake gog parity. Verified: gcal_auth 28 passed, gcal_cli/lifecycle/list/sync passed, lib gcal/client tests passed, fmt+clippy clean. Full just check has one pre-existing failure (table_layout_records_prose_tables_on_snapshot_route) that reproduces on clean base.

## Dependencies

- **Blocks:** [bob-cli-eg.2](bob-cli-eg.2.md) ◐ · ⧖ 2026-10-30

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-eg.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-eg.1/README.md) | [bob-cli-eg.1](bob-cli-eg.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`2ca76ca`](https://github.com/bobs-org/bob-cli/commit/2ca76ca05a1bc544f16a3686774ac4a6538a9550) | fix(gcal): reuse gog clients by piping normalized client JSON | [bob-cli-eg.1](bob-cli-eg.1.md) | 2026-10-30 10:13:17 EDT |
