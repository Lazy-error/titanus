# Network Architecture

## Core Decision

Use a **server-authoritative dual-world model**.

Players do not directly collide or fight in one shared physics space.
Instead, each player runs in a separate world while the server synchronizes:

- match time
- upgrades
- curses
- world modifiers
- wave state
- match outcome

## Why This Fits the Game

Because PvP is indirect:

- there is no direct player collision
- there is no shared duel arena
- most interactions happen through world pressure

This significantly simplifies networking compared to direct action PvP.

## Responsibilities

### Server

- authoritative match state
- world simulation state
- modifier application
- wave progression
- result resolution

### Client

- sends input
- renders local world
- predicts presentation where useful
- receives authoritative state updates

## Recommended Stack

- Node.js
- WebSocket
- event-driven sync
