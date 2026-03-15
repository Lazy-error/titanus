# Traversal Rules Specification

## Purpose

Traversal rules define how entities move between tiles with different height values.

Traversal affects:

- player control
- AI navigation
- combat positioning
- map design
- editor requirements

## Core Formula

```text
heightDelta = target.height - source.height
```

## Transition Types

### Walk

Allowed when:

- `heightDelta == 0`
- target tile is walkable

### Jump Up

Allowed when:

```text
heightDelta <= entity.maxJumpUpDelta
```

### Drop Down

Allowed when:

```text
abs(heightDelta) <= entity.maxDropDownDelta
```

### Climb

Requires:

- a `climb_edge` traversal link
- a matching `climbProfile`

### Special Traversal

Examples:

- ladder
- ramp
- monkey_path
- teleport
- drop_only

## Traversal Profile

Entities use traversal profiles such as:

- `maxJumpUpDelta`
- `maxDropDownDelta`
- `climbProfile`
- `canIgnoreHeightRules`

## Important Rule

Jump is both:

- a traversal mechanic
- a combat dodge mechanic

It may allow dodging totem waves or ground AoE.
