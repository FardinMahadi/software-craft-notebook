---
title: React TypeScript Practice Lab
status: not-started
last_reviewed: 09-11-2025
---

## Goal

Strengthen TypeScript usage in React components by implementing typical UI patterns with robust types.

## Tasks

1. Build a typed `Button` component supporting variant props, default props, and event handlers.
2. Create a `useAsync` hook typed with generics for resolved data and error shape; test with fetch calls.
3. Implement an `AuthContext` with discriminated union state (`idle | loading | authenticated | error`) and ensure consumers cannot access undefined values.
4. Type a reducer-based form manager with discriminated actions and exhaustive switch statements.

## Deliverables

- Code samples or links demonstrating each task with appropriate types.
- Notes on typing challenges (e.g., event types, union narrowing) captured in concept files or daily notes.
- Checklist updates referencing the lab completion.
