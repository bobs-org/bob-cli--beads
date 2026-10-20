# Bead: bob-cli-a7.1 — Bare names on whole-item and chained starts

[Bead Pages](../README.md) / [bob-cli-a7](README.md) / bob-cli-a7.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** `bbugyi200.apollo.9p` · **Assignee:** `bob-cli-a7.1` · **Size:** medium
**Created:** 2026-10-20 15:12:11 EDT · **Closed:** 2026-10-20 16:08:10 EDT
**Plan:** [202610/bare\_pomodoro\_names.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bare_pomodoro_names.md)

## Description

standalone: lex `=name` as the `=#name` named start (shared bare-name predicate, execution, editor spans, completion, spelling-aware diagnostics, terminal hints) with equivalence tests against the `#` spelling.

## Notes

[2026-10-20T20:08:10Z · bob-cli-a7.1] lexes =name as the =#name named start; Close remains retired_whole_item_close_rewrite; glued-timing only when the glued rest is a selector component (=3x/=3bugs/=2fa teach =#x@3/=3#x); editor spans have no hash gap; completion bare_name prefixes # for non-bare slugs (=fa → #2fa); empty-raw did-you-mean uses named_start_token (=bugs); Later trail uses short spelling; twin-vault CLI =bugs≡=#bugs and x =sase≡x =#sase; just check green; no leftover --epic-symbol entries

## Dependencies

- **Blocks:** [bob-cli-a7.2](bob-cli-a7.2.md) ◐ · ⧖ 2026-10-20
- **Blocks:** [bob-cli-a7.3](bob-cli-a7.3.md) ◐ · ⧖ 2026-10-20

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-a7.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-a7.1/README.md) | [bob-cli-a7.1](bob-cli-a7.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`18c16f3`](https://github.com/bobs-org/bob-cli/commit/18c16f3dae2b64fdc2bbabdd71ee83c68da381af) | feat(capture): lex =name as the named pomodoro start | [bob-cli-a7.1](bob-cli-a7.1.md) | 2026-10-20 16:09:05 EDT |
