---
title: Debugging & Developer Tools
status: draft
last_reviewed: 09-11-2025
---

# Debugging & Developer Tools

Guidance from React docs on debugging, troubleshooting effects, and using DevTools effectively.

## React Developer Tools (Browser)
- Inspect component trees, props, hooks, and state live.
- Highlight updates to detect unnecessary re-renders.
- Use Profiler tab to capture flame charts and interaction timings.

## Console Techniques
- Use `console.log` sparingly; prefer `console.table`, `console.group` for structured logging.
- Warn on unexpected states with `console.warn`.
- Strip debugging logs in production builds using bundler plugins (e.g., Babel remove-console).

## Debugging Effects
- Ensure dependency arrays include all reactive values; lint rules help catch omissions.
- Split large effects into focused ones when debugging complex flows.
- Add cleanup functions to verify teardown occurs as expected (log messages).

## Error Boundaries & Runtime Errors
- Wrap UI trees with error boundaries to catch render errors and display fallback UI.
- Use `ErrorBoundary` components to log errors to observability tools (Sentry, LogRocket).
- React 19’s `use` and `throw` support integrate with async boundaries—test suspense fallbacks.

## Common Pitfalls Checklist
- Infinite re-renders: confirm state setters are not called during render.
- Stale closures: use functional updates to access latest state.
- Context mismatch: ensure providers wrap consumers and values are stable (`useMemo`).

## Practice Prompts
- Profile a component tree and identify at least one wasted render; document the fix.
- Implement an error boundary and simulate an error to confirm fallback UI.
- Diagnose an effect that triggers continuously and record the corrected dependency array.

