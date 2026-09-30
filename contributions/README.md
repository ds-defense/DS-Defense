# `contributions/README.md`

# DS Defense Contributions

The `contributions/` directory contains work that DS Defense is permitted to host.

Each contribution is treated as an independent contribution unit.

The purpose of this structure is to provide a predictable repository boundary without forcing every project to use the same internal architecture.

## Contribution boundary

A contribution should normally live at:

```text
contributions/<project-id>/
```

For example:

```text
contributions/example-defense/
```

Everything below that directory may be organized according to the needs of the contribution maintainers.

For example, all of the following are acceptable:

```text
contributions/project-a/
├── README.md
├── metadata.yml
├── src/
└── tests/
```

or:

```text
contributions/project-b/
├── README.md
├── metadata.yml
├── models/
├── datasets/
└── notebooks/
```

or:

```text
contributions/project-c/
├── README.md
├── metadata.yml
└── rules.json
```

DS Defense does not require contributions to share the same internal layout.

## Required files

Each contribution should normally contain:

```text
README.md
metadata.yml
```

The `README.md` should explain what the contribution is and how it relates to DS Defense.

The `metadata.yml` should document provenance, maintainership, integration status, and licensing or permission information.

Where applicable, the contribution should also contain the relevant license information.

## Maintainer autonomy

Contribution maintainers may normally decide:

- directory structure;
- language;
- dependency management;
- documentation format;
- testing framework;
- model or data format;
- release process;
- internal naming conventions.

Repository-wide rules should only be introduced when a shared requirement provides clear value across multiple contributions.

## Hosting requirements

Before substantial third-party material is hosted here, its provenance and hosting basis should be documented.

Examples of a hosting basis include:

```text
original-author-submission
authorized-maintainer-submission
open-source-license
explicit-permission
original-ds-defense-work
```

If the hosting basis is unclear, create or maintain an entry under `catalog/` instead of copying the material into `contributions/`.

## Upstream projects

A contribution may have an independent upstream repository.

In that case, `metadata.yml` should identify it.

DS Defense does not assume that its hosted copy is automatically the authoritative upstream version.

The relationship should be made explicit.

Examples:

```text
mirror
downstream
integration
snapshot
independent-fork
authoritative
```

## Licensing

There is currently no single license that automatically applies to every contribution in DS Defense.

Each contribution should document its own licensing or permission status.

Do not remove upstream copyright, attribution, or license notices.

Do not assume that material can be relicensed merely because it has been contributed to the DS Defense repository.

