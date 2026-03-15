# Behavior DSL Specification

## Purpose

Behavior DSL is a declarative layer for describing behavior in data definitions.

It is intended to let the project build most enemies, totems, and some weapon behaviors without writing a dedicated class for each one.

It is **not** a full scripting language.

## Block Shape

```js
{
  type: "behavior_type",
  mode: "optional_mode",
  conditions: [],
  priority: 0,
  cooldown: null,
  tags: []
}
```

## Categories

### Targeting

Examples:

- acquire_target
- nearest_player
- owner_target

### Movement

Examples:

- chase_target
- keep_distance
- orbit_target
- flee_from_target

### Attack

Examples:

- melee_hit
- projectile_shot
- burst_projectile
- contact_damage
- pulse_wave

### Traversal Policy

Examples:

- preferHighGround
- allowJumpChase
- avoidHardDrop

### Reactive

Examples:

- on_hit
- on_low_hp
- on_death

### Passive / Periodic

Examples:

- emit_aura
- periodic_wave
- periodic_spawn
- regen

## Rule

If a mechanic cannot be expressed by existing blocks, add a new handler.
Do **not** turn the DSL into a free-form programming language.
