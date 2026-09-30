# Governance

## 1. Purpose

DS Defense is a community coordination project intended to connect related work while preserving clear authorship, provenance, licensing, and maintainer autonomy.

This governance document is intentionally lightweight.

DS Defense is currently in a **bootstrap phase**. The initial repository creator is acting as a coordinator and administrator, not as the technical owner of all work represented by the project.

This document may evolve as more original authors, maintainers, and contributors join.

---

## 2. Core principles

### 2.1 Original authorship is preserved

DS Defense does not claim authorship or ownership of third-party work merely because that work is referenced, documented, or hosted here.

Original attribution should be preserved wherever reasonably possible.

### 2.2 Contribution units are autonomous

Each hosted contribution should be treated as an independent contribution unit.

The repository defines only a small shared interface around such contributions.

Maintainers of an individual contribution are generally free to organize its internal files, code, data, documentation, tests, models, or other materials in the way that best fits that project.

### 2.3 Repository-wide structure should remain minimal

Top-level structure exists to make the repository understandable and maintainable.

It should not unnecessarily impose technical architecture, language choices, project layout, or research methodology on individual contributors.

### 2.4 Provenance matters more than uniformity

It is more important to know:

- where work came from;
- who maintains it;
- what license or permission applies;
- whether DS Defense is hosting or merely referencing it;

than to force every project into the same internal layout.

### 2.5 External hosting is a valid form of participation

A project does not need to move its code into DS Defense in order to participate.

Maintainers may choose to keep their work in an independent repository while being indexed through the DS Defense catalog.

### 2.6 Governance should follow participation

Repository authority should gradually reflect actual participation and maintenance work.

As contributors become active maintainers, repository responsibilities should be shared with them.

---

## 3. Repository areas

DS Defense distinguishes between two major types of project records.

### `catalog/`

The catalog records projects, repositories, research, tools, datasets, or other work that may be relevant to DS Defense.

A catalog entry does not imply:

- endorsement;
- ownership;
- permission to redistribute;
- participation by the original author;
- transfer of copyright;
- agreement with DS Defense governance.

Catalog entries may exist solely to document relationships and provenance.

### `contributions/`

The contributions area contains material that DS Defense is permitted to host.

Each contribution should normally have its own directory:

```text
contributions/<project-id>/
```

The internal structure of that directory is controlled primarily by the maintainers of that contribution.

---

## 4. Roles

Roles describe responsibilities rather than ownership.

### Coordinator

During the bootstrap phase, the repository creator acts as the initial coordinator.

Typical responsibilities include:

- maintaining basic repository infrastructure;
- helping contributors find the correct contribution process;
- maintaining shared documentation;
- coordinating repository-wide discussions;
- inviting additional maintainers;
- helping resolve attribution and provenance questions.

The coordinator does not automatically become the technical maintainer of individual contributions.

### Contribution Maintainer

A Contribution Maintainer is responsible for one or more contribution units.

Contribution Maintainers may:

- review changes affecting their contribution;
- define the internal structure of that contribution;
- maintain its documentation;
- clarify provenance and licensing;
- recommend additional maintainers.

Where possible, changes to an actively maintained contribution should be reviewed by one of its maintainers.

### Repository Maintainer

Repository Maintainers help maintain shared infrastructure and repository-wide policy.

Their responsibilities may include:

- top-level documentation;
- GitHub configuration;
- contribution templates;
- shared metadata conventions;
- repository-wide automation;
- governance documents.

Repository Maintainers should avoid imposing unnecessary technical requirements on independently maintained contribution units.

### Contributor

A Contributor is anyone who improves DS Defense through code, documentation, metadata, research, attribution corrections, project discovery, review, discussion, or other useful work.

---

## 5. Decision scope

Not every change requires the same process.

### Contribution-local decisions

Decisions affecting only one contribution should normally be made by that contribution's maintainers.

Examples include:

- directory layout inside the contribution;
- programming language;
- testing framework;
- model format;
- documentation format;
- internal naming;
- release process.

DS Defense should generally not standardize these unless there is a strong repository-wide reason.

### Repository-wide decisions

