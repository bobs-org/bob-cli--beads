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
| related | file:explicit:0968c32776984db9ba2bd327 | attached via sase artifact create --bead |
| related | file:explicit:0b7f5dcd3ad54a06615f0aa3 | attached via sase artifact create --bead |
| related | file:explicit:0f239313ecbd344e0161d93f | attached via sase artifact create --bead |
| related | file:explicit:102101973af2ca32e6bb022d | attached via sase artifact create --bead |
| related | file:explicit:10adb49472e0488fd8f5ff17 | attached via sase artifact create --bead |
| related | file:explicit:12e8f158d3c4e4b13c60ec71 | attached via sase artifact create --bead |
| related | file:explicit:1517ae57c0a2221475089d20 | attached via sase artifact create --bead |
| related | file:explicit:15e6ee9644ddca04b3e15b68 | attached via sase artifact create --bead |
| related | file:explicit:19f53c0edf45ce0e58dee417 | attached via sase artifact create --bead |
| related | file:explicit:1b3799fbd1a777e4bc49ffeb | attached via sase artifact create --bead |
| related | file:explicit:1f140b8a9cfe8c2603d455bc | attached via sase artifact create --bead |
| related | file:explicit:249d3656138a372e3b05e577 | attached via sase artifact create --bead |
| related | file:explicit:2589494040f185f61a254804 | attached via sase artifact create --bead |
| related | file:explicit:25c2cf52c795b8bb980ef342 | attached via sase artifact create --bead |
| related | file:explicit:273b2c658d5b61c382a38a37 | attached via sase artifact create --bead |
| related | file:explicit:35090815a79efcf615498fa8 | attached via sase artifact create --bead |
| related | file:explicit:380437933d2ad00ffe9bf9e5 | attached via sase artifact create --bead |
| related | file:explicit:3d14923815f5249ae65fa5fe | attached via sase artifact create --bead |
| related | file:explicit:41087d9690fc6e75ad958db1 | attached via sase artifact create --bead |
| related | file:explicit:4588b6ec4fe944b9260b1a18 | attached via sase artifact create --bead |
| related | file:explicit:45956d095b4a9c87c12538d7 | attached via sase artifact create --bead |
| related | file:explicit:45dc7735989a011cdf728260 | attached via sase artifact create --bead |
| related | file:explicit:47b5de8060e4fa99bc07a717 | attached via sase artifact create --bead |
| related | file:explicit:4b93754653436b0bea329531 | attached via sase artifact create --bead |
| related | file:explicit:4f7cfabb0cebd0eabd869db5 | attached via sase artifact create --bead |
| related | file:explicit:575ee3b4f1b1d6736814ddb3 | attached via sase artifact create --bead |
| related | file:explicit:61aa57d5ad5f26328e620ffd | attached via sase artifact create --bead |
| related | file:explicit:63a4fe6ed44162080cb82577 | attached via sase artifact create --bead |
| related | file:explicit:677fc7755c631262ce1ab876 | attached via sase artifact create --bead |
| related | file:explicit:69c4fda47ff362a7bffa75f8 | attached via sase artifact create --bead |
| related | file:explicit:69fff6f5a28d0761588ca8af | attached via sase artifact create --bead |
| related | file:explicit:6b2bf0d025a0feb24cb57c47 | attached via sase artifact create --bead |
| related | file:explicit:6b3cd7189b58978001673256 | attached via sase artifact create --bead |
| related | file:explicit:70fdaff98b9a79c329c9afb9 | attached via sase artifact create --bead |
| related | file:explicit:768c90e756f020c43204ce1d | attached via sase artifact create --bead |
| related | file:explicit:7930a61423fb45f7864096c3 | attached via sase artifact create --bead |
| related | file:explicit:7c7732897efd57852e58549d | attached via sase artifact create --bead |
| related | file:explicit:7de1b3a5b07bde5695deaef7 | attached via sase artifact create --bead |
| related | file:explicit:84880df9b16f7a86054bcf04 | attached via sase artifact create --bead |
| related | file:explicit:8e08cc4bfd0c453564c2812f | attached via sase artifact create --bead |
| related | file:explicit:8f8cccda01e4ecab5e121689 | attached via sase artifact create --bead |
| related | file:explicit:92040ed849846fdf0c78fcb1 | attached via sase artifact create --bead |
| related | file:explicit:9a122bd6dbc3cbe6b8dc0bf6 | attached via sase artifact create --bead |
| related | file:explicit:a4c35a9f39b9398dbcf72f92 | attached via sase artifact create --bead |
| related | file:explicit:a7aad6122b88c9990f221c94 | attached via sase artifact create --bead |
| related | file:explicit:ae7eed0a50602d4baca2d591 | attached via sase artifact create --bead |
| related | file:explicit:b487c294be4d48f18d63425b | attached via sase artifact create --bead |
| related | file:explicit:b4a8eb54c2ec5fa6c470a21e | attached via sase artifact create --bead |

