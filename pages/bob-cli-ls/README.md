# Bead: bob-cli-ls — Subscriptions album: records that know how they show up on the statement

[Bead Pages](../README.md) / bob-cli-ls

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.athena.1cp](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cp.md) · **Assignee:** `bob-cli-ls.land`
**Created:** 2026-11-15 13:11:21 EST · **Closed:** 2026-11-16 00:52:36 EST
**Plan:** [202611/bank\_subscriptions\_album.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_subscriptions_album.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/bank_subscriptions_album.md][1] | derived from the plan's `bead_id:` frontmatter field |
| related | [bead:bob-cli-m3][2] | Subscriptions album epic: owns candidate findings, the proposal JSON, and the Category-card linker this action extends |

_Plus 4 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/bank_subscriptions_album.md
[2]: https://github.com/bobs-org/bob-cli--beads/blob/main/pages/bob-cli-m3/README.md

<!-- sase:links:end -->

## Description

A 🔁 Subscriptions album under bank holds every discretionary recurring charge, seeded from a reviewed bank history. bob bank import links each new matching row to its record, and the link renders as a quiet 🔁 chip. bob bank check and bob bank subscriptions keep the album honest: they flag price changes, charges after a cancel, and possible new subscriptions. The old Zorg recurring table retires without losing a link, and bob-cli-kt closes.

## Notes

[2026-11-16T01:13:27Z · 1cv--1] DISCOVERED ISSUE: kr closeout check and source build on clean bob-cli 893bd2af failed E0061 at check_subscriptions.rs:58 and test line 1105 because compute_ledger gained config/raw_descs arguments. Evidence file:explicit:afa1a0e6e83c8ef403056363. This is already repaired by f252f185 (bank subscriptions report); this checkout fast-forwarded to 7729a962 for final verification. No new task.

[2026-11-16T03:56:31Z · bob-cli-ls.land] LAND TRIAGE (bob-cli-ls.land) of every child PROPOSED FOLLOW-UP:
(1) ls.3 #1, legacy_eat duplicate block IDs: not caused by this epic. Corroborated existing bob-cli-kz with +1.
(2) ls.7 #2 and ls.9 #2, Live Preview 200-link wall-clock flakes: not caused by this epic. Corroborated bob-cli-km, bob-cli-ki, and bob-cli-ju with +1 each.
(3) ls.9 #1, linker test file not registered in package.json test:unit: caused by ls.8. Kept as epic work in the landing tale.
(4) ls.4 #1, ls.5 #1, ls.6 #1, ls.7 #1, ls.8 #1, ls.9 #3, ls.10 #1, bob-ledger-tools.md over the 6000-word cap: partly caused by this epic. Chips, linker, and surfaces added about 226 words (6055 -> 6281), and lt.8 brought the page to 6302. The landing tale trims the page to 6000 words or fewer, as earlier landers did. No new task; bob-cli-il keeps its separate 300-word headroom goal.
(5) Lander-discovered, not caused by this epic: dismissing a candidate through bob-cli-lt's guarded rule.add writer. Filed feature bob-cli-m3 (medium, ready).
Declined:
- LedgerSnapshot.diagnostics (amount overflow, link/row-id ambiguity) and non-amount record_invalid diagnostics never reach bank check. The plan's findings table defines no code for them, schema errors already surface in bob records check and bob albums check, and ambiguous links surface as bank_subscription_overlap.
- 'bob bank subscriptions -a leaves the JSON list unchanged' is deliberate: JSON is the full data source for the plugin surfaces.
- 'the linker picker cannot show cancelled records' is a false alarm: the JSON always lists every record.

[2026-11-16T05:52:36Z · bob-cli-ls.land--2] Parts A-C land verified. just check green (lib 7215 pass, cli 3687 pass; one zsh-adapter load flake passes in isolation). docs lint green: json-outputs 5999 words, ledger-tools plugin page 5998 words, both under the 6000 cap; one pre-existing docs unit-test failure (capture-token coverage, fails identically on the clean tree, unrelated to this plan). Plugin full-suite wall-clock flakes green in isolation with tracked beads cited: event-link-times km 23/23, frees-marks io 17/17, keep-moving-surface ki 14/14, off-clock-chips ju 56/56. Vault read-only: bank check 0 findings with 0 errors/0 warnings; bank subscriptions 28 records with 0 errors/0 warnings and 0 findings; bank list -a 11 rows with 0 waiting and 2 subscription rows both carrying latest. Integrations 10 (bank membership line, usage, snapshots, docs) and 11 (category.remove counts subscription records, refuses with category_in_use, missing album allows removal) done with tests. No just symvision recipe defined. No epic-symbol entries.

## Phases

