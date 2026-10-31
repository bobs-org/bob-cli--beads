# Bead: bob-cli-ey.1.1.2 — % directive lexer with %c/%c\<N\>, and clipboard parsing split from reading

[Bead Pages](../README.md) / [bob-cli-ey.1.1](bob-cli-ey.1.1.md) / bob-cli-ey.1.1.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase · **↺ Reopened:** ↺1
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-ey.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.md) · **Assignee:** `bob-cli-ey.1.1.2` · **Size:** medium
**Created:** 2026-10-31 12:58:15 EDT · **Closed:** 2026-10-31 18:06:53 EDT
**Plan:** [202610/cli\_directives\_split.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/cli_directives_split.md)

## Previously Closed

> ↺ Closed 2026-10-31T20:42:44Z · done
>
> (none)
>
> Reopened 2026-10-31T21:00:46Z by `sase bead open`

## Description

directive-lexer-clip: add `capture_language/directive.rs` (edge position rule, transparency, bare `%` incomplete with need `directive`, `unknown_directive`, `\%` escape, duplicate refusal, `directive` span) recognizing `%c` and `%c<N>`; delete `%`/`%N`/`%header`, `parse_clip_token`, `ClipRequest` headers, `is_valid_header`, `ClipOutput.header`, and `CaptureParseOptions.parse_clip_markers`; make `-n/--no-clip` mean never-read (`clip.status: not_read`, `clip_not_read` refusal) and `-c/--clip` a plain flag; add a "Directives (`%`)" docs section. Commit as `feat(capture)!:`.

## Notes

[2026-10-31T20:42:44Z · bob-cli-ey.1.1.2] %c/%c<N> directive lexer; --clip flag; --no-clip never-read (clip.status not_read / clip_not_read). cargo fmt + clippy gates pass; 1242 capture lib tests; 15 CLI clip tests; just docs-gen + just docs-check; no leftover epic-symbols. just check via prepared monitor.

[2026-10-31T20:43:53Z · bob-cli-ey.1.1.2] PROPOSED FOLLOW-UP: Mac Capture live-preview docs still describe URL % listen and %N/%header clipboard; update bob-mac-capture capture-panel.md for URL @ listen and %c clip.status not_read under --no-clip

[2026-10-31T21:37:51Z · bob-cli-ey.1.1.2--2] Leftover template_clipboard test still used trailing %; switched to %c and matched the docs table. capture::parse_template CLI suite passes; just docs-check passed; no leftover epic-symbols.

[2026-10-31T22:06:53Z · bob-cli-ey.1.1.2--3] Verified %c/%c<N> directive lexer, plain --clip flag, and --no-clip never-read (clip.status not_read / clip_not_read). just check and just docs-check passed; no leftover epic-symbols.

## Dependencies

- **Depends on:** [bob-cli-ey.1.1.1](bob-cli-ey.1.1.1.md) ✓ · ⧖ 2026-10-31
- **Blocks:** [bob-cli-ey.1.1.3](bob-cli-ey.1.1.3.md) ◐ · ⧖ 2026-10-31

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ey.1.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-ey.1.1.2.md) | [bob-cli-ey.1.1.2](bob-cli-ey.1.1.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6ae5df0`](https://github.com/bobs-org/bob-cli/commit/6ae5df0033a4082b8a09a4406bbb16e70c436a05) | feat(capture)!: add %c/%c\<N\> directive lexer and split clipboard reading | [bob-cli-ey.1.1.2](bob-cli-ey.1.1.2.md) | 2026-10-31 18:23:34 EDT |
