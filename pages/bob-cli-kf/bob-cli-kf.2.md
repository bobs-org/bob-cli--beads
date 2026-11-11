# Bead: bob-cli-kf.2 — Web clip out-of-band fetch guard

[Bead Pages](../README.md) / [bob-cli-kf](README.md) / bob-cli-kf.2

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1bj](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1bj.md) · **Assignee:** `bob-cli-kf.2` · **Size:** medium
**Created:** 2026-11-11 13:33:44 EST · **Closed:** 2026-11-11 13:50:19 EST
**Plan:** [202611/security\_audit\_fixes.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/security_audit_fixes.md)

## Description

web-clip-fetch-guard: route image/PDF APIRequestContext fetches through the private-network guard with per-hop redirect checks, escape < in the reader CSS title, and fix the sanitize-order bug that disabled inline-SVG externalization.

## Notes

[2026-11-11T18:50:19Z · bob-cli-kf.2] Guarded APIRequestContext fetches refuse private image srcs and redirect-to-private PDF hops (no private fetch); css_escape_string blocks </style> breakout; sanitize-then-localize externalizes data-bob-svg; host verdict cache is per-capture. just check-web-clip-adapter passed.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-kf.2](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-kf.2/README.md) | [bob-cli-kf.2](bob-cli-kf.2.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0a7fce2`](https://github.com/bobs-org/bob-cli/commit/0a7fce2b399ae9865d6bc36670517f5d6893fbe3) | fix(web-clip): guard out-of-band fetches and CSS/SVG clip sinks | [bob-cli-kf.2](bob-cli-kf.2.md) | 2026-11-11 13:51:43 EST |
