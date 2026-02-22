# MedNode

MedNode is an open-source interoperability platform concept for healthcare networks.  
This repository is currently in **foundation phase**: structure, documentation, and project scaffolding are in place, with implementation to follow.

## Vision
Clinical data often stays locked inside fragmented EHR systems and legacy interfaces.  
MedNode aims to become a translation and routing layer that helps normalize and share data across HL7v2 and FHIR ecosystems with a strong focus on safety, performance, and reliability.

## Current Status
- Repository scaffolding and architecture documentation
- Team/process standards for contribution and security reporting
- Domain structure for parser, router, and interface specs
- No production code committed yet

## Proposed System Components
- `mednode-parser`: Ingest and normalize HL7v2 payloads
- `mednode-router`: Route normalized events between trusted nodes
- `mednode-core`: Shared domain models, contracts, and primitives

## Repository Layout
```text
.
├── crates/
│   ├── mednode-core/
│   ├── mednode-parser/
│   └── mednode-router/
├── docs/
│   ├── adr/
│   ├── architecture.md
│   └── roadmap.md
├── interfaces/
│   ├── fhir-r4/
│   └── hl7v2/
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── SECURITY.md
└── README.md
```

## Next Build Steps
1. Lock RFC/ADR decisions for message boundaries and error models.
2. Define canonical HL7v2-to-FHIR mapping contracts.
3. Bootstrap Rust workspace and crate targets.
4. Add CI checks (format, lint, test, security scan).

## Roadmap
- **Phase 1:** HL7v2 parsing + FHIR R4 normalization baseline
- **Phase 2:** Multi-node routing and state synchronization primitives
- **Phase 3:** Operational hardening, compliance tooling, and hosted control plane

## License
Apache License 2.0