| Bead | Title | Status | Size | Created | Agents | Commits |
|---|---|---|---|---|---:|---:|
| [bob-cli-ls.1](bob-cli-ls.1.md) | Seed the album from a reviewed bank history | ✓ closed | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.10](bob-cli-ls.10.md) | Vault acceptance, memory, and closing bob-cli-kt | ✓ closed | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.2](bob-cli-ls.2.md) | Subscription registry, match resolver, and ledger | ✓ closed | large | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.3](bob-cli-ls.3.md) | Retire old\_recur.md into a legacy\_recur notebook | ✓ closed | medium | 2026-11-15 | 1 | 0 |
| [bob-cli-ls.4](bob-cli-ls.4.md) | Import links new rows to their subscription | ✓ closed | medium | 2026-11-15 | 1 | 1 |
| [bob-cli-ls.5](bob-cli-ls.5.md) | Subscription findings in bob bank check | ✓ closed | medium | 2026-11-15 | 1 | 1 |
| [bob-cli-ls.6](bob-cli-ls.6.md) | The bob bank subscriptions command | ✓ closed | medium | 2026-11-15 | 1 | 1 |
| [bob-cli-ls.7](bob-cli-ls.7.md) | 🔁 chips on bank rows | ✓ closed | medium | 2026-11-15 | 1 | 1 |
| [bob-cli-ls.8](bob-cli-ls.8.md) | Category card subscription linker | ✓ closed | medium | 2026-11-15 | 1 | 1 |
| [bob-cli-ls.9](bob-cli-ls.9.md) | Record header strip and album summary card | ✓ closed | medium | 2026-11-15 | 1 | 1 |

## Lineage

