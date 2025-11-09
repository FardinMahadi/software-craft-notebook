---
title: Advanced Type System
status: draft
last_reviewed: 09-11-2025
---

# Advanced Type System Features

## Type Inference & Widening

- TypeScript widens literal types (`const status = "ready"` inferred as `"ready"` if `const`; as `string` if `let`).
- Use `as const` to preserve literal types, especially for discriminated unions or config objects.

## Discriminated Unions

- Combine union members with a literal discriminant field:

```ts
type Status =
  | { kind: "idle" }
  | { kind: "loading" }
  | { kind: "success"; data: string[] }
  | { kind: "error"; message: string };
```

- Switch statements or `if (state.kind === "success")` narrow types automatically.

## Utility Types

- Built-in helpers:
  - `Partial<T>`, `Required<T>`, `Readonly<T>`
  - `Pick<T, K>`, `Omit<T, K>`
  - `Record<K, T>`, `ReturnType<T>` , `Parameters<T>`
  - `NonNullable<T>`
- Compose to create flexible state shapes (`Partial` for form drafts).

## Index Signatures & Mapped Types

- Index signatures: `type Dictionary = { [key: string]: string }`.
- Mapped types transform keys: `type Optional<T> = { [K in keyof T]?: T[K] };`.
- Use `keyof` to reference property names generically.

## Conditional Types

- `type IsArray<T> = T extends unknown[] ? true : false`.
- Combine with `infer` to extract types: `type ElementType<T> = T extends (infer U)[] ? U : T`.
- Useful for deriving event handler types or API response structures in React.

## Template Literal Types

- Compose strings at type level: `type EventName = `on${Capitalize<string>}`;`.
- Enforce naming conventions for props or CSS variables.

## Practice Prompts

- Build a discriminated union representing async request states and use it in a reducer.
- Implement a mapped type that converts all properties of a type to optional functions (`Wrap<T>`).
- Create a conditional type `DeepReadonly<T>` that recursively marks nested properties as read-only.
