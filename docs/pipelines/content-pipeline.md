# Content Pipeline

## Core Flow

```text
file → validate → normalize → register → runtime
```

## Goals

The content pipeline must provide:

- unified definitions
- validation before gameplay starts
- reference resolution
- normalization and defaults
- shared format between editor and runtime

## Definition Sources

Definitions are loaded from data folders such as:

- enemies
- weapons
- maps
- waves
- balance
- modifiers

## Validation

Validation must catch errors before match start, including:

- missing fields
- invalid types
- broken references
- invalid traversal data
- invalid map structure

## Registry Layer

Registries expose normalized definitions to runtime systems.

Examples:

- EnemyRegistry
- WeaponRegistry
- LevelRegistry
- WaveRegistry

## Rule

Definitions are the single source of truth for content.
