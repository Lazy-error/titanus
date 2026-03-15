# Advanced Stat & Modifier System

## Goal

The stat system calculates all meaningful gameplay numbers in a consistent, inspectable way.

It must support:

- enemies
- weapons
- totems
- curses
- artifacts
- progression
- traversal modifiers
- world pressure

## Runtime Representation

Entities should carry:

- `baseStats`
- `activeModifiers`
- `computedStats`

## Pipeline Order

Recommended order:

1. definition base stats
2. global balance modifiers
3. mode/world modifiers
4. progression modifiers
5. artifact/curse modifiers
6. temporary runtime buffs/debuffs
7. derived stat calculations
8. final caps / clamps / rounding

## Modifier Operations

Supported operations should include:

- flat
- multiplier
- override
- cap_min
- cap_max
- derived

## Rule

Gameplay systems must not patch final stats directly.
They should add or remove modifiers and let the stat resolver compute results.
