---
title: Managing State
status: draft
last_reviewed: 09-11-2025
---

# Managing State

Organize state for complex UIs by choosing the right structure, sharing between components, and extracting logic.

## Reacting to Input

- Sync form inputs with state using controlled components (`value` + `onChange`).
- Derive state from props when necessary but avoid duplicating props in state unless you need to “remember” changes.

## Choosing State Structure

- Keep state minimal; prefer derived values computed during render.
- Normalize state for collections (store IDs separately from items).
- Group related state in objects when updates should stay in sync.

## Sharing State Between Components

- Lift state to the closest common ancestor.
- Pass down state and setters or derived data/handlers as props.
- For deep trees, consider context to avoid prop drilling.

## Preserving & Resetting State

- React preserves state by element position in the tree; changing `key` resets stateful components.
- Use keys to intentionally reset forms or keep state isolated between list items.

## Reducers & Context (See Dedicated Notes)

- Use reducers when state transitions grow complex or events originate from multiple components.
- Reach for context when data must be shared widely without prop drilling.
- Detailed guidance now lives in `07-reducers.md` and `08-context-scaling.md`.

## Practice Prompts

- Refactor a prop-drilled theme toggler using patterns from the context/scaling note.
- Build a reducer-driven todo app that supports add/toggle/delete and persists state (see reducers note).
- Use keys to reset form state when switching between list items and document when resets occur.
