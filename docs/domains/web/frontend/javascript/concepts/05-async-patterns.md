---
title: Asynchronous Patterns & Browser APIs
status: draft
last_reviewed: 09-11-2025
---

# Asynchronous Patterns & Browser APIs

## Why It Matters

- Modern apps depend on asynchronous workflows for network requests, scheduling, and browser APIs. Understanding the event loop prevents race conditions and unhandled errors.

## Core Ideas

- **Event loop refresher:** distinguish macro tasks (`setTimeout`, DOM events) and microtasks (Promises, `queueMicrotask`); React scheduling often leverages microtasks.
- **Promises:** handle lifecycle (pending → fulfilled/rejected), chain with `.then/.catch/.finally`, and coordinate with `Promise.all`, `Promise.allSettled`, `Promise.race`, `Promise.any`.
- **Async/await:** syntactic sugar over promises; wrap `await` in `try/catch`, parallelize with `Promise.all`, convert callback APIs to promises.
- **Fetch & AbortController:** check `response.ok`, parse with `response.json()`, pass `AbortController` signals to cancel requests.
- **Timers & scheduling:** use `setTimeout`, `setInterval`, `requestAnimationFrame`; clear timers on cleanup (especially in React effects); leverage `queueMicrotask` for post-render adjustments.
- **Error handling & retry:** implement backoff strategies, propagate errors, surface issues via UI or logging.

## Real-World Scenario

- A React dashboard wraps `fetch` in a utility that adds timeouts, retries, and abort support. During component unmount, the effect cleanup calls `controller.abort()` to prevent setting state on an unmounted component.

## Follow-up

- [ ] Write a utility that wraps fetch with timeout, retry, and JSON parsing.
- [ ] Demonstrate how microtasks and macrotasks interleave by logging inside different callbacks.
- [ ] Build a data loader that batches concurrent requests with `Promise.all` and handles partial failures.
