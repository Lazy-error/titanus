# ADR-001 — Grid World with Derived Navigation Graph

## Status
Accepted

## Decision
The game world is represented as a grid-based map.
Navigation is implemented as a derived graph built from:

- height
- collision
- traversal links
- entity traversal profile

## Rationale
This fits:

- tile-based map authoring
- multi-level height gameplay
- editor requirements
- predictable serialization
- traversal-aware pathfinding