```mermaid
flowchart TD
    n0["bob-cli-ls: Subscriptions album: records that know how they show up on the statement [closed]"]
    n1["bob-cli-ls.1: Seed the album from a reviewed bank history [closed]"]
    n2["bob-cli-ls.10: Vault acceptance, memory, and closing bob-cli-kt [closed]"]
    n3["bob-cli-ls.2: Subscription registry, match resolver, and ledger [closed]"]
    n4["bob-cli-ls.2.1: Subscription registry, attribution, and ledger core [closed]"]
    n5["bob-cli-ls.2.1.1: Typed subscription registry and deterministic matching [closed]"]
    n6["bob-cli-ls.2.1.2: Shared charge attribution and subscription ledger [closed]"]
    n7["bob-cli-ls.2.1.3: Guarded loaders, row JSON, suggestions, and documentation [closed]"]
    n8["bob-cli-ls.3: Retire old_recur.md into a legacy_recur notebook [closed]"]
    n9["bob-cli-ls.4: Import links new rows to their subscription [closed]"]
    n10["bob-cli-ls.5: Subscription findings in bob bank check [closed]"]
    n11["bob-cli-ls.6: The bob bank subscriptions command [closed]"]
    n12["bob-cli-ls.7: 🔁 chips on bank rows [closed]"]
    n13["bob-cli-ls.8: Category card subscription linker [closed]"]
    n14["bob-cli-ls.9: Record header strip and album summary card [closed]"]
    n0 --> n1
    n0 --> n2
    n0 --> n3
    n3 --> n4
    n4 --> n5
    n4 --> n6
    n4 --> n7
    n0 --> n8
    n0 --> n9
    n0 --> n10
    n0 --> n11
    n0 --> n12
    n0 --> n13
    n0 --> n14
    n1 -.-> n8
    n3 -.-> n9
    n3 -.-> n10
    n3 -.-> n11
    n3 -.-> n12
    n5 -.-> n6
    n5 -.-> n7
    n6 -.-> n7
    n8 -.-> n2
    n9 -.-> n2
    n10 -.-> n11
    n11 -.-> n13
    n11 -.-> n14
    n12 -.-> n13
    n13 -.-> n14
    n14 -.-> n2
```

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.athena.bob-cli-ls.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.1.md) | [bob-cli-ls.1](bob-cli-ls.1.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.10](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.10/README.md) | [bob-cli-ls.10](bob-cli-ls.10.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.md) | [bob-cli-ls.2](bob-cli-ls.2.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.2.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.1.1.md) | [bob-cli-ls.2.1.1](bob-cli-ls.2.1.1.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.2.1.2](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.1.2.md) | [bob-cli-ls.2.1.2](bob-cli-ls.2.1.2.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.2.1.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.2.1.3/README.md) | [bob-cli-ls.2.1.3](bob-cli-ls.2.1.3.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.2.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.2.1.land.md) | [bob-cli-ls.2.1](bob-cli-ls.2.1.md) | 2 |
| [bbugyi200.athena.bob-cli-ls.3](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.3/README.md) | [bob-cli-ls.3](bob-cli-ls.3.md) | 0 |
| [bbugyi200.athena.bob-cli-ls.4](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.4/README.md) | [bob-cli-ls.4](bob-cli-ls.4.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.5.md) | [bob-cli-ls.5](bob-cli-ls.5.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.6](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.6/README.md) | [bob-cli-ls.6](bob-cli-ls.6.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.7](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.7/README.md) | [bob-cli-ls.7](bob-cli-ls.7.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.8](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.8.md) | [bob-cli-ls.8](bob-cli-ls.8.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.9](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.9/README.md) | [bob-cli-ls.9](bob-cli-ls.9.md) | 1 |
| [bbugyi200.athena.bob-cli-ls.land](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.bob-cli-ls.land.md) | [bob-cli-ls](README.md) | 2 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli | [`96b35f4`](https://github.com/bobs-org/bob-cli/commit/96b35f41c4d20cecc065e85e2fe5ac1d8d191c2c) | feat(bank): add subscription attribution and ledger | [bob-cli-ls.2.1.2](bob-cli-ls.2.1.2.md) | 2026-11-15 16:08:32 EST |
| bob-cli | [`055f9b6`](https://github.com/bobs-org/bob-cli/commit/055f9b6e0558c8458ac37a20d0533f22ac4d5d77) | feat(bank): integrate subscription core into rows, suggestions, and docs | [bob-cli-ls.2.1.3](bob-cli-ls.2.1.3.md) | 2026-11-15 16:51:38 EST |
| bob-cli | [`b8aed5a`](https://github.com/bobs-org/bob-cli/commit/b8aed5a943242a5517a6f536de9914432193ed90) | fix(bank): repair subscription core ledger, import after-state, and guards | [bob-cli-ls.2.1](bob-cli-ls.2.1.md) | 2026-11-15 17:58:47 EST |
| bob-cli--plans | [`bob-cli--plans@594215a`](https://github.com/bobs-org/bob-cli--plans/commit/594215ae91c9d361ab200f833ee8dbf82f45ea2e) | docs: mark subscription core epic plan done | [bob-cli-ls.2.1](bob-cli-ls.2.1.md) | 2026-11-15 17:59:49 EST |
| bob-plugins | [`bob-plugins@cd14e67`](https://github.com/bobs-org/bob-plugins/commit/cd14e675b165530ece3797f697df4e790ec3ddbf) | feat(bank): paint state-aware 🔁 subscription chips on bank rows | [bob-cli-ls.7](bob-cli-ls.7.md) | 2026-11-15 18:31:27 EST |
| bob-cli | [`cfd4548`](https://github.com/bobs-org/bob-cli/commit/cfd4548a2cd60a165fdbdc67bd0472e2d6968343) | feat(bank): add native bank checks and subscription registry | [bob-cli-ls.5](bob-cli-ls.5.md) | 2026-11-15 18:48:43 EST |
| bob-cli | [`219e854`](https://github.com/bobs-org/bob-cli/commit/219e854eab66ef329e1b9a5b21873f98279153f0) | feat(bank): link import rows to subscriptions with summary | [bob-cli-ls.4](bob-cli-ls.4.md) | 2026-11-15 18:59:57 EST |
| bob-cli | [`f252f18`](https://github.com/bobs-org/bob-cli/commit/f252f1856abc3ef2f12c6e7555f7c6964b484979) | feat(bank): add bank subscriptions report command | [bob-cli-ls.6](bob-cli-ls.6.md) | 2026-11-15 19:52:02 EST |
| bob-plugins | [`bob-plugins@a6eaea6`](https://github.com/bobs-org/bob-plugins/commit/a6eaea6601cbd9c891d34ab6f49e8b55697cb8c5) | feat(bank): link subscriptions from the Category card | [bob-cli-ls.8](bob-cli-ls.8.md) | 2026-11-15 20:58:39 EST |
| bob-plugins | [`bob-plugins@cb885ca`](https://github.com/bobs-org/bob-plugins/commit/cb885cad16ccf013466b5b1ee8ebe89c7d75834c) | feat(bank): add subscription header strip and album summary card | [bob-cli-ls.9](bob-cli-ls.9.md) | 2026-11-15 21:43:22 EST |
| bob-cli | [`5dec7c5`](https://github.com/bobs-org/bob-cli/commit/5dec7c52c22729c2a566cb7ea178859943eb2e93) | fix(bank): land subscription gaps from the landing review | [bob-cli-ls](README.md) | 2026-11-16 01:06:31 EST |
| bob-plugins | [`bob-plugins@0aa5de3`](https://github.com/bobs-org/bob-plugins/commit/0aa5de358ac5052d5a9721bd731150a32aa6e8cd) | fix(bank): land subscription linker, surfaces, and docs cap | [bob-cli-ls](README.md) | 2026-11-16 01:11:30 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:1cv--1][1] | Inspect exact scope and prior evidence for unrelated check failures | 2 |
| read-by | [agent:bob-cli-lr.land][2] | Check whether bank subscription registry dead code breaking just check on master is tracked in-flight work | 1 |
| read-by | [agent:bob-cli-ls.7][3] | Need parent epic DECISIONS and overall design | 1 |
| read-by | [agent:bob-cli-ls.9][4] | Need parent epic scope, phase list, and land requirements for subscriptions album | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.1cv.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-lr.land/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.7/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.bob-cli-ls.9/README.md

<!-- sase:referenced-by:end -->