Changes that affect multiple contributors or the structure of DS Defense as a whole should be discussed publicly.

Examples include:

- changing top-level repository structure;
- changing required metadata;
- introducing repository-wide licensing rules;
- changing maintainer permissions;
- adding mandatory contribution requirements;
- restructuring multiple existing contributions;
- changing governance.

Major repository-wide proposals should normally be discussed before adoption.

An RFC may be used when the change is substantial.

---

## 6. Bootstrap decision-making

During the early stage of DS Defense, there may not yet be enough maintainers for a formal voting system to be useful.

Therefore:

1. Routine, reversible repository administration may be handled by the initial coordinator or repository maintainers.
2. Changes affecting a specific contribution should involve that contribution's maintainer whenever possible.
3. Significant repository-wide changes should be proposed publicly before adoption.
4. Once multiple active maintainers exist, repository-wide decisions should not depend solely on the original repository creator.
5. When there is disagreement, preserving existing contributor autonomy is preferred over introducing unnecessary new restrictions.

The project may adopt a more formal decision process later if participation grows enough to justify one.

---

## 7. RFC process

The `rfcs/` directory may be used for substantial repository-wide proposals.

Examples include:

- major changes to repository structure;
- metadata schema changes;
- governance changes;
- cross-project interfaces;
- repository-wide automation;
- migration of multiple projects.

An RFC should explain:

```text
Problem

Proposed change

Why the change is needed

Who or what is affected

Alternatives considered

Migration impact, if any

Open questions
```

An RFC is a discussion mechanism, not proof that a proposal has already been accepted.

---

## 8. Contribution ownership and CODEOWNERS

`CODEOWNERS` may be used to route review requests to the people who maintain particular paths.

Code ownership in GitHub is an operational responsibility.

It does **not** imply:

- copyright ownership;
- original authorship;
- exclusive legal rights;
- ownership of third-party projects.

Where an original maintainer joins DS Defense, their contribution path should normally be assigned to them or to the appropriate maintainer team.

---

## 9. Licensing

DS Defense currently does **not** apply a single repository-wide license to all content.

The absence of a repository-wide license should not be interpreted as permission to copy, redistribute, relicense, or create derivative works from repository content.

Each hosted contribution should document the license or other permission that allows DS Defense to host it.

Where licensing or redistribution rights are unclear, the preferred approach is to create a catalog entry linking to the original source rather than copying the material into `contributions/`.

A contribution may use a different license from another contribution.

Repository-wide licensing policy may be revisited later with community participation.

---

## 10. Required information for hosted contributions

A hosted contribution should normally include:

```text
README.md
metadata.yml
```

and, where applicable, appropriate licensing information.

The contribution's `metadata.yml` should identify:

- project name;
- upstream source, if any;
- authors or maintainers where known;
- contribution type;
- hosting status;
- licensing or permission status.

Additional internal structure is determined by the contribution maintainers.

---

## 11. Attribution and corrections

Corrections involving:

- authorship;
- provenance;
- original repository;
- project history;
- licensing;
- maintainer identity;

should be treated as important.

When credible conflicting information exists, the repository should avoid presenting uncertain information as established fact.

Where necessary, an entry may be marked as:

```text
Unconfirmed
Disputed
License unclear
Maintainer unknown
```

until the issue is resolved.

---

## 12. Removal and externalization

A project does not have to remain hosted inside DS Defense permanently.

A contribution may later be:

- moved to an independent repository;
- maintained elsewhere and referenced through the catalog;
- archived;
- reorganized;
- split into multiple projects.

Where possible, such changes should preserve history, attribution, and links to the authoritative source.

If an original maintainer requests that DS Defense stop hosting material and there is uncertainty about redistribution rights, maintainers should prioritize resolving the rights and provenance question before continuing redistribution.

---

## 13. Evolution of this governance

This document is provisional.

It is intended to provide enough structure for collaboration without locking future contributors into decisions made before they joined.

Changes to governance should be proposed publicly and should take into account the views of contributors directly affected by those changes.

The long-term goal is for DS Defense governance to be shaped by the people who actively build and maintain the project.
