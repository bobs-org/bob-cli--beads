# Bead: bob-cli-ni.1 — Plugin scaffold, grammar module, and conformance vectors

[Bead Pages](../README.md) / [bob-cli-ni](README.md) / bob-cli-ni.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.research.5g.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.5g.linker.w0.md) · **Assignee:** `bob-cli-ni.1` · **Size:** medium
**Created:** 2026-11-19 10:05:33 EST · **Closed:** 2026-11-19 10:38:47 EST
**Plan:** [202611/copy\_chips.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/copy_chips.md)

## Description

grammar: create and register the bob-copy-chips plugin, then build the pure parser, scanner, and serializer every surface shares, pinned by JSON vectors and a round-trip property test.

## Notes

[2026-11-19T15:38:35Z · bob-cli-ni.1] COLLISION CENSUS: 1 live copy: chip in hidden .bob/ref-sources/chat/starts_after_relation--b7b0721aec41/source.md:499 (`copy: {title, why?, ...}`). Research-doc examples in .bob/ref-sources/chat/obsidian_copy_chips--b6905f2cb98e/source.md are extra-backtick quoted and do not parse as chips. No user-facing note would change meaning.

[2026-11-19T15:38:47Z · bob-cli-ni.1] Scaffolded bob-copy-chips 0.1.0 with frozen grammar (parse/scan/serialize/fence), JSON vectors, and 5000-iteration round-trip tests. Registered in chezmoi plugins.sync, vault .gitignore, and community-plugins.json; bob plugins sync --no-pull deployed it enabled. npm run build, validate, docs:gen, docs:check passed; grammar+roundtrip tests passed. Collision census: one hidden .bob/ref-sources hit, no user-facing collisions.

## Dependencies

- **Blocks:** [bob-cli-ni.2](bob-cli-ni.2.md) ◐ · ⧖ 2026-11-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-ni.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-ni.1/README.md) | [bob-cli-ni.1](bob-cli-ni.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@0b38f84`](https://github.com/bobs-org/bob-plugins/commit/0b38f84abee32d5c8b99de85de53b7fac4683ed7) | feat(bob-copy-chips): add plugin scaffold, grammar, and conformance vectors | [bob-cli-ni.1](bob-cli-ni.1.md) | 2026-11-19 11:02:38 EST |
