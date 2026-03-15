# Core Gameplay Loop

## Core Loop

```text
spawn enemies
→ fight
→ gain XP
→ level up
→ choose upgrade
→ modify world pressure
→ stronger waves
→ repeat
```

The player constantly balances between:

- increasing personal power
- increasing own-world difficulty for better rewards
- increasing opponent-world difficulty to apply pressure

## Match Start

At match start the game should:

1. load the map
2. initialize the navigation graph
3. initialize the wave system
4. create the player entity
5. apply initial match modifiers
6. start the wave timeline

## Upgrade Categories

Upgrade options can belong to the following categories:

- player power
- weapon upgrade
- artifact gain
- world modifier
- opponent curse

## Parallel Worlds

Each player has a separate world with:

- its own waves
- its own enemies
- its own modifiers

Some actions transfer modifiers to the opponent's world.

## Win / Lose Conditions

Lose condition:

- player health reaches 0

Win condition:

- opponent dies
- or time limit ends and the player has the better result
