---
title: Typing React Components & Hooks
status: draft
last_reviewed: 09-11-2025
---

# Typing React Components & Hooks

## Function Components

- Preferred signature: `type Props = { title: string; onClick?: () => void }; const Button: React.FC<Props> = ({ title, onClick }) => { ... };`
- Consider defining return type explicitly (`React.ReactNode`, `JSX.Element`) for shared code.
- Use `PropsWithChildren` when accepting children (`type CardProps = React.PropsWithChildren<{ title: string }>`).

## Default Props & Optional Values

- Use default parameters in function signature (`({ size = "md" }: Props)`) to keep types aligned.
- Avoid legacy `Component.defaultProps` pattern; TypeScript handles optional props naturally.

## Event Handlers

- Leverage React event types: `React.MouseEvent<HTMLButtonElement>`, `React.ChangeEvent<HTMLInputElement>`.
- Generic event handlers: `React.FormEvent<HTMLFormElement>` for form submissions.
- Use `React.SyntheticEvent` as fallback when specific events aren’t needed.

## Hooks

- `useState` generics: `const [count, setCount] = useState<number>(0);`
- Derived state with union types to represent multiple shapes.
- Custom hooks should declare return type and parameter constraints:

```ts
function useFetch<T>(url: string): { data: T | null; loading: boolean; error: Error | null } { ... }
```

- `useReducer` requires typed reducers and actions (`type Action = { type: "add"; task: Task } | { type: "remove"; id: string }`).

## Context & Providers

- `const ThemeContext = createContext<ThemeContextValue | undefined>(undefined);`
- Create `useTheme` custom hook that throws when used outside provider.
- Memoize context value to avoid stale or untyped consumers.

## Forwarding Refs & Imperative Handles

- `const Input = forwardRef<HTMLInputElement, InputProps>((props, ref) => { ... });`
- Use `useImperativeHandle` to type imperative APIs (`useImperativeHandle(ref, () => ({ focus() { ... } }))`).

## Practice Prompts

- Type a reusable form component with generic data shape and onSubmit handler.
- Create a typed context for authentication state with strict null checks.
- Implement a `usePagination` hook returning typed helpers (next, prev, setPage) and ensure `setPage` accepts only valid values.
