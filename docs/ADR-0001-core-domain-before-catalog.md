# ADR-0001: Keep the core domain independent from the publication catalog

- Status: Accepted
- Date: 2026-10-05

## Context

The platform must represent administrative-function classification, multi-agent role history, changing rights/access conditions, physical carriers, preservation/restoration events and compound viewers. A conventional catalog model alone does not cover these requirements.

## Decision

The authoritative domain model is independent from CKAN or any other publication catalog. A catalog may be connected through API or synchronization and may provide public discovery, but catalog organizations/datasets/resources are not authoritative core entities.

## Consequences

- Core identifiers and history survive catalog replacement.
- CKAN remains an implementation option rather than a prerequisite.
- Publication adapters must respect access and rights policy.
- Domain-to-catalog mapping requires explicit tests.
