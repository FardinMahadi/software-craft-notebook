---
title: Tooling & Integration
status: draft
last_reviewed: 09-11-2025
---

# Tooling & Integration

## Project Setup

- Create new projects with TypeScript templates (`npm create vite@latest my-app -- --template react-ts`, `npx create-next-app@latest --ts`).
- Convert existing JavaScript project by renaming files to `.ts`/`.tsx`, updating imports, adding `tsconfig.json`.
- Ensure bundler supports TS: Vite (esbuild), Next.js (SWC), Webpack (ts-loader or swc-loader).

## tsconfig Essentials

- Base options:
  - `"strict": true` for full type checking.
  - `"isolatedModules": true` with Babel/ts-jest pipelines.
  - `"esModuleInterop": true` for compatibility with CommonJS modules.
  - `"paths"` for module aliases; update bundler config accordingly (e.g., Vite `resolve.alias`).
- `types` array controls global typings; include testing libraries (e.g., `"types": ["vitest/globals"]`).

## ESLint & Prettier

- Use `@typescript-eslint/parser` and `@typescript-eslint/eslint-plugin`.
- Extend recommended configs: `"extends": ["eslint:recommended", "plugin:@typescript-eslint/recommended", "plugin:react/recommended"]`.
- Configure Prettier integration with `eslint-config-prettier` to disable conflicting rules.

## Testing & Type Checking

- Use TS-aware test runners: Vitest, Jest (with `ts-jest` or Babel), Testing Library for React.
- Configure `tsconfig.test.json` for tests if needed (looser rules, DOM libs).
- Set up type checking script (`"typecheck": "tsc --noEmit"`) for CI.

## Monorepos & Shared Types

- Leverage project references (`"references": [{ "path": "../shared" }]`) for multi-package setups.
- Share type definitions via separate packages or `@types` directory.
- Keep consistent TS versions across workspace to avoid mismatches.

## Practice Prompts

- Convert a JavaScript utility file to TypeScript and describe the required changes.
- Configure ESLint with TypeScript in an existing project and run linting scripts.
- Add a path alias to access shared types (`@/types`) and update bundler config to resolve it.
