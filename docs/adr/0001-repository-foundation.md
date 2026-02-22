# 0001 Repository Foundation

- Status: Accepted
- Date: 2026-02-22

## Context
The project requires a clear repository structure and contribution model before implementation begins.

## Decision
Adopt a documentation-first foundation with separated domains:
- `crates/` for implementation modules
- `interfaces/` for protocol and schema contracts
- `docs/adr/` for architecture decisions

## Consequences
- Faster onboarding and shared language before coding
- Lower refactor risk from ambiguous module boundaries
- Delayed executable artifacts until contracts are better defined

## Alternatives Considered
- Start coding directly in a single crate (rejected due to architecture ambiguity)
- Keep all docs in `README.md` only (rejected due to scaling/maintainability concerns)
