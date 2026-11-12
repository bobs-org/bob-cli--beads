# Bead: bob-cli-kq.1 — Literal git pathspecs for vault filenames

[Bead Pages](../README.md) / [bob-cli-kq](README.md) / bob-cli-kq.1

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bo](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bo.md) · **Assignee:** `bob-cli-kq.1` · **Size:** small
**Created:** 2026-11-12 05:24:40 EST
**Plan:** [202611/security\_audit\_fixes\_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes_1.md)

## Description

git-literal-pathspecs: switch the highlights_ref recovery/mutation and collect_done git call sites that pass concrete vault filenames from ob::git_command to ob::git_command_literal, reject pathspec magic in recovery's validated_paths, and add glob-filename regression tests.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kq.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-kq.1.md) | [bob-cli-kq.1](bob-cli-kq.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`1920aab`](https://github.com/bobs-org/bob-cli/commit/1920aab661d37310fc58d57790b8a66026054d2c) | fix(git): use literal pathspecs for file mutations | [bob-cli-kq.1](bob-cli-kq.1.md) | 2026-11-12 06:11:12 EST |
