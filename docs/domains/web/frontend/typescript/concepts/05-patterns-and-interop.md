---
title: Typed Patterns & Interop
status: draft
last_reviewed: 09-11-2025
---

# Typed Patterns & Interoperability

## Interacting with JavaScript & Third-Party Libraries

- Use declaration files (`.d.ts`) or ambient module declarations when libraries lack types.
- Rely on DefinitelyTyped (`@types/...`) packages for popular libraries.
- For dynamic imports, annotate default exports: `const module = (await import("./legacy.js")) as { legacyFn: () => void };`

## Type Guards & Refinements

- Custom type guards improve type narrowing:

```ts
function isError(value: unknown): value is Error {
  return value instanceof Error;
}
```

- Use discriminant fields or `in` checks to narrow API responses.

## Error Handling Types

- Represent API errors using union types: `type ApiResult<T> = { data: T; error: null } | { data: null; error: ApiError };`
- Ensure React components handle both branches explicitly.

## Forms & Controlled Inputs

- Create form state types (e.g., `type LoginForm = { email: string; password: string }`).
- Use `keyof` to create reusable change handlers: `function handleChange<K extends keyof LoginForm>(field: K, value: LoginForm[K])`.
- Integrate with libraries (`react-hook-form`, `formik`) using provided type helpers.

## State Machines & Reducers

- Combine discriminated unions with reducers:

```ts
type Action =
  | { type: "start" }
  | { type: "success"; payload: Data }
  | { type: "failure"; error: string };
```

- Ensure exhaustive checks via `default` case that throws (`const exhaustive: never = action;`).

## Public API Design

- Export types alongside functions (`export type { User }`) to aid consumers.
- Avoid default exports for shared types to encourage named imports.
- Provide utility types for consumers to extend (`type ThemeConfig = Partial<ThemeTokens>`).

## Practice Prompts

- Type a reducer with discriminated union actions and ensure exhaustive checking.
- Extend type definitions for a library missing certain interfaces (declare module augmentation).
- Implement a form state manager using generics to ensure field names align with the data shape.
