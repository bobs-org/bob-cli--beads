# Bead: bob-cli-iu.1 — bob capture-rewrite turns a spaced \`.\` into \`@\`

[Bead Pages](../README.md) / [bob-cli-iu](README.md) / bob-cli-iu.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.d0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.d0.md) · **Assignee:** `bob-cli-iu.1` · **Size:** small
**Created:** 2026-11-08 16:46:40 EST · **Closed:** 2026-11-08 17:35:56 EST
**Plan:** [202611/dot\_route\_alias.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/dot_route_alias.md)

## Description

bob-dot-route-alias: add the spaced `.` → `@` fallback to `expand_sigil_alias` behind Bob's route-completion gate, with unit and CLI tests, help text, and capture docs.

## Notes

[2026-11-08T22:35:56Z · bob-cli-iu.1] Spaced . now aliases @ via expand_dot_route_alias behind the route-completion gate (position: space/tab after body text with checkbox strip; token ends at cursor; no wikilink; Route field with empty replacement). Verified: 73 rewrite unit tests, full lib 5818 + cli 3301 suites, just docs-check, fmt, workspace clippy, and exact wire JSON for 'Buy milk .' (-c 10) with rule expand_sigil_alias, single @ edit, summary 'Typed @ for .'. capture-syntax.md needed meaning-preserving 20-word compression to stay under the 6000-word reference cap (was 3 words under at base).

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-iu.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-iu.1/README.md) | [bob-cli-iu.1](bob-cli-iu.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`0b8b913`](https://github.com/bobs-org/bob-cli/commit/0b8b913ff65e256ac8f4a4741841386aee9c800f) | feat(capture): alias spaced dot to @ where route completion opens | [bob-cli-iu.1](bob-cli-iu.1.md) | 2026-11-08 17:37:01 EST |
