# PvP Survivor — Project Vision

## Working Description

**PvP Survivor** is a data-driven top-down / pseudo-3D survivor game built with **JavaScript + Phaser**.

Players do **not** fight each other directly. Instead, they survive in **parallel worlds** and apply pressure indirectly by modifying their own world or the opponent's world through:

- curses
- totems
- wave modifiers
- miniboss events
- artifacts and progression choices

The core idea is that leveling up is not only about becoming stronger, but also about **deciding where to place additional danger**:

- strengthen yourself
- strengthen your own world in exchange for better rewards
- strengthen the opponent's world to pressure them

This creates **asymmetric PvP pressure**, not direct arena combat.

## Product Goal

Build not only one game, but a **stable data-driven gameplay foundation / mini-engine** that supports:

- new enemies
- new weapons
- new totems
- new curses
- new maps
- new wave profiles
- new modes

without repeatedly rewriting the core runtime.

## Gameplay Pillars

1. **Survivor pressure** — escalating waves drive constant risk.
2. **Indirect PvP** — players affect each other through world pressure, not direct combat.
3. **Height as gameplay** — pseudo-3D is tactical, not decorative.
4. **Jump as traversal and dodge** — movement is part of combat.
5. **Data-driven content** — new content should be added through definitions.

## MVP Scope

The MVP should include:

- 1 playable map
- 1 player in the first local prototype
- 5 enemy types
- 2–3 weapons
- 2 totems
- XP and level-up loop
- upgrade selection with self/world/opponent pressure choices
- map editor MVP
- centralized balance config

## Design Constraint

Direct player-vs-player collision is **not** part of the current design.
