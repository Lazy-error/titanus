# Wave System Architecture

## Goal

The wave system controls escalating survivor pressure through a fully data-driven model.

It should manage:

- wave phases
- enemy selection
- spawn zones
- threat scaling
- miniboss events
- totem integration
- PvP pressure modifiers

## Main Components

- wave timeline
- spawn pools
- spawn zones
- threat budget
- difficulty scaling
- event triggers

## Wave Timeline

Example:

```js
[
  { time: 0, profile: "early_wave" },
  { time: 120, profile: "mid_wave" },
  { time: 300, profile: "late_wave" }
]
```

## Threat Budget

Each enemy has a `threatCost`.
A wave receives a budget and spends it by spawning combinations of enemies.

## PvP Pressure

Players may apply modifiers such as:

- extra threat budget
- stronger enemies
- faster spawn rate
- miniboss chance increase

## Rule

Wave logic must be assembled from definitions, not hardcoded in per-map or per-enemy logic.
