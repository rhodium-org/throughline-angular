# throughline-angular

The official **Angular Style Guide** expressed as a
[throughline](https://pypi.org/project/throughline/) **source** — a standalone,
grounded requirements graph that a consuming project composes with
`tl` from [throughline](https://pypi.org/project/throughline/) 3.11.0 or later.

This repository holds no code. It is a directory of small YAML items with permanent
UIDs, validated by `tl check`. Consumers import it under a namespace and reference its
rules as `angular:SR-0001`.

## A framework-style source

`throughline-angular` is a **framework style** source: it governs how Angular
applications are structured and authored, orthogonal to the language source you compose
alongside it. An Angular project would typically compose `throughline-typescript`
(language) **and** `throughline-angular` (framework) at once.

## Status

<!-- tl:count type == 'user_requirement' -->
9
<!-- tl:end --> sections and
<!-- tl:count type == 'system_requirement' -->
36
<!-- tl:end --> style rules, published to [`docs/spec.md`](docs/spec.md):

- `INT-0001` — the root intent (why the guide exists), `normative: false`.
- Each major guide section as a `user_requirement` that `derives_from` the intent.
- Every individual rule as a `system_requirement` that `implements` its section,
  carrying the guide reference in `attrs.source_ref`.

The counts above are rendered from the live graph by the `tl:count` directive, so they
cannot drift.

## Editions — dated tags

The guide is a living document. A material revision is cut as a dated tag on this repo
(e.g. `v2026-08`); a consumer pins the ref it wants.

## Composing it

```toml
[[sources]]
namespace = "angular"
url = "https://github.com/rhodium-org/throughline-angular"
ref = "v2026-08"
```

Then reference a rule from your own items:

```yaml
links:
- target: angular:SR-0001      # Angular Style Guide: apply the single responsibility principle per file
  type: satisfies
```

`tl check` in the consuming project composes this source and resolves the reference.
A `tl` older than 3.11.0 reports it as `namespace-unresolved`.

## Local checks

```sh
pip install throughline
tl check --strict     # the graph must stay sound
tl docs --check       # docs/spec.md must match the graph
```

## Provenance

The Angular Style Guide is © Google, licensed CC BY 4.0. See [NOTICE](NOTICE) and
https://angular.dev/style-guide. This repository is Apache-2.0 for its structure and
tooling; the reproduced rule text remains Google's and the Angular contributors'.
