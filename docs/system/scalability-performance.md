# Scalability & Performance Architecture

## Goal

The project must scale to large numbers of enemies and effects without abandoning the data-driven architecture.

## Two Runtime Layers

### Layer A — Gameplay Entities

Full-featured entities for:

- player
- elites
- minibosses
- totems
- special projectiles
- interactive objects

### Layer B — Mass Entities

Lightweight pooled entities for:

- simple enemies
- simple projectiles
- hazards
- VFX-heavy objects

These may use packed arrays instead of heavy object state.

## Spatial Partitioning

Use a chunk system to accelerate:

- nearby target queries
- collision checks
- spawn density control
- local AI calculations

Recommended starting chunk sizes:

- 8×8 tiles
- 16×16 tiles

## Deterministic RNG

All random gameplay must use seeded deterministic RNG for:

- reproducibility
- networking
- balance testing
- replayability

## Rule

Optimization should extend the architecture, not replace it.
Behavior DSL and data-driven definitions remain the foundation.
