# Bead: bob-cli-da.2 — Keep language-mermaid through web-clip extraction

[Bead Pages](../README.md) / [bob-cli-da](README.md) / bob-cli-da.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.bob-cli-d7.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-d7.land.md) · **Assignee:** `bob-cli-da.2` · **Size:** medium
**Created:** 2026-10-27 16:30:19 EDT · **Closed:** 2026-10-27 17:04:20 EDT
**Plan:** [202610/backlog\_batch\_b2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/backlog_batch_b2.md)

## Description

mermaid-class: read bob-cli-d5, fix scripts/web_clip/web_clip_adapter.py so Defuddle extraction preserves language-mermaid (tag/restore via data attribute or post-process), extend --self-test to cover the real capture path, verify source.md/code.json record kind mermaid, and close bob-cli-d5 with evidence.

## Notes

[2026-10-27T21:04:20Z · bob-cli-da.2--2] Phase complete. Adapter stamps data-lang before Defuddle and restore_code_languages after; --self-test covers restore plus the real capture path. just check-web-clip-adapter passed (monitor kn9bs7pxcq60). Isolated bob ref create of article_basic.html (-H -k -N da2-mermaid-class-src) kept language-mermaid in render/source.html, wrote source.md with a mermaid fence, and cataloged code.json n=2 kind=mermaid. Closed bob-cli-d5 with that evidence. epic-symbols: none.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-da.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-da.2.md) | [bob-cli-da.2](bob-cli-da.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`6b0a30b`](https://github.com/bobs-org/bob-cli/commit/6b0a30bf7b6d18d568f8006088041848d046f976) | fix(web-ref): keep language-mermaid through Defuddle extraction | [bob-cli-da.2](bob-cli-da.2.md) | 2026-10-27 17:20:52 EDT |
