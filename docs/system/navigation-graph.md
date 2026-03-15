# Navigation Graph Architecture

## Core Decision

Pathfinding runs on a **derived navigation graph**, not directly on raw render geometry.

Graph inputs:

- level data
- height layer
- collision layer
- traversal links
- entity traversal profile

## Graph Layers

```text
Level Data
→ Tile Graph
→ Entity-Specific Navigation Graph
→ Pathfinding
```

## Edge Types

- walk
- jump_up
- drop_down
- climb
- special

## Cost Model

Recommended base costs:

- walk = 1.0
- jump_up = 1.4
- drop_down = 1.1
- climb = 1.8

Surface modifiers may further change path cost.

## Dynamic Adjustments

Navigation should support:

- dynamic blockers
- dynamic cost modifiers
- cached graphs per traversal archetype

## Rule

No entity should move outside navigation rules unless that behavior is explicitly defined by traversal profile or special mechanics.
