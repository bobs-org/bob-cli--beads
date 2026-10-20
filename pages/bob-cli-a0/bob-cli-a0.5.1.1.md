# Bead: bob-cli-a0.5.1.1 — Publication source selection and manifest contracts

[Bead Pages](../README.md) / [bob-cli-a0.5.1](bob-cli-a0.5.1.md) / bob-cli-a0.5.1.1

**Status:** ✓ closed · **Resolution:** done · **Type:** ↳ phase
**Owner:** `bryanbugyi34@gmail.com` · **Created by:** [bbugyi200.apollo.bob-cli-a0.5](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.bob-cli-a0.5.md) · **Assignee:** `bob-cli-a0.5.1.1` · **Size:** medium
**Created:** 2026-10-19 23:18:31 EDT · **Closed:** 2026-10-19 23:46:04 EDT
**Plan:** [202610/docs\_gated\_publication.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/docs_gated_publication.md)

## Description

source-plan: implement and test publish-plan, deterministic input fingerprints, production source manifests, and hold/pinned/force/drill selection semantics against local Git fixtures.

## Notes

[2026-10-20T03:46:04Z · bob-cli-a0.5.1.1] Implemented publish-plan source selection, versioned publication contracts, deterministic Git-object fingerprints, clean SHA-pinned source checkouts, and hold/pinned/force/drill/recovery semantics. Verified production assembler compatibility and 
✅  DOCS CHECK
────────────────────────────────────────────────
docs-check: assemble and validate source context

docs-check: lint
bob-docs lint: ok
docs-check: passed (lint)

docs-check: generated drift
generated contract content is up to date
docs-check: passed (generated drift)

docs-check: strict Zensical build
Build started
Build finished in 10.03s
running: zensical build --strict --config-file /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/target/docs/mkdocs.yml
built site: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/target/docs/site
docs-check: passed (strict Zensical build)

docs-check: published URLs
wrote /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/target/docs/site/urls.txt (63 published pages)
warning: live https://bobs-org.github.io/urls.txt is not published yet; skipping comparison
urls: OK (63 pages, 419 mentions checked, 1 curated links)
docs-check: passed (published URLs)

docs-check: offline lychee with fragments
🔍 8031 Total (in 679ms) 🔗 1098 Unique ✅ 7612 OK 🚫 0 Errors 👻 419 Excluded

running: /home/bryan/.cache/bob-docs/bin/lychee --offline --no-progress --include-fragments --index-files index.html --root-dir /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/target/docs/site --remap https://bobs-org.github.io/ file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/target/docs/site/ /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/target/docs/site
links: OK (offline lychee with fragment checking)
docs-check: passed (offline lychee with fragments)

docs-check: search smoke
search smoke: OK (2 cases; index /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/target/docs/site/search.json)
docs-check: passed (search smoke)

docs-check: documentation unit tests
============================= test session starts ==============================
platform linux -- Python 3.14.4, pytest-9.1.1, pluggy-1.7.0
rootdir: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/tools/docs
configfile: pyproject.toml
collected 231 items

tools/docs/tests/test_assemble.py ....                                   [  1%]
tools/docs/tests/test_assets.py ....ss                                   [  4%]
tools/docs/tests/test_check.py ...                                       [  5%]
tools/docs/tests/test_contracts.py .......                               [  8%]
tools/docs/tests/test_fences.py .......                                  [ 11%]
tools/docs/tests/test_gen_reference.py ........                          [ 15%]
tools/docs/tests/test_generated.py .....                                 [ 17%]
tools/docs/tests/test_links.py ...........                               [ 22%]
tools/docs/tests/test_lint.py .......................................... [ 40%]
..........                                                               [ 44%]
tools/docs/tests/test_mounts.py ........................................ [ 61%]
.............................                                            [ 74%]
tools/docs/tests/test_publish_plan.py .......................            [ 84%]
tools/docs/tests/test_search_smoke.py ........                           [ 87%]
tools/docs/tests/test_templates.py .s                                    [ 88%]
tools/docs/tests/test_urls.py ........................                   [ 99%]
tools/docs/tests/test_yaml_tools.py ..                                   [100%]

=========================== short test summary info ============================
SKIPPED [1] tools/docs/tests/test_assets.py:64: generation dependencies are absent (run with --group fonts)
SKIPPED [1] tools/docs/tests/test_assets.py:76: fonttools is absent (run with --group fonts)
SKIPPED [1] tools/docs/tests/test_templates.py:170: material builder not installed
======================= 228 passed, 3 skipped in 22.46s ========================
running: uv run --project tools/docs pytest tools/docs/tests
docs-check: passed (documentation unit tests)

docs-check: follow-on gates
skipped: CLI reference golden is a cargo test, not a docs-check gate
skipped: tutorial not implemented in this slice
skipped: media checks not implemented in this slice

docs-check: all implemented gates passed (228 passed, 3 skipped); epic-symbol check found no leftovers.

## Dependencies

- **Blocks:** [bob-cli-a0.5.1.2](bob-cli-a0.5.1.2.md) ◐ · ⧖ 2026-10-19

## Agents

| Agent | Bead | Commits |
|---|---|---:|
| [bbugyi200.apollo.bob-cli-a0.5.1.1](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.1/README.md) | [bob-cli-a0.5.1.1](bob-cli-a0.5.1.1.md) | 0 |

<!-- sase:referenced-by:start -->

## Referenced By

| Relation | Artifact | Why | Uses |
| --- | --- | --- | ---: |
| read-by | [agent:bob-cli-a0.5.1.1][1] | Need the phase scope and design file | 2 |

[1]: https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.bob-cli-a0.5.1.1/README.md

<!-- sase:referenced-by:end -->
