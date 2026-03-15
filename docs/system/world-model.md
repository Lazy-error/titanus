# World Model

## Core Decision

The game world is represented as a **grid-based map**.

The world is not stored as a navmesh. Instead:

- the map is authored as a grid
- height is discrete
- navigation is derived from the grid

## Tile Layers

A level definition contains multiple logical layers:

- height
- surface
- collision
- traversal links
- zones
- objects

## Height Model

Height is stored as a numeric discrete value and is **not limited to four levels**.

Examples:

- 0 — low ground
- 1 — ground
- 2 — ledge
- 3 — elevation
- 4+ — high platforms or special zones

## Collision Types

Recommended collision values:

- empty
- wall
- cliff
- void
- block_projectiles
- no_build

## Level Data Rule

The level data model is the single source of truth for:

- heights
- surfaces
- collisions
- traversal links
- zones
- map objects
