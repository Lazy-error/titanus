# TITANUS Documentation

This directory contains the architectural, design, and production documentation for the TITANUS project.

TITANUS is a data-driven PvP survivor game built with **JavaScript + Phaser**, featuring pseudo-3D height gameplay, procedural enemy waves, and indirect PvP pressure between players.

The goal of the project is not only to build a game but also to create a **content-driven runtime platform and toolchain** that allows fast iteration on enemies, weapons, maps, waves, and balance.

---

# Documentation Structure

The documentation is organized into several logical sections.

docs/
├── vision
├── design
├── system
├── pipelines
└── decisions

Each section serves a different purpose.

---

# Vision

High-level description of the project and product goals.

docs/vision/

| Document | Description |
|--------|-------------|
| project-vision.md | Overall concept of the game and its main goals |

---

# Design

Gameplay design and player experience.

docs/design/

| Document | Description |
|--------|-------------|
| core-gameplay-loop.md | Core loop of the survivor gameplay |
| visual-reference.md | Visual reference for the pseudo-3D map layout |

---

# System

Technical architecture of gameplay systems.

docs/system/

| Document | Description |
|--------|-------------|
| world-model.md | Grid world model and height layers |
| traversal-rules.md | Movement rules between height levels |
| navigation-graph.md | Navigation graph and pathfinding model |
| combat-height-rules.md | Combat rules affected by height differences |
| entity-model.md | Runtime entity architecture |
| behavior-dsl.md | Behavior scripting system for enemies |
| stat-system.md | Stat and modifier resolution system |
| wave-system.md | Enemy wave spawning architecture |
| editor-mvp.md | Initial scope of the level editor |
| scalability-performance.md | Performance and scalability architecture |
| network-architecture.md | Multiplayer synchronization model |

---

# Pipelines

Production and development pipelines.

docs/pipelines/

| Document | Description |
|--------|-------------|
| content-pipeline.md | Data-driven content pipeline |
| repository-structure.md | Repository and monorepo architecture |

---

# Decisions (ADR)

Architecture Decision Records.

docs/decisions/

| Document | Description |
|--------|-------------|
| adr-001-grid-world.md | Decision to use a grid-based world model |
| adr-002-system-driven-entities.md | Decision to use system-driven runtime entities |
| adr-003-height-is-gameplay.md | Height system as a core gameplay mechanic |
| adr-004-balance-layer.md | Centralized balance configuration layer |
| adr-005-editor-shares-runtime-format.md | Editor uses the same data formats as runtime |

---

# How to Use This Documentation

When working on the project:

1. Start with **Vision** to understand the project goals.
2. Read **Design** to understand gameplay.
3. Use **System** documents when implementing game systems.
4. Check **Pipelines** for repository and content workflows.
5. Use **Decisions** to understand architectural tradeoffs.

---

# Documentation Rules

When new systems are introduced:

• create a new document under `docs/system`  
• update this README index  
• record important architecture choices in `docs/decisions`

Documentation should always describe **concepts and architecture**, not implementation details.

---

# Related Directories

data/       → game content definitions  
schemas/    → validation schemas  
packages/   → runtime, editor, server code  
prototypes/ → experimental systems  
tools/      → development tools  

---

# Project Principle

TITANUS is built around **data-driven gameplay systems**.

Content should be modifiable without rewriting engine code.

The engine interprets data; the data defines gameplay.