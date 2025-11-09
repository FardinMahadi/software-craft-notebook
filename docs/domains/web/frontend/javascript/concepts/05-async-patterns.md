---
title: Asynchronous Patterns & Browser APIs
status: draft
last_reviewed: 09-11-2025
---

# Asynchronous Patterns & Browser APIs

## Event Loop Refresher

- Macro tasks (setTimeout, DOM events) vs microtasks (Promises, queueMicrotask).
- React scheduling leverages microtasks; understand ordering to avoid race conditions.

## Promises

- Promise lifecycle: pending → fulfilled/rejected.
- Chain with `.then`, `.catch`, `.finally`; always handle rejection to avoid unhandled errors.
- Use `Promise.all`, `Promise.allSettled`, `Promise.race`, `Promise.any` for coordination.

## Async/Await

- Syntactic sugar over promises; `await` pauses execution within async function until promise settles.
- Wrap `await` calls in `try/catch`; consider `Promise.all` for parallel awaits.
- Convert callback-based APIs (e.g., IndexedDB) into promises for async/await compatibility.

## Fetch & AbortController

- Fetch returns a promise; check `response.ok`, parse with `response.json()`.
- Abort requests with `AbortController`; pass signal to fetch and abort during cleanup.

## Timers & Scheduling

- `setTimeout`, `setInterval`, `requestAnimationFrame` for scheduling tasks.
- Clear timers on cleanup (especially in React effects) to avoid leaks.
- Use `queueMicrotask` for post-render adjustments without layout thrash.

## Error Handling & Retry

- Implement exponential backoff or limit retries for network calls.
- Bubble errors to calling context; in React, surface to error boundaries or UI messaging.
- Log errors with metadata for observability.

## Practice Prompts

- Write a utility that wraps fetch with timeout, retry, and JSON parsing.
- Demonstrate how microtasks and macrotasks interleave by logging inside different callbacks.
- Build a small data loader that batches concurrent requests with `Promise.all` and handles partial failures.
