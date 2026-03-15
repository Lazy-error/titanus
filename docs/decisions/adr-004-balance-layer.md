# ADR-004 — Centralized Balance Layer

## Status
Accepted

## Decision
Balance is maintained through a centralized balance configuration layer applied over entity definitions.

Definitions store base values.
The balance layer stores:

- global multipliers
- mode overrides
- wave scaling
- experiment flags

## Rationale
This allows fast balancing and testing without touching many content files.
