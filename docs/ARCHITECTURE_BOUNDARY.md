# Architecture Boundary

## Core domain

The authoritative core must be implementation-independent and persist at least:

- InformationResource
- Representation
- FileOrBitstream
- PhysicalCarrier
- Function / Policy / Measure / Program(Project) / Case
- Agent and RoleAssignment
- SpatialExtent and TemporalExtent
- ProvenanceEvent
- RightsStatement
- AccessPolicy
- PreservationAction
- QualityStatement
- Relationship

PostgreSQL/PostGIS is the default architectural candidate for core metadata and spatial relationships, subject to ADR confirmation.

## Boundaries

### Core application
Owns identifiers, classification, relationships, validity periods, provenance, rights/access, preservation, quality, workflow decisions and auditability.

### Object/file storage
Owns immutable or controlled bitstreams, checksums and storage locations. A file is not the same entity as an information resource.

### Search
Indexes only information the requesting principal is authorized to discover. Search counts and facets must not leak restricted records.

### Viewer
2D/3D/CAD/raster/point-cloud/audio/waveform/time-series viewers consume authorized representations. Viewer availability never changes the underlying access policy.

### Publication/catalog
May be CKAN or another implementation. Receives publishable metadata/representations through API or synchronization. It is not the source of truth for the core domain.

### Automation/AI
Performs extraction, candidate generation and conflict detection. Store processing method/model, execution time, inputs, evidence, confidence and human confirmation state. Rights, access, disposal/transfer, restoration treatment and official corrections require human determination.

## Implementation guardrails

- Do not model current department as owner of a record.
- Do not overwrite historical organization names/assignments after reorganization.
- Do not merge access scope with license/reuse conditions.
- Do not infer machine readability solely from file extension.
- Do not discard unreadable/damaged physical media merely because content is currently inaccessible.
- Do not hard-code CKAN entities into the core domain.
- Preserve Version 5 as reference material; successor code belongs under src/.
