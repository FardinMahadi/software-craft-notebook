---
title: Context & Scaling Up State
status: draft
last_reviewed: 09-11-2025
---

# Context & Scaling Up State

Summaries from “Passing Data Deeply with Context” and “Scaling Up with Reducer and Context”.

## When Context Makes Sense
- Data or handlers must be accessible deep in the tree without prop drilling.
- Multiple siblings need the same state and passing props through intermediate layers is noisy.
- Works best for settings, theming, authentication, router data, or global stores.

## Creating Context
```jsx
const ThemeContext = createContext("light");

function ThemeProvider({ children }) {
  const [theme, setTheme] = useState("light");
  const value = useMemo(() => ({ theme, setTheme }), [theme]);
  return (
    <ThemeContext.Provider value={value}>
      {children}
    </ThemeContext.Provider>
  );
}

function useTheme() {
  const context = useContext(ThemeContext);
  if (!context) throw new Error("useTheme must be used within ThemeProvider");
  return context;
}
```

## Avoiding Re-render Storms
- Memoize provided values (`useMemo`, `useCallback`) so consumers only update when necessary.
- Split providers when different data updates at different rates (e.g., Auth vs Theme).
- For frequently changing large data, consider selectors or external stores (`useSyncExternalStore`).

## Context + Reducer Pattern
- Pair context with a reducer to create a predictable store.
- Provider manages `[state, dispatch]` and exposes via custom hooks (`useTasks`).
- Dispatch actions from any consumer without prop drilling.

## Scaling Strategies
- Add module-level providers close to usage rather than wrapping the entire app.
- Create composition-friendly provider components (e.g., `<TaskProvider>`).
- Document dependencies between providers (some may rely on others).

## Anti-Patterns
- Using context for unrelated data—creates unnecessary coupling.
- Overusing context for frequently changing UI state; local state or props may suffice.
- Storing derived data in context instead of computing from base state.

## Practice Prompts
- Refactor a prop-drilled settings menu to use context and note re-render impacts.
- Implement a context + reducer store for notifications with add/remove actions.
- Profile context providers to ensure memoization strategies prevent excessive renders.

