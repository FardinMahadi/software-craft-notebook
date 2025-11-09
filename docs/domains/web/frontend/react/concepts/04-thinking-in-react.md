---
title: Thinking in React
status: draft
last_reviewed: 09-11-2025
---

# Thinking in React

Summarizes the canonical process for designing React UIs from the “Thinking in React” guide.

## Step 1: Break the UI into a Component Hierarchy
- Sketch the UI and draw boxes around logical pieces.
- Single responsibility principle: components do one thing well.
- Map boxes to component tree; reuse components where structure repeats.

## Step 2: Build a Static Version
- Implement components that render the model data without interactivity.
- Pass data via props; avoid using state until necessary.
- Static version clarifies component boundaries and data requirements.

## Step 3: Identify Minimal State
- Determine which pieces of data need to be mutable.
- Ask: can this be derived from props or state? If yes, don’t store it separately.
- Keep state minimal and colocated with components that own it.

## Step 4: Determine Where State Lives
- Find common ancestors that need to share state.
- Hoist state to the closest parent that uses it or passes it down.
- When multiple siblings need the same data, lift state to their parent.

## Step 5: Add Inverse Data Flow
- Implement callbacks to let child components update parent state.
- Use event handlers to propagate changes upward (`onChange`, `onToggle` patterns).
- Keep data flow predictable by having a single “source of truth”.

## Practice Prompts
- Choose a small app idea (e.g., product filter) and produce component tree diagrams before coding.
- Build a static version of the UI solely with props; note how the data flows.
- Add interactivity step-by-step, documenting state ownership decisions.

