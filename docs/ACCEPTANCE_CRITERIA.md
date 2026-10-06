# Acceptance Criteria

The following criteria are derived from the Version 5 handoff baseline and must be traceable to tests as implementation grows.

- AC-01: A search using a pre-reorganization department name can reach the current program/project and related records.
- AC-02: For multi-party information, provider, aggregator, rights holder, custodian, operational manager and publisher can be represented separately with role periods.
- AC-03: Original carrier, preservation file, access file and machine-processing data for one information resource can be related without collapsing them into one file.
- AC-04: Access scope and reuse conditions can be configured independently and unauthorized users cannot receive restricted information.
- AC-05: Human-readable but not structurally machine-readable material can be distinguished from the reverse case.
- AC-06: Currently unreadable or damaged media can be registered as a preservation target while content remains unknown.
- AC-07: From map, drawing, 3D, point cloud, audio or waveform views, users can navigate to related program/project and records when an authorized relationship exists.
- AC-08: AI candidate adoption/correction records actor, time, evidence and the original candidate.
- AC-09: Published datasets expose source/provenance, reference time, update time, CRS when applicable, quality, rights, reuse conditions and acquisition method.
- AC-10: R0–R6 requiredness is enforced consistently in UI/API/workflow validation, including conditional and unknown-state handling.
- AC-11: C0 corrections append evidence and correction events rather than silently overwriting recorded facts.
- AC-12: Current and historical administrative/geographic boundaries can both participate in search where historical extents are available.

Each criterion must eventually map to one or more automated tests or an explicit manual verification procedure.
