# Bead: bob-cli-k3.2 — Album recognition, the vault schema registry, and bob albums list and check

[Bead Pages](../README.md) / [bob-cli-k3](README.md) / bob-cli-k3.2

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.research.43.linker.w0` · **Assignee:** `bob-cli-k3.2` · **Size:** large
**Created:** 2026-11-11 04:56:43 EST
**Plan:** [202611/album\_and\_record\_notes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/album_and_record_notes.md)

## Description

album-model: recognize `type: "[[album]]"` and `type: "[[record]]"`, parse album frontmatter (top-level facts plus one nested `record:` schema) with key-path and line diagnostics, build the vault-aware record-kind registry with per-album isolation and the album-wins transition rule over config, and ship the read-only `bob albums list` and `check` with beautiful human output and JSON.

## Dependencies

- **Blocks:** [bob-cli-k3.4](bob-cli-k3.4.md) ◐ · ⧖ 2026-11-11
