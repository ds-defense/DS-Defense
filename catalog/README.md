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

