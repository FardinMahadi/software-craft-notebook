---
title: TypeScript Basics
status: draft
last_reviewed: 09-11-2025
---

# TypeScript Basics

## Compiler Setup

- `tsconfig.json` key fields for React:
  - `"target": "ES2020"` (or project requirement).
  - `"module": "ESNext"` for bundlers, `"moduleResolution": "NodeNext"` for modern resolution.
  - `"jsx": "react-jsx"` or `"preserve"` for custom tooling.
  - Enable `"strict": true` to opt into best practices.
- Use `ts-node` or React bundler integration (Vite, Next.js) to compile TS.

## Types & Annotations

- Primitive types: `string`, `number`, `boolean`, `bigint`, `symbol`, `null`, `undefined`.
- Structural typing (`type User = { name: string; age: number }`) ensures shape compatibility.
- Optional properties: `age?: number`; read-only: `readonly id: string`.
- Use type aliases (`type`, `interface`) to describe reusable shapes.

## Union & Intersection

- Union (`type Result = Success | Failure`) express either/or.
- Intersection (`type Elevated = Base & Admin`) merges shapes; conflicts must be compatible.
- Narrow unions with control flow: `if ("error" in result) { ... }`.

## Generics

- Generic functions infer types: `function identity<T>(value: T): T`.
- Constrain generics with `extends`: `function pluck<T extends object, K extends keyof T>(obj: T, key: K)`.
- Default generic parameters: `type ApiResponse<T = unknown> = { data: T; error?: string }`.

## Type Assertions & Guards

- Prefer type narrowing over assertions; use assertions when calling third-party code (`value as HTMLInputElement`).
- Build reusable guards: `function isUser(value: unknown): value is User`.
- Non-null assertion `user!.email` should be used sparingly; consider optional chaining.

## Practice Prompts

- Configure a minimal `tsconfig.json` for a React project and explain each option.
- Create union types for API responses and narrow them safely in control flow.
- Implement a generic `pick` utility that returns a subset of object properties with proper typing.