_… and 26 more_

_Plus 6 automatic references — see [Referenced By](#referenced-by)._

<!-- sase:links:end -->

## Description

settings-acceptance: extend the scratch-vault harness, exercise settings and generic parity with current bob, inspect screenshots, fix phase-specific regressions, and record deployment and verification evidence.

## Notes

[2026-11-25T12:12:55Z · bob-cli-pl.6.1.5] PROPOSED FOLLOW-UP: `npm run docs:check` has the same clean-base failures in docs/develop/plugins/plugin-apis.md (9287/8000), docs/reference/mac-capture/keyboard.md (6019/6000), docs/reference/mac-capture/protocol.md (6308/6000), and docs/reference/plugins/bob-navigation-hotkeys.md (6029/6000); already tracked by bob-cli-pw.8.1.3.

[2026-11-25T18:08:52Z · bob-cli-pl.6.1.5] Acceptance recovery: latest attached report file:explicit:d4ed91d90e134cdc4dc01091 has 120 passes, then protected-copy timeout before settings scenarios. Fixed the unreachable managed-group expansion by opening the visible keep_exact row first. Also fixed missing bobLog/oldFlag/noContractFlag context and synthetic-row keyboard focus, and reset prior old-Bob capability. Expanded real acceptance for warning saves/undo, every fixture chip, exact theme/clock and ghost copy, retired-count delete/undo, IME Enter, settings geometry, and no-write repaint. Focused suites 67/67; latest offline harness 13/13; build:check and validate 12/12 pass. Plugin sync from opened checkout succeeds with 0 copied/0 skipped/3 unchanged, deployed source c9454208. No epic symbols. Full tests and real Obsidian verification will run from clean post-finalization source bundles through .build/settings-acceptance/run.sh; results pointer .build/settings-acceptance/latest-run. Phase remains in progress pending actual run and image review; no product-code changes in this recovery.

[2026-11-25T18:42:11Z · bob-cli-pl.6.1.5--1] Reviewed monitor vc3zr2 independently: real Obsidian 220 assertions pass, then bank-close timeout; no console exceptions. npm unit 9522 pass/14 fail/3 skip (same failures on retry), perf 26/26; validate 12/12; docs 2 reference budget errors plus develop warning. Exact report file:explicit:4b93754653436b0bea329531; all 25 individually viewed image hashes/verdicts and check summary file:explicit:0968c32776984db9ba2bd327; complete report/logs/PNG archive file:explicit:575ee3b4f1b1d6736814ddb3. Six narrow stage screenshots were insufficient because controls were offscreen; no visual acceptance claimed. Failure screenshot proves the bank modal closed while the inline panel remained. Fixed open/close probes to use the actual bank modal, corrected invalid project-task/hierarchy/status fixtures, added real-Bob fixture preflight, awaited/closed actual Task Cards, reset capability before settings screenshots, and scrolled/asserted stage visibility/focus. Same monitored Bob binary confirms corrected nested/top-level root and exact ^prj fixtures. Focused 54/54 plus harness 13/13 pass; build/validate pass. No production plugin code/generated bundle changes. Sync FROM OPENED checkout passes 0 copied/0 skipped/3 unchanged; clean deployment stamp c9454208ac8eede09f338c328ab640166ea3168e. Ledger main SHA256 d22e17c2dbc002013f8621b7ed59cff28b4c637bc8ec7d8edc09f5faf891304b; CSS 91464604824c5c00cfba95141dad1669af2c1a7d2d637c405fc6f504eae29bb7. Original run CLI 0742684de3390415ffb5dbb3423c0dbc841f4b3e and binary e6a18bcd29783d4fda9bcb3eb5ab5fff185ce17208c05e64aa585da2cb7b5c5c, plugins 689da09262ecd1492cc1bc52e84cebad2fb79631. Opened plugin base now abbac5acc380b651c091657d40f77d43680a9054 (test-only upstream change). Prepared next monitor to run full npm on that clean base and finalized current source, isolated timing reproduction, validate, real Obsidian, and docs base/current; correct nested clone layout fixes two harness-environment fixture ENOENTs. New follow-up notes await actual clean-base proof. Foundation bob-cli-pf remains closed; epic-symbols empty. Phase stays in progress pending complete app run and new image review; no ancestors closed or new beads created.

## Dependencies

- **Depends on:** [bob-cli-pl.6.1.4](bob-cli-pl.6.1.4.md) ✓ · ⧖ 2026-11-24

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pl.6.1.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.1.5.md) | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 9 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-plugins | [`bob-plugins@6904786`](https://github.com/bobs-org/bob-plugins/commit/69047866eacd505e8a306440c99e71b481cfdf31) | test(props): add real-Obsidian settings acceptance coverage | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 07:15:21 EST |
| bob-plugins | [`bob-plugins@2ec1304`](https://github.com/bobs-org/bob-plugins/commit/2ec1304231ad4d3c6c47b290aab938f8fb57a1b4) | test(property-editor): navigate expanded managed rows in Obsidian acceptance | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 07:58:11 EST |
| bob-plugins | [`bob-plugins@7c34314`](https://github.com/bobs-org/bob-plugins/commit/7c3431499200db62cd062ecab0e2587010a426f6) | test(settings): reopen managed rows after YAML navigation | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 08:15:19 EST |
| bob-plugins | [`bob-plugins@ede02e2`](https://github.com/bobs-org/bob-plugins/commit/ede02e2d8f1982c5336d2430f58eb3e3a234092f) | test(plugins): focus selected rows in acceptance harness | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 09:11:29 EST |
| bob-plugins | [`bob-plugins@8e4f6ad`](https://github.com/bobs-org/bob-plugins/commit/8e4f6adc4c707aaf5407cbf9bb94678918ffec3d) | fix(settings): expand managed property rows in acceptance harness | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 10:18:53 EST |
| bob-plugins | [`bob-plugins@49bdcb8`](https://github.com/bobs-org/bob-plugins/commit/49bdcb85a4979c837779cc0812b8d26e91bf1b24) | fix(property-editor): route source-only marked deletes through shared batch handler | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 11:30:31 EST |
| bob-plugins | [`bob-plugins@475527c`](https://github.com/bobs-org/bob-plugins/commit/475527caa1eee0469d7553de51b503a4e8237afb) | test(bob-ledger-tools): expand managed group before protected copy | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 12:14:58 EST |
| bob-plugins | [`bob-plugins@689da09`](https://github.com/bobs-org/bob-plugins/commit/689da09262ecd1492cc1bc52e84cebad2fb79631) | test(settings): unblock Obsidian acceptance and cover setting writes | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 13:10:32 EST |
| bob-plugins | [`bob-plugins@fd2a290`](https://github.com/bobs-org/bob-plugins/commit/fd2a2907fdba71ee5389d73a330eef30897b3746) | test(settings): correct Obsidian fixtures and visible acceptance probes | [bob-cli-pl.6.1.5](bob-cli-pl.6.1.5.md) | 2026-11-25 13:43:55 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pl.6.1.5--3][1] | Need current phase scope and blockers before recording acceptance evidence | 1 |
| read-by | [agent:bob-cli-pl.6.1.5--4][1] | Inspect assigned phase status, existing notes, and any remaining work before finishing acceptance | 1 |
| read-by | [agent:bob-cli-pl.6.1.5--5][1] | Verify all failed acceptance artifacts are linked before rerunning | 2 |
| read-by | [agent:bob-cli-pl.6.1.5--7][1] | Verify all failed settings acceptance evidence references are attached before fixing the harness | 1 |
| read-by | [agent:bob-cli-pl.6.1.5--8][1] | Review design link and current acceptance notes | 7 |
| read-by | [agent:bob-cli-pl.6.1.5--9][1] | Verify every failed-run acceptance artifact is attached before the corrected rerun | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pl.6.1.5.md

<!-- sase:referenced-by:end -->
