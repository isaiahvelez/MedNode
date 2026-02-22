# Architecture Overview

## Problem Domain
Healthcare systems frequently exchange data through legacy HL7v2 interfaces while modern applications expect FHIR resources.

## Proposed Bounded Components
- **Parser Domain (`mednode-parser`)**
  - Input: HL7v2 messages and transport metadata
  - Output: validated canonical events
- **Core Domain (`mednode-core`)**
  - Shared contracts, canonical event model, and error taxonomy
- **Router Domain (`mednode-router`)**
  - Delivery guarantees, node-to-node exchange, and synchronization policies

## Non-Functional Priorities
1. Memory safety and deterministic behavior
2. Low latency under high message throughput
3. Auditability and traceability
4. Explicit error handling and resilience

## Boundary Decisions (Initial)
- Parsing logic and routing logic remain isolated by contract.
- Interface adapters live near protocol boundaries, not in domain core.
- External integrations should depend on stable contracts, not internal parser internals.

## Open Questions
- Canonical event schema versioning strategy
- FHIR profile strictness level at MVP
- Message deduplication and replay semantics
