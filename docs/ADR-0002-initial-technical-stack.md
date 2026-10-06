# ADR-0002: Initial technical stack and implementation sequence

- Status: Proposed
- Date: 2026-10-06

## Context

The design baseline fixes the domain concepts and implementation boundaries but intentionally does not make CKAN the authoritative model. Codex needs a reproducible starting point without prematurely locking the publication catalog.

## Decision

For the first implementation milestone:

- Python is the primary server-side implementation language.
- PostgreSQL is the authoritative relational store candidate.
- PostGIS is used when spatial persistence/search is introduced.
- Domain and service modules under `src/` must remain independent from CKAN-specific entities.
- HTTP/API, search, object storage and publication catalog integrations are adapters around the domain core.
- Automated tests are required before catalog/GIS/viewer expansion.
- CKAN adoption remains a later adapter decision and must not alter core identifiers or history semantics.

Exact framework/package versions are intentionally deferred until the executable scaffold PR, where compatibility can be verified by CI.

## Implementation sequence

1. Domain vocabulary, stable identifiers, R0–R6 and C0–C4.
2. Agent/RoleAssignment and validity history.
3. InformationResource/Representation/FileOrBitstream/PhysicalCarrier.
4. RightsStatement and AccessPolicy.
5. Provenance, preservation and quality.
6. Persistence and authorized search.
7. Registration/detail/history/audit API.
8. GIS/viewers and publication adapters.

## Consequences

- Codex can start domain work without inventing a CKAN-shaped schema.
- Framework choices remain reversible during the first scaffold.
- CI becomes the evidence for supported runtime versions.
