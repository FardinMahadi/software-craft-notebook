---
title: Reducers & State Machines
status: draft
last_reviewed: 09-11-2025
---

# Reducers & State Machines

Summarizes the React docs sections “Extracting State Logic into a Reducer” and related guidance.

## When to Use Reducers
- State logic involves many events or complex transitions.
- Multiple components need to dispatch actions that affect shared state.
- You want predictable state transitions centralised in one function.

## Anatomy of a Reducer
- Signature: `(state, action) => newState`.
- Must be pure: no side effects, no asynchronous work, no mutation.
- Action objects typically have a `type` and optional payload.

```jsx
function tasksReducer(state, action) {
  switch (action.type) {
    case "added": {
      return [...state, action.task];
    }
    case "updated": {
      return state.map((task) =>
        task.id === action.task.id ? action.task : task
      );
    }
    case "deleted": {
      return state.filter((task) => task.id !== action.id);
    }
    default: {
      throw new Error("Unknown action type: " + action.type);
    }
  }
}

const [tasks, dispatch] = useReducer(tasksReducer, initialTasks);
```

## Action Patterns
- Use constants/enums for action types to avoid typos.
- Keep payload minimal but sufficient for the transition.
- Group related updates into one action to prevent sequential dispatch churn.

## Transition Tables & State Machines
- Map combinations of current state and action to new state.
- Helps validate coverage (no missing cases).
- Optional: use libraries like XState when transitions become graph-like.

## Side Effects with Reducers
- Keep reducers pure; perform side effects in the component or via custom hooks.
- Use effects (`useEffect`) triggered by state changes to sync with external systems.
- For async logic, dispatch actions before/after (e.g., `fetch-started`, `fetch-success`).

## Testing Reducers
- Reducers are pure functions; unit test them directly.
- Provide sample states and actions and assert resulting state.
- Document invariants (e.g., no duplicate IDs) via tests.

## Scaling Patterns
- Co-locate reducer files with components that own the state.
- Use context providers (`const TasksContext = createContext`) to expose `[state, dispatch]`.
- Memoize context value (`useMemo(() => ({ tasks, dispatch }), [tasks])`) to prevent re-renders.

## Practice Prompts
- Convert a multi-action `useState` implementation to `useReducer` and compare readability.
- Add optimistic updates to a reducer-based list, handling success/failure events.
- Write unit tests covering all reducer branches, including error paths.

