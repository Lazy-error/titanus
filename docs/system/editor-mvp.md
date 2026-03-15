# Level Editor MVP Specification

## Goal

The level editor is part of the content pipeline, not a side tool.

The MVP editor must allow:

- creating a map
- painting heights
- painting surfaces
- assigning collisions
- placing spawns
- creating traversal links
- saving levels in the runtime data format

## Editing Layers

- height layer
- surface layer
- collision layer
- zone layer
- traversal links
- objects layer

## Core Tools

### Height Paint Tool

Must support:

- raise height
- lower height
- flatten
- set exact height

Height levels are discrete and not limited to four values.

### Collision Tool

Suggested values:

- none
- wall
- cliff
- void

### Traversal Link Tool

Used for:

- climb edges
- ladders
- ramps
- drop-only transitions

### Spawn Tool

Used for:

- player spawns
- enemy spawns
- wave spawn zones
- miniboss spawns

## Rule

The editor must save the same definitions the runtime consumes, without a separate private format.
