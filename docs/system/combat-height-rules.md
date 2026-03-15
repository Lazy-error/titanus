# Combat Height Rules

## Goal

Height must influence combat mechanically, not only visually.

It should affect:

- damage advantage
- effective range
- AoE propagation
- tactical safety
- totem wave behavior

## Height Delta

```text
heightDelta = attacker.height - target.height
```

## High Ground Bonus

When the attacker is above the target, damage receives a bonus.

Suggested shape:

```text
damageMultiplier = 1 + (heightDelta * HIGH_GROUND_DAMAGE_BONUS)
```

## Low Ground Penalty

When attacking upward, optional penalties may apply to:

- damage
- effective range

## AoE Propagation

Many effects should propagate:

- on the same level
- downward

but **not upward**.

## Totem Wave Rule

Totem waves should:

- affect same level
- spread downward
- not spread upward

## Jump Interaction

If the entity is airborne, jump may allow dodging:

- totem waves
- some ground AoE
