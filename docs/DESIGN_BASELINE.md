# Design Baseline

## Status

This document fixes the design baseline to be handed to Codex. The successor implementation in this repository is the main development line. Version 5 is a reference implementation for information architecture, UI/interaction, VI and fictional test data; it must not be overwritten.

## Authoritative design principles

1. Primary classification is **administrative function → policy → measure → program/project → case → information resource**. Organization charts are not the primary classification.
2. Organizations and other agents are modeled by role and validity period. Creation, provision, rights, custody, physical custody, operational management, aggregation and publication are distinct roles.
3. InformationResource, Representation, FileOrBitstream and PhysicalCarrier are distinct entities.
4. Provenance, rights, access, spatial/temporal extent, preservation and quality are independent historical models.
5. Human readability, machine readability, playback requirements and preservation condition are separate axes.
6. High-impact decisions are not automatically finalized. Automated/AI processing produces candidates with evidence and confidence; a human records the final decision.
7. Requiredness R0–R6 and changeability C0–C4 are domain rules, not merely UI labels.
8. Map/drawing/time-space viewers complement, but do not replace, downloadable resources and metadata.
9. The Mitakihara VI and Web Design Guidelines are the UI baseline.
10. CKAN is optional. If adopted, it is a publication/catalog/search boundary, not the authoritative core domain model.

## Requiredness

- R0: system-required
- R1: business-required
- R2: conditionally required
- R3: required when known; unknown reason/investigation state retained
- R4: recommended
- R5: optional
- R6: system-generated

## Changeability

- C0: recorded fact; corrections are additive events
- C1: exceptional change; approval and evidence required
- C2: long-term change; validity history required
- C3: periodic change; versioned by revision
- C4: frequent change; event/time-series append

## Access and reuse

Access scope and reuse conditions must remain independent. Rights holder, copyright/rights type, license, permission scope, third-party rights, legal/contractual basis and validity period are not collapsed into one field.

## Standards

Detailed versions and the Mitakihara application profile remain architecture decisions. Candidate families include DCAT/SKOS, ISO 19115/19157, OGC API families, GeoPackage/GML/CityGML, SensorThings/O&M/SensorML, OAIS/PREMIS/METS/BagIt, IIIF/EAD/Dublin Core, WCAG 2.2/JIS X 8341-3/WAI-ARIA, and Creative Commons rights expressions.

## Source baseline

The formal source document is "Version 5 設計引継ぎ書" (document version 1.0, 2026-09-10). The live Version 5 site is a comparison target for screens and interaction. Approved Mitakihara VI/Web Guidelines and brand masters are separate authoritative brand sources.
