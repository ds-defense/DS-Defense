# `catalog/README.md`

# DS Defense Catalog

The `catalog/` directory is a registry of projects, repositories, research, datasets, tools, models, documentation, and other work that may be relevant to DS Defense.

A catalog entry is primarily a **provenance and discovery record**.

It does not mean that DS Defense owns, hosts, endorses, or has permission to redistribute the referenced work.

## Directory structure

Each project should normally have its own directory:

```text
catalog/
├── project-a/
│   └── metadata.yml
├── project-b/
│   └── metadata.yml
└── project-c/
    └── metadata.yml
```

Use a stable, lowercase project identifier where practical.

For example:

```text
catalog/example-defense/
```

## Minimum contents

A catalog entry should normally contain:

```text
metadata.yml
```

An optional `README.md` may be added when additional context is useful.

## What belongs in the catalog?

The catalog is appropriate when:

- a relevant project exists elsewhere;
- the authoritative version should remain in another repository;
- the original maintainer has not yet joined DS Defense;
- licensing or redistribution rights are unclear;
- DS Defense only needs to document or link to the project;
- a project is relevant historically but is not being actively integrated.

## What should not be copied into the catalog?

Do not copy third-party source code, datasets, models, papers, or other substantial materials into a catalog entry merely because they are publicly accessible.

When rights are unclear, record the authoritative source instead.

For example:

```yaml
upstream:
  repository: https://github.com/example/project

integration:
  mode: external
```

## Catalog status

Catalog entries may describe their status using metadata such as:

```text
unconfirmed
confirmed
contacted
active
inactive
archived
maintainer-unknown
license-unclear
```

These labels are informational.

They should not be interpreted as judgments about the quality or legitimacy of a project.

## Moving from catalog to contributions

A project may move from being catalog-only to being hosted under `contributions/` when there is a sufficient basis to host the material.

Examples may include:

- submission by the original author;
- submission by an authorized maintainer;
- an applicable license permitting redistribution;
- explicit permission from the relevant rights holder;
- original work created directly within DS Defense.

The catalog entry may remain after hosting begins so that upstream provenance remains visible.

## Corrections

If you are an original author or maintainer and a catalog entry incorrectly describes your work, please open an Issue or Pull Request.

Corrections to:

- authorship;
- project name;
- repository URL;
- licensing;
- maintenance status;
- project relationships;

are welcome.

---

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

## CODEOWNERS

Once a contribution has an identified maintainer, its path should normally be added to `.github/CODEOWNERS`.

For example:

```text
/contributions/example-defense/ @example-maintainer
```

This helps route Pull Requests to the people responsible for that contribution.

CODEOWNERS identifies review responsibility, not copyright ownership.

## Moving a contribution

A contribution may later move to another repository or become independently maintained.

This is acceptable.

DS Defense should prioritize:

- preserving attribution;
- preserving project history where practical;
- maintaining working references;
- identifying the authoritative upstream location.

The repository structure exists to support contributors, not to permanently contain them.
