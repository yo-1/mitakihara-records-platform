# Codex Handoff

## Mission

Implement the successor Mitakihara Records Platform from the approved design baseline. The repository implementation is the main line. Version 5 is read-only reference material for UI, interaction, VI and test scenarios.

## Read first

1. README.md
2. docs/DESIGN_BASELINE.md
3. docs/ARCHITECTURE_BOUNDARY.md
4. docs/ACCEPTANCE_CRITERIA.md
5. CONTRIBUTING.md
6. prototype/README.md
7. assets/brand/README.md

## First implementation milestone

Do not begin with a CKAN organization/dataset schema. First establish domain vocabulary, identifiers and testable schemas for:
- administrative classification and validity periods;
- Agent + RoleAssignment;
- rights and access separation;
- R0–R6 requiredness;
- C0–C4 changeability;
- InformationResource / Representation / FileOrBitstream / PhysicalCarrier separation.

Then implement persistence/search/detail/registration/history/audit APIs against fictional data.

## Non-negotiable behavior

- Historical department names remain searchable after reorganization.
- Provider, aggregator, rights holder, custodian, manager and publisher may all differ.
- Access scope and reuse conditions are independently enforced.
- Original carrier, preservation representation, access representation and machine-processing representation can be related.
- Human and machine readability are independently assessed.
- Unreadable damaged media can be registered without inventing its content.
- AI suggestions retain candidate, evidence, confidence, processing history and human decision.
- Public outputs expose only authorized data and display provenance/time/CRS/quality/rights/reuse/acquisition information where applicable.

## Change protocol

For each PR state: design basis, changed modules, verification, completion criteria, and unverified items. Architecture decisions that resolve an open design question must be recorded as ADRs rather than silently embedded in code.

## Out of scope for the first Codex pass

- Final selection of CKAN versus another publication catalog.
- Final OGC/ISO/PREMIS application-profile versions.
- Production IAM.
- Destructive disposal or physical restoration automation.
- Production deployment.
