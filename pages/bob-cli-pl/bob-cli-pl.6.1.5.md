# Bead: bob-cli-pl.6.1.5 — Verify settings behavior and visuals in real Obsidian

[Bead Pages](../README.md) / [bob-cli-pl.6.1](bob-cli-pl.6.1.md) / bob-cli-pl.6.1.5

**Status:** ◐ in_progress · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pl.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.md) · **Assignee:** `bob-cli-pl.6.1.5` · **Size:** medium
**Created:** 2026-11-24 15:49:21 EST
**Plan:** [202611/area\_project\_settings.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/area_project_settings.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| related | file:explicit:00ecd6d831fb1b470bfb515e | attached via sase artifact create --bead |
| related | file:explicit:06dc13b5afc95d4c0c5a784f | attached via sase artifact create --bead |
| related | file:explicit:0b7f5dcd3ad54a06615f0aa3 | attached via sase artifact create --bead |
| related | file:explicit:102101973af2ca32e6bb022d | attached via sase artifact create --bead |
| related | file:explicit:1517ae57c0a2221475089d20 | attached via sase artifact create --bead |
| related | file:explicit:15e6ee9644ddca04b3e15b68 | attached via sase artifact create --bead |
| related | file:explicit:1f140b8a9cfe8c2603d455bc | attached via sase artifact create --bead |
| related | file:explicit:2589494040f185f61a254804 | attached via sase artifact create --bead |
| related | file:explicit:25c2cf52c795b8bb980ef342 | attached via sase artifact create --bead |
| related | file:explicit:273b2c658d5b61c382a38a37 | attached via sase artifact create --bead |
| related | file:explicit:35090815a79efcf615498fa8 | attached via sase artifact create --bead |
| related | file:explicit:380437933d2ad00ffe9bf9e5 | attached via sase artifact create --bead |
| related | file:explicit:41087d9690fc6e75ad958db1 | attached via sase artifact create --bead |
| related | file:explicit:45956d095b4a9c87c12538d7 | attached via sase artifact create --bead |
| related | file:explicit:45dc7735989a011cdf728260 | attached via sase artifact create --bead |
| related | file:explicit:47b5de8060e4fa99bc07a717 | attached via sase artifact create --bead |
| related | file:explicit:4f7cfabb0cebd0eabd869db5 | attached via sase artifact create --bead |
| related | file:explicit:61aa57d5ad5f26328e620ffd | attached via sase artifact create --bead |
| related | file:explicit:63a4fe6ed44162080cb82577 | attached via sase artifact create --bead |
| related | file:explicit:69c4fda47ff362a7bffa75f8 | attached via sase artifact create --bead |
| related | file:explicit:69fff6f5a28d0761588ca8af | attached via sase artifact create --bead |
| related | file:explicit:6b3cd7189b58978001673256 | attached via sase artifact create --bead |
| related | file:explicit:768c90e756f020c43204ce1d | attached via sase artifact create --bead |
| related | file:explicit:7930a61423fb45f7864096c3 | attached via sase artifact create --bead |
| related | file:explicit:7c7732897efd57852e58549d | attached via sase artifact create --bead |
| related | file:explicit:7de1b3a5b07bde5695deaef7 | attached via sase artifact create --bead |
| related | file:explicit:84880df9b16f7a86054bcf04 | attached via sase artifact create --bead |
| related | file:explicit:8e08cc4bfd0c453564c2812f | attached via sase artifact create --bead |
| related | file:explicit:8f8cccda01e4ecab5e121689 | attached via sase artifact create --bead |
| related | file:explicit:a4c35a9f39b9398dbcf72f92 | attached via sase artifact create --bead |
| related | file:explicit:a7aad6122b88c9990f221c94 | attached via sase artifact create --bead |
| related | file:explicit:ae7eed0a50602d4baca2d591 | attached via sase artifact create --bead |
| related | file:explicit:b4a8eb54c2ec5fa6c470a21e | attached via sase artifact create --bead |
| related | file:explicit:c438fc384834aa3283bd6781 | Preserves the failed settings acceptance screenshot for the phase |
| related | file:explicit:c7d159491a8bb9e1baa7a352 | attached via sase artifact create --bead |
| related | file:explicit:c8e6f29f29359949ecbc2b5b | attached via sase artifact create --bead |
| related | file:explicit:ce1130b9190729572809a7b8 | attached via sase artifact create --bead |
| related | file:explicit:ce1569949e700d6cabaca6be | attached via sase artifact create --bead |
| related | file:explicit:ceac5914a62d6c380e0ccc51 | attached via sase artifact create --bead |
| related | file:explicit:d2709269d2d7eb52365f5f55 | attached via sase artifact create --bead |
| related | file:explicit:d80781d73db77817e7e20033 | attached via sase artifact create --bead |
| related | file:explicit:df648c0cb0cc5a2fd010f811 | attached via sase artifact create --bead |
| related | file:explicit:ed2035cf2c05f92752f0d83e | attached via sase artifact create --bead |
| related | file:explicit:f772ca3b26930c7f3fc9d2b7 | attached via sase artifact create --bead |
| related | file:explicit:fd4c679b570b513dca1338c5 | attached via sase artifact create --bead |
| related | file:explicit:ffc0445d5aad578111533de3 | failed settings acceptance filter dark screenshot ewgwedrv584s |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

settings-acceptance: extend the scratch-vault harness, exercise settings and generic parity with current bob, inspect screenshots, fix phase-specific regressions, and record deployment and verification evidence.

## Notes

[2026-11-25T12:12:55Z · bob-cli-pl.6.1.5] PROPOSED FOLLOW-UP: `npm run docs:check` has the same clean-base failures in docs/develop/plugins/plugin-apis.md (9287/8000), docs/reference/mac-capture/keyboard.md (6019/6000), docs/reference/mac-capture/protocol.md (6308/6000), and docs/reference/plugins/bob-navigation-hotkeys.md (6029/6000); already tracked by bob-cli-pw.8.1.3.

## Dependencies

- **Depends on:** [bob-cli-pl.6.1.4](bob-cli-pl.6.1.4.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.6.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.1.5.md) | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 6 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6904786`](https://github.com/bobs-org/bob-plugins/commit/69047866eacd505e8a306440c99e71b481cfdf31) | test(props): add real-Obsidian settings acceptance coverage | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 07:15:21 EST |
| bob-plugins | [`bob-plugins@2ec1304`](https://github.com/bobs-org/bob-plugins/commit/2ec1304231ad4d3c6c47b290aab938f8fb57a1b4) | test(property-editor): navigate expanded managed rows in Obsidian acceptance | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 07:58:11 EST |
| bob-plugins | [`bob-plugins@7c34314`](https://github.com/bobs-org/bob-plugins/commit/7c3431499200db62cd062ecab0e2587010a426f6) | test(settings): reopen managed rows after YAML navigation | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 08:15:19 EST |
| bob-plugins | [`bob-plugins@ede02e2`](https://github.com/bobs-org/bob-plugins/commit/ede02e2d8f1982c5336d2430f58eb3e3a234092f) | test(plugins): focus selected rows in acceptance harness | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 09:11:29 EST |
| bob-plugins | [`bob-plugins@8e4f6ad`](https://github.com/bobs-org/bob-plugins/commit/8e4f6adc4c707aaf5407cbf9bb94678918ffec3d) | fix(settings): expand managed property rows in acceptance harness | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 10:18:53 EST |
| bob-plugins | [`bob-plugins@49bdcb8`](https://github.com/bobs-org/bob-plugins/commit/49bdcb85a4979c837779cc0812b8d26e91bf1b24) | fix(property-editor): route source-only marked deletes through shared batch handler | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 11:30:31 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.6.1.5--3][1] | Need current phase scope and blockers before recording acceptance evidence | 1 |
| read-by | [agent:bob-cli-pl.6.1.5--4][1] | Inspect assigned phase status, existing notes, and any remaining work before finishing acceptance | 1 |
| read-by | [agent:bob-cli-pl.6.1.5--5][1] | Verify all failed acceptance artifacts are linked before rerunning | 2 |
| read-by | [agent:bob-cli-pl.6.1.5--7][1] | Verify all failed settings acceptance evidence references are attached before fixing the harness | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.1.5.md

<!-- sase:referenced-by:end -->
