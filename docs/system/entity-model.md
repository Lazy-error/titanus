# Entity Model

## Core Decision

The project uses a **system-driven entity model**, not full ECS as the main architecture.

Each gameplay entity has three layers:

1. **Definition** — data description
2. **Runtime Entity** — live state in match
3. **Behavior Handlers** — systems executing logic

## Runtime Entity

A runtime entity should contain at minimum:

- id
- entityType
- definitionId
- position
- state
- baseStats
- activeModifiers
- computedStats
- behaviorState
- flags
- tags

## Why Not Full ECS

The project contains many special gameplay rules:

- height logic
- traversal exceptions
- propagation rules
- totems
- curses
- editor integration

A full ECS-first approach would increase complexity without enough benefit at the current project scope.
