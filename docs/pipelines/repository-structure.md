# Repository Structure

## Recommended Layout

```text
project-root/
  data/
  docs/
  packages/
    editor/
    game-client/
    server/
    shared/
  prototypes/
  schemas/
  scripts/
  tools/
```

## Package Roles

### game-client

Runtime game code:

- core
- rendering
- combat
- scenes
- navigation
- systems
- waves
- pvp

### server

Match orchestration and authoritative world state.

### editor

Authoring tools for maps, entities, balance, and preview.

### shared

Reusable code shared between client, server, editor, and utilities.

Examples:

- RNG
- math helpers
- config helpers
- schema helpers
- constants

## Rule

Shared runtime code belongs in `packages/shared/src`, not in scripts or one-off tools.
