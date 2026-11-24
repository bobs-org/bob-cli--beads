# Bead: bob-cli-pf.6.1 — Complete card frontmatter takeover

[Bead Pages](../README.md) / [bob-cli-pf.6](bob-cli-pf.6.md) / bob-cli-pf.6.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ▸ plan · **Tier:** epic
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-pf.6](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-pf.6.md) · **Assignee:** `bob-cli-pf.6.1.land`
**Created:** 2026-11-23 20:38:15 EST · **Closed:** 2026-11-24 09:11:50 EST
**Plan:** [202611/frontmatter\_takeover.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202611/frontmatter_takeover.md)

<!-- sase:links:start -->

## Links

| Relation | Artifact | Why |
| --- | --- | --- |
| implemented-by | [plan:202611/frontmatter_takeover.md][1] | derived from the plan's `bead_id:` frontmatter field |

_Plus 5 automatic references — see [Referenced By](#referenced-by)._

[1]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/frontmatter_takeover.md

<!-- sase:links:end -->

## Description

Eligible mounted cards replace native in-document Properties without losing keyboard editing, native recovery, sidebar access, or source fidelity.

## Notes

[2026-11-24T14:11:50Z · bob-cli-pf.6.1.land] Land verified all 5 phases closed with notes addressed. Code review (bob-plugins 305b637c..b1413ba9): 240q primitive + mount coordinator gates ownership on mounted card+foot, desktop Live Preview/Reading, non-denied scope (embed/popover/canvas/print), closed duplicate-free source matching the metadata cache, confirmed props_v1 for the current bob key, and installed command routing; releases on Source/file change (same CM transaction), cache change, rename/delete, capability loss, mount loss, unload; CSS scoped to the owned class (no global .metadata-container rule); bank excluded (kinds album/record/day/week/quarter/year only). 298v caches confirmed/absent/unconfirmed per bob path with in-flight dedupe and bounded retry, wraps markdown:add-metadata-property (checkCallback preserved, own wrapper restored only), routes owned scopes to openPropertyEditor add, releases before native fallback; 241d routes notebookFocusSummaryProperty to key summary only on owned scopes, sidebar stays native; metadataEditor/.metadata-property audit found no other native focus paths. Decisions honored: bank_foot=yes (bank keeps native block), drawer_memory=note unchanged, glossary edits limited to property-card/record-card (bob-cli e3e437ba), no decision records. Reran: npm run build:check green; 21 focused takeover/ownership/routing/adapter/offline-wrapper test files 423/423 pass; all fragments <=1000 lines; bob plugins list synced and sync dry-run up to date; sase memory init --check no drift from this epic. Acceptance evidence: pf.6.1.4 real Obsidian 1.15.1 GO 51/51, 46 inspected captures, archive file:explicit:85b3b710894edb85fafa6063 (sha256 3ad1198d... verified), all modes supported (no S1-denied mode, no retained per-mode fallback beyond the designed per-row fallback while capability/evidence is uncertain). Integration: only non-epic commit since start is bob-plugins da688dd3 (bare - / + drawer/editor keys); pf.6.1.4 retested on da688dd3+fix (3824ce55) and pf.6.1.5 documented bare -/+, no stale =-/=+ refs remain; bob-cli had no other commits since start; upstream of both repos fetched and current. Follow-ups: perf-budget flakes corroborated on bob-cli-km (event-link-times) and bob-cli-io (frees-marks); held-lock self-test corroborated on bob-cli-n0; capture-sigils unresolved glossary links corroborated on bob-cli-ga; none caused by this epic, no new tasks. epic-symbols: none for pf.6.1 or pf.6.

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-pf.6.1.land](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.land/README.md) | [bob-cli-pf.6.1](bob-cli-pf.6.1.md) | 1 |

## Commits

| Repo | Commit | Subject | Bead | Committed |
|---|---|---|---|---|
| bob-cli--plans | [`bob-cli--plans@a0d608f`](https://github.com/bobs-org/bob-cli--plans/commit/a0d608ff6d7a3d009797d05b5540d5d09422400d) | chore(plans): mark frontmatter takeover epic plan done | [bob-cli-pf.6.1](bob-cli-pf.6.1.md) | 2026-11-24 09:13:09 EST |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-pf.6.1.1][1] | Need ancestor epic scope and decisions | 1 |
| read-by | [agent:bob-cli-pf.6.1.3][2] | Need inherited decisions and phase completion evidence for the adapter takeover | 1 |
| read-by | [agent:bob-cli-pf.6.1.5][3] | Need inherited decisions and completed verification evidence for docs phase | 1 |
| read-by | [agent:bob-cli-pf.6.1.land][4] | Need the epic scope, children, and linked plan file | 1 |
| read-by | [agent:fx][5] | Assess pf.6 takeover remaining work vs pl dependency | 1 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.1/README.md
[2]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.3/README.md
[3]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.5/README.md
[4]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-pf.6.1.land/README.md
[5]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.fx/README.md

<!-- sase:referenced-by:end -->
