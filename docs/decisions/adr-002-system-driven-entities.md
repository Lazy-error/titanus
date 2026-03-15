# ADR-002 — System-Driven Entity Model

## Status
Accepted

## Decision
The project uses a system-driven entity model instead of full ECS as the core architecture.

Entities consist of:

1. definitions
2. runtime entities
3. behavior handlers

## Rationale
This provides a better fit for:

- special gameplay rules
- data-driven content
- editor integration
- readable debugging
- reusable behavior patterns
